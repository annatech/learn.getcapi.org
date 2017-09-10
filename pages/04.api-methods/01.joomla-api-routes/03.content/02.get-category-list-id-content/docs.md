---
title: 'GET category/list/:id/content'
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

List Joomla Content in Category by Category ID

### Resource URL
https://yourdomain.com/api/v1/category/list/:id/content

### Resource Information

***IMPORTANT ***
- This method currently requires core.admin ("Super User") permissions to return a response. This will be fixed in an upcoming release.

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
https://yourdomain.com/api/v1/category/list/42/content

### Example Result

#### JSON Response

```json
{
  "0": {
    "id": "30",
    "asset_id": "561",
    "title": "Joomla REST Services Documentation",
    "alias": "joomla-rest-services-docs",
    "introtext": "<p>Documentation coming soon!<\/p>\r\n<table border=\"0\">\r\n<tbody>\r\n<tr>\r\n<td>Sample Content A<\/td>\r\n<td>Sample Content B<\/td>\r\n<td>Sample Content C<\/td>\r\n<td>Sample Content D<\/td>\r\n<\/tr>\r\n<tr>\r\n<td>row 1<\/td>\r\n<td>&nbsp;<\/td>\r\n<td>&nbsp;<\/td>\r\n<td>&nbsp;<\/td>\r\n<\/tr>\r\n<tr>\r\n<td>row 2<\/td>\r\n<td>&nbsp;<\/td>\r\n<td>&nbsp;<\/td>\r\n<td>&nbsp;<\/td>\r\n<\/tr>\r\n<tr>\r\n<td>row 3<\/td>\r\n<td>&nbsp;<\/td>\r\n<td>&nbsp;<\/td>\r\n<td>&nbsp;<\/td>\r\n<\/tr>\r\n<\/tbody>\r\n<\/table>",
    "fulltext": "",
    "state": "1",
    "catid": "42",
    "created": "2015-08-15 22:25:04",
    "created_by": "123",
    "created_by_alias": "",
    "modified": "2015-08-19 19:07:52",
    "modified_by": "43",
    "checked_out": "0",
    "checked_out_time": "0000-00-00 00:00:00",
    "publish_up": "2015-08-15 22:25:04",
    "publish_down": "0000-00-00 00:00:00",
    "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
    "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
    "attribs": "{\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_layout\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
    "version": "9",
    "ordering": "0",
    "metakey": "",
    "metadesc": "",
    "access": "34",
    "hits": "2",
    "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
    "featured": "0",
    "language": "*",
    "xreference": ""
  },
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Wed, 23 Dec 2015 01:32:10 GMT
Server: Apache
X-Powered-By: PHP/5.4.39
Access-Control-Allow-Origin: *
Joomla-Sessionid: 9f8699999999999e35c14e999990f4838
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=50
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json
```