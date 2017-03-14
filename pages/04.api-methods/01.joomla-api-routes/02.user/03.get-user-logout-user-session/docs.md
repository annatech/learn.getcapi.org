---
title: 'GET user/logout/:user/:session'
taxonomy:
    category:
        - docs
---

User logout action via Joomla authentication plugins with username and session ID. Note that since the session ID and username are passed into the URL, be aware that they can be stored in server logs. API traffic must traverse a secure (HTTPS) connection.

### Resource URL
https://yourdomain.com/api/v1/user/logout/:user/:session

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | YES |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **username** | <ul><li>required</li><li>alpha-numeric</li></ul> |
|  **session** | <ul><li>required</li><li>alpha-numeric, lowercase</li></ul> |


### Example Request

GET
https://yourdomain.com/api/v1/user/logout/dynus.borvalds/1a269ab5e9c102c970118e9049f05020

### Example Result

#### JSON Response

```json
{
  "msg": "Logout successful",
  "jresponse": true,
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Sat, 24 Oct 2015 19:47:44 GMT
Server: Apache
X-Powered-By: PHP/5.4.39
Access-Control-Allow-Origin: *
Set-Cookie: a2c071e00a02bb4eb0c99fdc0e673999=deleted; expires=Thu, 01-Jan-1970 00:00:01 GMT; path=/
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=50
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json
```