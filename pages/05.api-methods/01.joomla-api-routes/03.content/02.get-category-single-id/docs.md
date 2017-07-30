---
title: 'GET category/single/:id'
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

Returns Joomla Content Catetory by ID.

### Resource URL
https://yourdomain.com/api/v1/category/single/:id

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

GET
https://yourdomain.com/api/v1/category/single/59

### Example Result

#### JSON Response

```json
{
  "category": {
    "id": "59",
    "asset_id": "201",
    "parent_id": "root",
    "lft": "15",
    "rgt": "16",
    "level": "1",
    "extension": "com_content",
    "title": "Sample Category",
    "alias": "sample-category",
    "description": "<p>Sample category description text.<\/p>",
    "published": "1",
    "checked_out": "0",
    "checked_out_time": "0000-00-00 00:00:00",
    "access": "1",
    "params": "{\"category_layout\":\"\",\"image\":\"\",\"image_alt\":\"\"}",
    "metadesc": "",
    "metakey": "",
    "metadata": "{\"author\":\"\",\"robots\":\"\"}",
    "created_user_id": "326",
    "created_time": "2015-12-22 23:29:42",
    "modified_user_id": "0",
    "modified_time": "2015-12-22 23:29:42",
    "hits": "0",
    "language": "*",
    "numitems": null,
    "childrennumitems": null,
    "slug": "59:sample-category",
    "assets": null,
    "note": "",
    "path": "sample-category",
    "version": "1"
  },
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Tue, 22 Dec 2015 23:29:55 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 4l5q1so5edg5fo0hvr4938ql67
X-Ratelimit-Remaining: 119
X-Ratelimit-Limit: 120
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json

```