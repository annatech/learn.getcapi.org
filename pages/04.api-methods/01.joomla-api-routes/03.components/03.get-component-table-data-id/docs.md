---
title: 'GET component/table/data/:id'
published: true
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

Returns component table row by ID.

>>> Access depends on core.edit permissions at component-level or matching item->access and authorised view levels of requesting user..

### Resource URL
https://yourdomain.com/api/v1/component/table/data/:id

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes - core.edit or matching View Level |
| Rate limited    | YES (token only)|

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **id** | <ul><li>path</li><li>required</li><li>numeric</li></ul> |


### Example Request

GET https://yourdomain.com/api/v1/component/table/data/2?option=Menus&type=Menu&prefix=MenusTable&get_class_methods=0

### Example Result

#### JSON Response

```json
{
  "menus": {
    "parent_id": 1,
    "level": 1,
    "lft": 1,
    "rgt": 10,
    "alias": "Banners",
    "id": 2,
    "menutype": "main",
    "title": "com_banners",
    "note": "",
    "path": "Banners",
    "link": "index.php?option=com_banners",
    "type": "component",
    "published": 1,
    "component_id": 4,
    "checked_out": "0",
    "checked_out_time": "0000-00-00 00:00:00",
    "browserNav": "0",
    "access": "0",
    "img": "class:banners",
    "template_style_id": "0",
    "params": "",
    "home": "0",
    "language": "*",
    "client_id": 1
  },
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Thu, 16 Nov 2017 12:45:00 GMT
Server: Apache/2.4.6
X-Powered-By: PHP/7.0.25
Joomla-Sessionid: 3aa0enpsfonvgnbjpuhuss5ufv
Set-Cookie: d01caba7bc5c20bda9610d1fdd9da85=3ja0enpvgonvgnbjpuhumb5uf4; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/; HttpOnly
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce, Authorization
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json

```