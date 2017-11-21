---
title: 'GET component/model/data'
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

Returns data from component Model.

>>> Access depends on core.edit permissions at component or item level or item access level matching the requestor's account.

### Resource URL
https://yourdomain.com/api/v1/component/model/data

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes - core.edit on given component |
| Rate limited    | YES (token only)|

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **option** | <ul><li>required</li><li>string</li></ul> |
|  **type** | <ul><li>required</li><li>string</li></ul> |
|  **prefix** | <ul><li>required</li><li>string</li></ul> |

### Example Request

GET
https://yourdomain.com/api/v1/component/table/fields?&option=Content&type=Content&prefix=JTable

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
      "Collation": "utf8mb4_unicode_ci",
      "Null": "NO",
      "Key": "",
      "Default": "",
      "Extra": "",
      "Privileges": "select,insert,update,references",
      "Comment": ""
    },
    "alias": {
      "Field": "alias",
      "Type": "varchar(400)",
      "Collation": "utf8mb4_bin",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
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
      "Collation": "utf8mb4_unicode_ci",
      "Null": "NO",
      "Key": "MUL",
      "Default": "",
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
Date: Tue, 21 Nov 2017 16:31:57 GMT
Server: Apache/2.4.6
X-Powered-By: PHP/7.0.25
Joomla-Sessionid: auvvstq3btfqbtnfo43qk5v3n4
Set-Cookie: 303caba3bc5c2a0bda3610d1fdd9da85=3uvrstqeb3fqbtcfo4rqk57gn4; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/; HttpOnly
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce, Authorization
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json
```