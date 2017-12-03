---
title: 'GET tag/name/:ids'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: false
child_type: default
routable: true
cache_enable: true
visible: true
---

Return tag name(s) by id.

### Resource URL
https://yourdomain.com/api/v1/tag/name/:ids

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **ids** | <ul><li>required</li><li>string</li><li></li>Comma-separate list of Tag id(s)</ul> |



### Example Request

GET
https://yourdomain.com/api/v1/tag/name/2,5,6

### Example Result

#### JSON Response

```json
{
  "0": "Sample Sub-tag 1",
  "1": "Sample Sub-tag 2",
  "2": "Sample Tag A",
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Sun, 03 Dec 2017 17:31:42 GMT
Server: Apache/2.4.6
X-Powered-By: PHP/7.0.25
Joomla-Sessionid: nb8oa730zt8kvgks7b9iqcl7va
Set-Cookie: n01caba7fjeibng0bda9610d1fdd9da85=rb8oi7304jd9gh3seg9iqcl7v1; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/; HttpOnly
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce, Authorization
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json
```