---
title: 'Cross Origin Resource Sharing'
taxonomy:
    category:
        - docs
---

> Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources (e.g. fonts) on a web page to be requested from another domain outside the domain from which the resource originated.

[https://en.wikipedia.org/wiki/Cross-origin_resource_sharing](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing) <span class="fa fa-external-link"></span>


jQuery AJAX is an excellent method for displaying the response object of a JSON API within an HTML page without reloading or using an iFrame.

Example:

I will first show you sample jQuery Ajax syntax followed by the html for the div container which will display the output.

<iframe width="100%" height="350" src="//jsfiddle.net/annatech/18255qtb/embedded/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

As you can see, it is possible to query a RESTful JSON API and output the contents directly on a web page (all client-side, in browser).

To make the request to the API server possible, two important steps are taken:

1.
/api/v1/.htaccess

```
Header add Access-Control-Allow-Headers "X-Requested-With, Origin, Content-Type, token, dlid, nonce"
Header add Access-Control-Allow-Methods "PUT, GET, POST, DELETE, OPTIONS"
```

2.
/api/v1/index.php

``` php
if(isset($_SERVER['HTTP_REFERER'])) {
    header('Access-Control-Allow-Origin: ' . parse_url($_SERVER['HTTP_REFERER'])['scheme'] . '://' . parse_url($_SERVER['HTTP_REFERER'])['host']);
}
// respond to preflights
if ($_SERVER['REQUEST_METHOD'] === 'OPTIONS') {
    // return only the headers and not the content
    // only allow CORS if we're doing a GET - i.e. no saving for now.
    if (isset($_SERVER['HTTP_ACCESS_CONTROL_REQUEST_METHOD']) && $_SERVER['HTTP_ACCESS_CONTROL_REQUEST_METHOD'] === 'GET') {
        $app->response->header('Access-Control-Allow-Origin', '*');
        $app->response->header('Access-Control-Allow-Headers', 'X-Requested-With');
    }
    exit;
}
```

>>> Soon, cAPI will include functionality in the Services Control Panel to define which domains are allowed to make CORS requests.

```