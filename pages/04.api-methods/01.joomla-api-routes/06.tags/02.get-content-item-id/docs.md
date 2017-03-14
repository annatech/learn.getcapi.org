---
title: 'GET content/item/:id'
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

Returns Joomla content by ID.

### Resource URL
https://yourdomain.com/api/v1/content/item/:id

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **id** | <ul><li>required</li><li>numeric</li></ul> |



### Example Request

GET
https://yourdomain.com/api/v1/content/item/42

### Example Result

#### JSON Response

```json
{
  "article": {
    "id": "42",
    "asset_id": "999",
    "title": "cAPI Core Package Ajax Test Page",
    "alias": "capi-core-package-ajax-test-page",
    "introtext": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis a euismod lectus, quis porttitor eros. Sed pellentesque ex ac ante porta, et mollis elit malesuada. Quisque in felis accumsan, tempus urna eget, facilisis lorem. Suspendisse ornare nulla a erat lobortis rutrum.",
    "fulltext": "",
    "state": "1",
    "catid": "2",
    "created": "2015-09-23 01:54:56",
    "created_by": "43",
    "created_by_alias": "",
    "modified": "2015-09-23 03:39:05",
    "modified_by": "43",
    "checked_out": "0",
    "checked_out_time": "0000-00-00 00:00:00",
    "publish_up": "2015-09-23 01:54:56",
    "publish_down": "0000-00-00 00:00:00",
    "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
    "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
    "attribs": "{\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_layout\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
    "version": "11",
    "ordering": "0",
    "metakey": "",
    "metadesc": "",
    "access": "2",
    "hits": "0",
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
Date: Sun, 25 Oct 2015 16:33:13 GMT
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