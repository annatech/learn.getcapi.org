---
title: 'DELETE content/delete/:id'
published: false
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

Delete Joomla content by ID.

### Resource URL
https://yourdomain.com/api/v1/content/delete/:id

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes, session-based - Depends on Joomla content security and user permissions levels. |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **id** | <ul><li>required</li><li>numeric</li></ul> |



### Example Request

DELETE
https://yourdomain.com/api/v1/content/delete/42

### Example Result

#### JSON Response

```json
[Description coming soon...]
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Sun, 25 Oct 2015 17:14:13 GMT
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