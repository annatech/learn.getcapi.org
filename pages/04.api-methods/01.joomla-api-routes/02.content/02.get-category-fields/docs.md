---
title: 'GET category/fields'
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

List all Joomla Content Fields

### Resource URL
https://yourdomain.com/api/v1/category/fields

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | YES |

### Parameters

This method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/category/fields

### Example Result

#### JSON Response

```json
{
  "fields": {
    "id": {
      "Field": "id",
      "Type": "int(11)",
      "Collation": null,
      "Null": "NO",
      "Key": "PRI",
      "Default": null,
      "Extra": "auto_increment",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "asset_id": {
      "Field": "asset_id",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": "FK to the #__assets table."
    },
    "parent_id": {
      "Field": "parent_id",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "lft": {
      "Field": "lft",
      "Type": "int(11)",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "rgt": {
      "Field": "rgt",
      "Type": "int(11)",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "level": {
      "Field": "level",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "path": {
      "Field": "path",
      "Type": "varchar(255)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "MUL",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "extension": {
      "Field": "extension",
      "Type": "varchar(50)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "MUL",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "title": {
      "Field": "title",
      "Type": "varchar(255)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "alias": {
      "Field": "alias",
      "Type": "varchar(255)",
      "Collation": "utf8_bin",
      "Null": "NO",
      "Key": "MUL",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "note": {
      "Field": "note",
      "Type": "varchar(255)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "description": {
      "Field": "description",
      "Type": "mediumtext",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "published": {
      "Field": "published",
      "Type": "tinyint(1)",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "checked_out": {
      "Field": "checked_out",
      "Type": "int(11) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "checked_out_time": {
      "Field": "checked_out_time",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "access": {
      "Field": "access",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "params": {
      "Field": "params",
      "Type": "text",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "metadesc": {
      "Field": "metadesc",
      "Type": "varchar(1024)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": "The meta description for the page."
    },
    "metakey": {
      "Field": "metakey",
      "Type": "varchar(1024)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": "The meta keywords for the page."
    },
    "metadata": {
      "Field": "metadata",
      "Type": "varchar(2048)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": "JSON encoded metadata properties."
    },
    "created_user_id": {
      "Field": "created_user_id",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "created_time": {
      "Field": "created_time",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "modified_user_id": {
      "Field": "modified_user_id",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "modified_time": {
      "Field": "modified_time",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "hits": {
      "Field": "hits",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "language": {
      "Field": "language",
      "Type": "char(7)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "MUL",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "version": {
      "Field": "version",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "1",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    }
  },
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Wed, 23 Dec 2015 01:29:41 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 999991so5ed999o0hvr4999ql67
X-Ratelimit-Remaining: 119
X-Ratelimit-Limit: 120
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json
```