---
title: 'GET user/login/:username/:password'
taxonomy:
    category:
        - docs
---

User login authentication via Joomla authentication plugins with username and password. Note that since credentials are passed into the URL, be aware that they can be stored in server logs. API traffic must traverse a secure (HTTPS) connection.

### Resource URL
https://yourdomain.com/api/v1/login/:username/:password

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | NO |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **username** | <ul><li>required</li><li>alpha-numeric</li></ul> |
|  **password** | <ul><li>required</li><li>Should match expected Joomla password format. This may depend on the type of plugin used, particularly if you have enabled additional authentication plugins.</li></ul> |



### Example Request

GET
https://yourdomain.com/api/v1/user/login/dynus.borvalds/3jf9LfjNdiw

### Example Result

#### JSON Response

```json
{
  "msg": "Authenticated",
  "jresponse": true,
  "session": "1a36eab5e2b102a979918ee049f15e27",
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Sat, 24 Oct 2015 19:16:03 GMT
Server: Apache
X-Powered-By: PHP/5.4.39
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=50
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json
```