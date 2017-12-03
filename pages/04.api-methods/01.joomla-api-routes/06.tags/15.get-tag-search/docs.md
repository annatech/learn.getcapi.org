---
title: 'GET tag/search'
published: false
taxonomy:
    category:
        - docs
---

Return list of searched tags.

>>> Access depends on core.edit permissions at component or item level or item access level matching the requestor's account.

### Resource URL
https://yourdomain.com/api/v1/tag/search

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Optional |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **tag** | <ul><li>Tag search value</li><li>required</li><li>string</li></ul> |
|  **title** | <ul><li>Tag title</li><li>optional</li><li>string</li></ul> |
|  **flanguage** | <ul><li>Tag language</li><li>optional</li><li>string</li></ul> |
|  **published** | <ul><li>Tag published state</li><li>optional</li><li>integer</li><li>0,1,-2</li></ul> |
|  **parent_id** | <ul><li>Tag parent ID</li><li>optional</li><li>integer</li></ul> |

### Example Request A

GET
https://yourdomain.com/api/v1//api/v1/tag/search?tag=sample&title=&flanguage=&published=1parent_id=

### Example Result A

#### JSON Response

```json
{
  "0": {
    "value": "2",
    "text": "Sample Tag A",
    "path": "sample-tag-a"
  },
  "1": {
    "value": "5",
    "text": "Sample Tag A\/Sample Sub-tag 1",
    "path": "sample-tag-a\/sample-sub-tag-1"
  },
  "2": {
    "value": "3",
    "text": "Sample Tag B",
    "path": "sample-tag-b"
  },
  "3": {
    "value": "6",
    "text": "Sample Tag B\/Sample Sub-tag 2",
    "path": "sample-tag-b\/sample-sub-tag-2"
  },
  "4": {
    "value": "4",
    "text": "Sample Tag C",
    "path": "sample-tag-c"
  },
  "5": {
    "value": "7",
    "text": "Sample Tag C\/Sample Sub-tag 3",
    "path": "sample-tag-c\/sample-sub-tag-3"
  },
  "error": false,
  "status": 200
}
```

### Example Request B

GET
https://yourdomain.com/api/v1//api/v1/tag/search?tag=&title=Sample%20Tag%20B&flanguage=&published=1parent_id=

### Example Result B

#### JSON Response

```json
{
  "0": {
    "value": "3",
    "text": "Sample Tag B",
    "path": "sample-tag-b"
  },
  "error": false,
  "status": 200
}
```

### Example Request C

GET
https://yourdomain.com/api/v1//api/v1/tag/search?tag=&title=&flanguage=&published=1parent_id=4

### Example Result C

#### JSON Response

```json
{
  "0": {
    "value": "4",
    "text": "Sample Tag C",
    "path": "sample-tag-c"
  },
  "1": {
    "value": "7",
    "text": "Sample Tag C\/Sample Sub-tag 3",
    "path": "sample-tag-c\/sample-sub-tag-3"
  },
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Tue, 21 Nov 2017 16:42:01 GMT
Server: Apache/2.4.6
X-Powered-By: PHP/7.0.25
Joomla-Sessionid: ccdvob3bhi3ludtfslv1smbgb7
Set-Cookie: 001ca6a7bc5c250bda9610d1f7d9da85=acavobdbhidlunt8klv1fmbsic; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/; HttpOnly
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce, Authorization
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json

```