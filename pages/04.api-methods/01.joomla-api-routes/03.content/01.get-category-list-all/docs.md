---
title: 'GET category/list/all'
published: true
process:
    markdown: true
    twig: false
routable: true
cache_enable: true
visible: true
child_type: default
taxonomy:
    category:
        - docs
---

Return list of all Joomla Content Categories

>>> This method requires that a persistent HTTP session can be maintained between the client and server. Super Admin access is required.

### Resource URL
https://yourdomain.com/api/v1/content/list/all

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes - Super Admin |
| Rate limited    | YES |

### Parameters

Method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/content/list/all

### Example Result

#### JSON Response

```json
{
  "categories": {
    "2": {
      "id": "2",
      "asset_id": "27",
      "parent_id": "root",
      "lft": "1",
      "rgt": "2",
      "level": "1",
      "extension": "com_content",
      "title": "Uncategorised",
      "alias": "uncategorised",
      "description": "",
      "published": "1",
      "checked_out": "0",
      "checked_out_time": "0000-00-00 00:00:00",
      "access": "1",
      "params": "{\"category_layout\":\"\",\"image\":\"\"}",
      "metadesc": "",
      "metakey": "",
      "metadata": "{\"author\":\"\",\"robots\":\"\"}",
      "created_user_id": "42",
      "created_time": "2011-01-01 00:00:01",
      "modified_user_id": "0",
      "modified_time": "0000-00-00 00:00:00",
      "hits": "0",
      "language": "*",
      "numitems": null,
      "childrennumitems": null,
      "slug": "2:uncategorised",
      "assets": null,
      "note": "",
      "path": "uncategorised",
      "version": "1",
      "_rightsibling": {
        "id": "58",
        "asset_id": "199",
        "parent_id": "root",
        "lft": "13",
        "rgt": "14",
        "level": "1",
        "extension": "com_content",
        "title": "Sample Category B",
        "alias": "sample-category-b",
        "description": "",
        "published": "1",
        "checked_out": "0",
        "checked_out_time": "0000-00-00 00:00:00",
        "access": "1",
        "params": "{\"category_layout\":\"\",\"image\":\"\",\"image_alt\":\"\"}",
        "metadesc": "",
        "metakey": "",
        "metadata": "{\"author\":\"\",\"robots\":\"\"}",
        "created_user_id": "326",
        "created_time": "2015-12-20 23:02:23",
        "modified_user_id": "326",
        "modified_time": "2015-12-20 23:03:11",
        "hits": "0",
        "language": "*",
        "numitems": null,
        "childrennumitems": null,
        "slug": "58:sample-category-b",
        "assets": null,
        "note": "",
        "path": "sample-category-b",
        "version": "1",
        "_rightsibling": {
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
        }
      }
    },
    "58": {
      "id": "58",
      "asset_id": "199",
      "parent_id": "root",
      "lft": "13",
      "rgt": "14",
      "level": "1",
      "extension": "com_content",
      "title": "Sample Category B",
      "alias": "sample-category-b",
      "description": "",
      "published": "1",
      "checked_out": "0",
      "checked_out_time": "0000-00-00 00:00:00",
      "access": "1",
      "params": "{\"category_layout\":\"\",\"image\":\"\",\"image_alt\":\"\"}",
      "metadesc": "",
      "metakey": "",
      "metadata": "{\"author\":\"\",\"robots\":\"\"}",
      "created_user_id": "326",
      "created_time": "2015-12-20 23:02:23",
      "modified_user_id": "326",
      "modified_time": "2015-12-20 23:03:11",
      "hits": "0",
      "language": "*",
      "numitems": null,
      "childrennumitems": null,
      "slug": "58:sample-category-b",
      "assets": null,
      "note": "",
      "path": "sample-category-b",
      "version": "1",
      "_rightsibling": {
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
      }
    },
    "59": {
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
    }
  },
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Tue, 22 Dec 2015 23:40:02 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 999991so5edg99999vr49999967
X-Ratelimit-Remaining: 119
X-Ratelimit-Limit: 120
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json

```