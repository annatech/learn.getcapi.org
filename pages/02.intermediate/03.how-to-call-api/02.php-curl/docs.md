---
title: 'PHP cURL'
published: true
taxonomy:
    category:
        - docs
---

### Overview

If you are interfacing with a REST API via PHP, cURL is a convenient and easy way send and receive CRUD (Create, Read, Update, Delete) requests. In order for this to work properly, you need to ensure certain parameters are configured properly, including:

* Content Type
* Customer Headers
* Request Methods
* Request Data (applies to POST, PUT, DELETE methods)

The following is a basic example of 

``` php
$ch = curl_init('https://www.annatech.com/api/v1/user');                                                                      
curl_setopt($ch, CURLOPT_CUSTOMREQUEST, "GET");                                   
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);                                                                      
curl_setopt($ch, CURLOPT_HTTPHEADER, array(                                                                          
    'Content-Type: application/json',
    'token: EN3RHT2HFH3NSKGH8F9382NSKDFN2AG9GH0',
    'Content-Length: ' . strlen($data_string))                                                                       
);                                                                                                                   
                                                                                                                     
$result = curl_exec($ch);
```

### Additional Resources

**Client URL Library**
[http://php.net/manual/en/book.curl.php](http://php.net/manual/en/book.curl.php)

**Basic cURL Examples**
[http://php.net/manual/en/curl.examples-basic.php](http://php.net/manual/en/curl.examples-basic.php)

**Using cURL for Remote Requests**
[http://www.sitepoint.com/using-curl-for-remote-requests/](http://www.sitepoint.com/using-curl-for-remote-requests/)

**Curl and PHP - how can I pass a json through curl by PUT,POST,GET**
[http://stackoverflow.com/questions/21271140/curl-and-php-how-can-i-pass-a-json-through-curl-by-put-post-get](http://stackoverflow.com/questions/21271140/curl-and-php-how-can-i-pass-a-json-through-curl-by-put-post-get)

**Example GET, POST, PUT and DELETE requests**
[http://www.copernica.com/en/support/rest/example-get-post-put-and-delete-requests](http://www.copernica.com/en/support/rest/example-get-post-put-and-delete-requests)
