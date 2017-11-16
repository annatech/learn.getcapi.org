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
| Requires authentication | Yes - Super Admin |
| Rate limited    | YES |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **id** | <ul><li>required</li><li>integer</li></ul> |

### Example Request

GET
https://yourdomain.com/api/v1/component/model/data?option=Content&type=Articles&prefix=ContentModel&filter_param=filter.language&context=site&get_class_methods=0&activeFilters=0&properties=0

### Example Result

#### JSON Response

```json
{
  "content": {
    "items": [
      {
        "id": "1",
        "title": "API Sandbox",
        "alias": "api-sandbox",
        "introtext": "",
        "fulltext": "",
        "checked_out": "0",
        "checked_out_time": "0000-00-00 00:00:00",
        "catid": "2",
        "created": "2016-03-29 01:55:43",
        "created_by": "184",
        "created_by_alias": "",
        "state": "1",
        "modified": "2016-04-10 19:32:15",
        "modified_by": "184",
        "modified_by_name": "Super User",
        "publish_up": "2016-03-29 01:55:43",
        "publish_down": "0000-00-00 00:00:00",
        "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
        "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
        "attribs": "{\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_layout\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
        "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
        "metakey": "",
        "metadesc": "",
        "access": "1",
        "hits": "300",
        "xreference": "",
        "featured": "0",
        "language": "*",
        "readmore": "0",
        "ordering": "0",
        "category_title": "Uncategorised",
        "category_route": "uncategorised",
        "category_access": "1",
        "category_alias": "uncategorised",
        "published": "1",
        "parents_published": "1",
        "lft": "1",
        "author": "Super User",
        "author_email": "stevetsi@annatech.com",
        "parent_title": "ROOT",
        "parent_id": "1",
        "parent_route": "",
        "parent_alias": "root",
        "rating": "0",
        "rating_count": "0",
        "alternative_readmore": null,
        "layout": null,
        "params": {
          "access-edit": true,
          "access-view": true
        },
        "displayDate": "2016-03-29 01:55:43",
        "tags": {
          "typeAlias": null,
          "itemTags": []
        }
      },
      {
        "id": "2",
        "title": "Sample Article #1",
        "alias": "sample-article-1",
        "introtext": "Updated sample content",
        "fulltext": "",
        "checked_out": "0",
        "checked_out_time": "0000-00-00 00:00:00",
        "catid": "9",
        "created": "2016-11-02 14:57:18",
        "created_by": "184",
        "created_by_alias": "",
        "state": "1",
        "modified": "2016-11-02 15:51:56",
        "modified_by": "184",
        "modified_by_name": "Super User",
        "publish_up": "2016-11-02 14:57:18",
        "publish_down": "0000-00-00 00:00:00",
        "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
        "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
        "attribs": "{\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"info_block_show_title\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_layout\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
        "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
        "metakey": "",
        "metadesc": "",
        "access": "1",
        "hits": "141",
        "xreference": "",
        "featured": "0",
        "language": "*",
        "readmore": "0",
        "ordering": "0",
        "category_title": "Sandbox",
        "category_route": "sandbox",
        "category_access": "1",
        "category_alias": "sandbox",
        "published": "1",
        "parents_published": "1",
        "lft": "13",
        "author": "Super User",
        "author_email": "stevetsi@annatech.com",
        "parent_title": "ROOT",
        "parent_id": "1",
        "parent_route": "",
        "parent_alias": "root",
        "rating": "0",
        "rating_count": "0",
        "alternative_readmore": null,
        "layout": null,
        "params": {
          "access-edit": true,
          "access-view": true
        },
        "displayDate": "2016-11-02 14:57:18",
        "tags": {
          "typeAlias": null,
          "itemTags": []
        }
      }
    ]
  },
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Wed, 23 Dec 2015 01:24:55 GMT
Server: Apache
X-Powered-By: PHP/5.4.39
Access-Control-Allow-Origin: *
Joomla-Sessionid: 9f862b999999ffe35c1999991999998
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=50
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json

```