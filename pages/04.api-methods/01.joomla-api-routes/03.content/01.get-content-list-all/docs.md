---
title: 'GET content/list/all'
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

Return list of all Joomla content

>>> This method requires that a persistent HTTP session can be maintained between the client and server. Super Admin access is required.

### Resource URL
https://yourdomain.com/api/v1/content/list/all

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes - Super Admin |
| Rate limited    | NO |

### Parameters

Method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/content/list/all

### Example Result

>>>>> Responses have been cleansed to protect private data.

#### JSON Response

```json
{
  "0": {
    "id": "41",
    "asset_id": "194",
    "title": "Sample Content Article W",
    "alias": "sample-content-article-w",
    "introtext": "<p>This is another sample content article.<\/p>",
    "fulltext": "",
    "state": "1",
    "catid": "2",
    "created": "2015-12-18 04:06:32",
    "created_by": "326",
    "created_by_alias": "",
    "modified": "2015-12-21 02:14:01",
    "modified_by": "326",
    "checked_out": "0",
    "checked_out_time": "0000-00-00 00:00:00",
    "publish_up": "2015-12-18 04:06:32",
    "publish_down": "0000-00-00 00:00:00",
    "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
    "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
    "attribs": "{\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_layout\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
    "version": "4",
    "ordering": "0",
    "metakey": "",
    "metadesc": "",
    "access": "6",
    "hits": "0",
    "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
    "featured": "0",
    "language": "*",
    "xreference": ""
  },
  "1": {
    "id": "42",
    "asset_id": "191",
    "title": "Sample Content 72",
    "alias": "sample-content-72",
    "introtext": "",
    "fulltext": "",
    "state": "1",
    "catid": "2",
    "created": "2015-12-18 04:09:08",
    "created_by": "326",
    "created_by_alias": "",
    "modified": "2015-12-21 02:13:56",
    "modified_by": "326",
    "checked_out": "0",
    "checked_out_time": "0000-00-00 00:00:00",
    "publish_up": "2015-12-18 04:09:26",
    "publish_down": "0000-00-00 00:00:00",
    "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
    "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
    "attribs": "{\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_layout\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
    "version": "4",
    "ordering": "0",
    "metakey": "",
    "metadesc": "",
    "access": "6",
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
Date: Tue, 22 Dec 2015 03:51:15 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 4l5q199999hvr499999938ql67
X-Ratelimit-Remaining: 119
X-Ratelimit-Limit: 120
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json
```