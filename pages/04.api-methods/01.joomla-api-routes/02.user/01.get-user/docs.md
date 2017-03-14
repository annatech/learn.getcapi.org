---
title: 'GET user'
taxonomy:
    category:
        - docs
---

Get current logged in user or display if accessing web service as guest.

>>> This method requires that a persistent HTTP sessions can be maintained between the client and server since the user returned with respect to the current browser (or other persistent) session.

### Resource URL
https://yourdomain.com/api/v1/user

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | No |
| Rate limited    | NO |

### Parameters

Method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/user

### Example Result

>>>>> Responses have been cleansed to protect private session data.

#### JSON Response

##### Guest
```json
{
  "msg": "Welcome guest",
  "error": false,
  "status": 200
}
```
##### Logged In
```json
{
  "msg": "Welcome Steve Tsiopanos",
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Sun, 25 Oct 2015 15:08:00 GMT
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