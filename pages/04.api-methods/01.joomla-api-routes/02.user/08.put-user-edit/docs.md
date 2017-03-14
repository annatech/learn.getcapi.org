---
title: 'PUT user/edit/:id'
taxonomy:
    category:
        - docs
---

Update existing Joomla user.

### Resource URL
https://yourdomain.com/api/v1/user/edit/:id

>>> UNDER CONSTRUCTION - PAGE INCOMPLETE

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | YES |
| Rate limited    | YES |

### Parameters

| Name | Details |
|  :-----          |  :-----          |
| ***name***   | <ul><li>REQUIRED</li><li>string</li></ul> |
| ***username*** | <ul><li>REQUIRED</li><li>string</li></ul> |
| ***password***   | <ul><li>REQUIRED</li><li>string</li></ul> |
| ***email***   | <ul><li>REQUIRED</li><li>email</li></ul> |
| ***groups***   | <ul><li>OPTIONAL</li><li>comma separated integer string*</li></ul> |

If the groups list is missing, null or out of bounds, it will default to group ids array(1,2).

### Example Request

POST
https://yourdomain.com/api/v1/user/edit
?name=First Last
&username=firstlast
&password=randompassword

### Example Result

#### JSON Response

```json
{
  "id": 344,
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Wed, 23 Mar 2016 03:30:05 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Access-Control-Allow-Origin: *
Joomla-Sessionid: 34343434343434343434343434
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json
```