---
title: 'GET tag/fields'
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

List all Joomla Tag Fields

### Resource URL
https://yourdomain.com/api/v1/tag/fields

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | NO |

### Parameters

This method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/tag/fields

### Example Result

#### JSON Response

```json
{
  "fields": {
    "id": {
      "Field": "id",
      "Type": "int(10) unsigned",
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
    "title": {
      "Field": "title",
      "Type": "varchar(255)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "alias": {
      "Field": "alias",
      "Type": "varchar(255)",
      "Collation": "utf8_bin",
      "Null": "NO",
      "Key": "",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "introtext": {
      "Field": "introtext",
      "Type": "mediumtext",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "fulltext": {
      "Field": "fulltext",
      "Type": "mediumtext",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "state": {
      "Field": "state",
      "Type": "tinyint(3)",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "catid": {
      "Field": "catid",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "created": {
      "Field": "created",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "created_by": {
      "Field": "created_by",
      "Type": "int(10) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "created_by_alias": {
      "Field": "created_by_alias",
      "Type": "varchar(255)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "modified": {
      "Field": "modified",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "modified_by": {
      "Field": "modified_by",
      "Type": "int(10) unsigned",
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
      "Type": "int(10) unsigned",
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
    "publish_up": {
      "Field": "publish_up",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "publish_down": {
      "Field": "publish_down",
      "Type": "datetime",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0000-00-00 00:00:00",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "images": {
      "Field": "images",
      "Type": "text",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "urls": {
      "Field": "urls",
      "Type": "text",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "attribs": {
      "Field": "attribs",
      "Type": "varchar(5120)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
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
    },
    "ordering": {
      "Field": "ordering",
      "Type": "int(11)",
      "Collation": null,
      "Null": "NO",
      "Key": "",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "metakey": {
      "Field": "metakey",
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
      "Type": "text",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
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
    "metadata": {
      "Field": "metadata",
      "Type": "text",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "featured": {
      "Field": "featured",
      "Type": "tinyint(3) unsigned",
      "Collation": null,
      "Null": "NO",
      "Key": "MUL",
      "Default": "0",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": "Set if article is featured."
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
      "Comment": "The language code for the article."
    },
    "xreference": {
      "Field": "xreference",
      "Type": "varchar(50)",
      "Collation": "utf8_general_ci",
      "Null": "NO",
      "Key": "MUL",
      "Default": null,
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": "A reference to enable linkages to external data sets."
    }
  },
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Wed, 23 Dec 2015 01:35:36 GMT
Server: Apache
X-Powered-By: PHP/5.4.39
Access-Control-Allow-Origin: *
Joomla-Sessionid: 9f899999539999e35c14e999990f4839
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=50
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json

```