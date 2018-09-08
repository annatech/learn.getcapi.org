---
title: 'GET user/list/all'
published: false
taxonomy:
    category:
        - docs
---

Get a list of all user accounts.

### Resource URL
https://yourdomain.com/api/v1/user/list/all

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes, core.edit |
| Rate limited    | NO |

### Parameters

Method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/user/list/all

### Example Result

#### JSON Response

##### Guest
```json
{
  "msg": "Forbidden",
  "error": false,
  "status": 403
}
```
##### Logged In
```json
{
  "users": {
    "items": [
      {
        "id": "287",
        "name": "cAPI Demo User",
        "username": "capidemouser",
        "email": "capidemouser@getcapi.io",
        "block": "0",
        "sendEmail": "0",
        "registerDate": "2016-04-10 19:57:19",
        "lastvisitDate": "2016-05-07 20:49:07",
        "activation": "",
        "params": {
          "admin_style": "",
          "admin_language": "",
          "language": "",
          "editor": "",
          "helpsite": "",
          "timezone": ""
        },
        "lastResetTime": "0000-00-00 00:00:00",
        "resetCount": "0",
        "otpKey": "",
        "otep": "",
        "requireReset": "0",
        "group_count": "3",
        "group_names": "Registered\ncAPI Demo Group",
        "note_count": 0
      },
      {
        "id": "292",
        "name": "capidemoreg",
        "username": "capidemoreg",
        "email": "capidemoreg@annatech.com",
        "block": "0",
        "sendEmail": "0",
        "registerDate": "2018-09-08 17:42:45",
        "lastvisitDate": "2018-09-08 17:43:09",
        "activation": "",
        "params": {
          "admin_style": "",
          "admin_language": "",
          "language": "",
          "editor": "",
          "helpsite": "",
          "timezone": ""
        },
        "lastResetTime": "0000-00-00 00:00:00",
        "resetCount": "0",
        "otpKey": "",
        "otep": "",
        "requireReset": "0",
        "group_count": "2",
        "group_names": "Registered\nManager",
        "note_count": 0
      },
      {
        "id": "189",
        "name": "Sample User",
        "username": "sample.user",
        "email": "sample.user@annatech.com",
        "block": "0",
        "sendEmail": "0",
        "registerDate": "2017-02-28 14:25:55",
        "lastvisitDate": "0000-00-00 00:00:00",
        "activation": "",
        "params": {},
        "lastResetTime": "0000-00-00 00:00:00",
        "resetCount": "0",
        "otpKey": "",
        "otep": "",
        "requireReset": "0",
        "group_count": "1",
        "group_names": "Public",
        "note_count": 0
      },
      {
        "id": "284",
        "name": "Bob Clark",
        "username": "bob.clark",
        "email": "bob.clark@annatech.com",
        "block": "0",
        "sendEmail": "1",
        "registerDate": "2016-03-25 02:50:07",
        "lastvisitDate": "2018-09-08 18:50:27",
        "activation": "0",
        "params": null,
        "lastResetTime": "0000-00-00 00:00:00",
        "resetCount": "0",
        "otpKey": "",
        "otep": "",
        "requireReset": "0",
        "group_count": "1",
        "group_names": "Super Users",
        "note_count": 0
      }
    ]
  },
  "error": false,
  "status": 200
}
```

#### Response Headers
```
{
  "access-control-allow-headers": "X-Requested-With, Origin, Content-Type, token, dlid, nonce, Authorization",
  "access-control-allow-methods": "GET, PUT, POST, DELETE, OPTIONS",
  "access-control-allow-origin": "*",
  "connection": "Keep-Alive",
  "content-type": "application/json",
  "date": "Sat, 08 Sep 2018 18:50:33 GMT",
  "keep-alive": "timeout=5, max=95",
  "server": "Apache/2.4.6",
  "transfer-encoding": "Identity"
}
```