---
title: 'GET token/:token'
published: true
taxonomy:
    category:
        - docs
---

Returns Joomla Session ID on successful authentication with access token.

>>>> Always secure access to your API server via HTTPS.

### Resource URL
https://yourdomain.com/api/v1/token/:token

### Resource Information

| Option | Description |
| ------ | ----------- |
| Request format	|	Request Header Parameter	|
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | NO |

### Parameters

|  name  |  Details  |  
|  :-----          |  :-----          |
|  **token** | <ul><li>required</li><li>numeric</li></ul> |


### Example Request

POST
https://yourdomain.com/api/token/xCzlAPpX8zAIPbk78XNkoF6O0Q3h2J3958X:21

### Example Result

#### JSON Response

``` json
{
  "msg": "Authenticated",
  "jresponse": "true",
  "error": false,
  "status": 200
}
```

#### Response Headers

```
HTTP/1.1 200 OK
Date: Sun, 25 Oct 2015 19:55:05 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 99993p1kqtfucdjq9qs9oq99p9
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json
```

