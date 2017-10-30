---
title: 'Basic Authentication'
taxonomy:
    category:
        - docs
---

### Overview
cAPI's REST API is protected by the same restrictions which are provided via Joomla's standard web interface. This means that if you do not log in, you are accessing cAPI anonymously. Furthermore, if you log in and do not have permission to access something in Joomla, you will not be able to access it using the cAPI REST API either.

In most cases, the first step in using the cAPI REST API is to authenticate a user account with your Joomla site. Any authentication that works against Joomla will work against the REST API. On this page we will show you a simple example of basic authentication.

**Simple example**

Most client software provides a simple mechanism for supplying a user name and password and will build the required authentication headers automatically. For example you can specify the -u argument with curl as follows:
``` bash
curl -D- -u Bob:Loblaw -X GET -H "Content-Type: application/json" https://yoursite.com/api/v1/user
```
**Supplying Basic Auth headers**

If you need to you may construct and send basic auth headers yourself. To do this you need to perform the following steps:

* Build a string of the form username:password
* Base64 encode the string
* Supply an "Authorization" header with content "Basic " followed by the encoded string. For example, the string "bob:loblaw" encodes to "Ym9iOmxvYmxhdw==" in base64, so you would make the request as follows.
curl -D- -X GET -H "Authorization: Basic Ym9iOmxvYmxhdw==" -H "Content-Type: application/json" "https://yoursite.com/api/v1/user"



### Troubleshooting

#### PHP Does Not See Authorization Header

( [original source](https://cweiske.de/tagebuch/php-apache-authorization.htm) )

While implementing a token endpoint you may notice that you are unable to access the value of an HTTP Authorization header - $_SERVER did not include it. 

``` bash
$ curl -H 'Authorization: Basic U1RBUkJVVFRPTlNOT1RUVUJSQVRT' 127.0.0.1/securepage.php |grep -i auth
$
```

It turns out that you manually have to pass them, e.g. by adding the following line to your .htaccess file:

``` bash
SetEnvIf Authorization "(.*)" HTTP_AUTHORIZATION=$1
```
``` php
$ curl -H 'Authorization: Bearer wolf' 127.0.0.1/dumpserver.php |grep -i auth
  'HTTP_AUTHORIZATION' => string 'Bearer wolf'(length=11)
$
```

Alternatively you may use mod_rewrite:

``` bash
RewriteCond %{HTTP:Authorization} ^(.+)$
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
```
**FastCGI**

When Apache speaks via FastCGI with PHP, then the authorization header is available as REDIRECT_HTTP_AUTHORIZATION. There is no way to get rid of the REDIRECT_ in front; your code has to check both variants.


### References

[HTTP Authentication](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication)

[PSR-7 Basic Auth Middleware](https://github.com/tuupola/slim-basic-auth/tree/2.x)

[HTTP authentication with PHP](http://php.net/manual/en/features.http-auth.php)

[How To Check If A String is Valid Base64 in PHP](https://stackoverflow.com/a/10797086/5361267)

[Authentication and Authorization](https://httpd.apache.org/docs/2.4/howto/auth.html)

[JIRA REST API Example - Basic Authentication](https://developer.atlassian.com/jiradev/jira-apis/jira-rest-apis/jira-rest-api-tutorials/jira-rest-api-example-basic-authentication)

===

@since version 1.3.4