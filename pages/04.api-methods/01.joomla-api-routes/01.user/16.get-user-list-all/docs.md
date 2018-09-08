---
title: 'GET user/list/all'
published: false
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
  "0": {
    "username": "steve.tsiopanos",
    "email": "stevetsi@annatech.com",
    "sendEmail": "1",
    "registerDate": "2016-03-25 02:50:07",
    "lastvisitDate": "2017-03-19 19:12:31",
    "activation": "0",
    "params": "",
    "groups": {
      "8": "8"
    },
    "lastResetTime": "0000-00-00 00:00:00",
    "resetCount": "0",
    "requireReset": "0"
  },
  "error": false,
  "status": 200
}
```

#### Response Headers
```
{
  "server": "Apache/2.4.6",
  "transfer-encoding": "Identity",
  "content-type": "application/json",
  "date": "Sun, 19 Mar 2017 19:12:42 GMT",
  "connection": "Keep-Alive",
  "access-control-allow-methods": "PUT, GET, POST, DELETE, OPTIONS",
  "access-control-allow-origin": "*",
  "keep-alive": "timeout=5, max=87",
  "access-control-allow-headers": "X-Requested-With, Origin, Content-Type, token, dlid, nonce"
}
```