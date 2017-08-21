---
title: 'DELETE content/delete/:id'
published: true
taxonomy:
    category:
        - docs
process:
    markdown: true
child_type: default
routable: true
cache_enable: true
visible: true
---

Delete Joomla content by ID

### Resource URL
https://yourdomain.com/api/v1/content/delete/:id

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | YES |

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
{
  "content": true,
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Wed, 23 Dec 2015 01:21:43 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 4l599999edg5fo0hvr99999l67
X-Ratelimit-Remaining: 119
X-Ratelimit-Limit: 120
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json

```