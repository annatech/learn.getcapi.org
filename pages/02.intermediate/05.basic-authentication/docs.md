---
title: 'Basic Authentication'
taxonomy:
    category:
        - docs
---

### Overview

### Troubleshooting

#### PHP Does Not See Authorization Header

( [original source](https://cweiske.de/tagebuch/php-apache-authorization.htm) )

While implementing a token endpoint you may notice that you are unable to access the value of an HTTP Authorization header - $_SERVER did not include it. 

$ curl -H 'Authorization: Bearer wolf' 127.0.0.1/dumpserver.php |grep -i auth
$

It turns out that you manually have to pass them, e.g. by adding the following line to your .htaccess file: ​

``SetEnvIf Authorization "(.*)" HTTP_AUTHORIZATION=$1

``$ curl -H 'Authorization: Bearer wolf' 127.0.0.1/dumpserver.php |grep -i auth
  'HTTP_AUTHORIZATION' => string 'Bearer wolf'(length=11)
$
Alternatively you may use mod_rewrite: ​

RewriteCond %{HTTP:Authorization} ^(.+)$
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]​
FastCGI​

When Apache speaks via FastCGI with PHP, then the authorization header is available as REDIRECT_HTTP_AUTHORIZATION. There is no way to get rid of the REDIRECT_ in front; you code has to check both variants.




### Additional References

[HTTP Authentication](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication)

[PSR-7 Basic Auth Middleware](https://github.com/tuupola/slim-basic-auth/tree/2.x)

[HTTP authentication with PHP](http://php.net/manual/en/features.http-auth.php)

[How To Check If A String is Valid Base64 in PHP](https://stackoverflow.com/a/10797086/5361267)

[Authentication and Authorization](https://httpd.apache.org/docs/2.4/howto/auth.html)

@since version 1.3.4