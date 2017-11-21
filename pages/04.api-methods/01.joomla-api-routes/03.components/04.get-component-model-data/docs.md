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
|  **filter_param** | <ul><li>optional</li><li>string</li></ul> |
|  **filter_value** | <ul><li>optional</li><li>string</li></ul> |
|  **get_class_methods** | <ul><li>optional</li><li>string</li><li>0,1</li></ul> |
|  **properties** | <ul><li>optional</li><li>string</li><li>0,1</li></ul> |
|  **activeFilters** | <ul><li>optional</li><li>string</li><li>0,1</li></ul> |

### Example Request

GET
https://yourdomain.com/api/v1/component/model/data?option=Content&type=Articles&prefix=ContentModel&get_class_methods=1&filter_param=filter.language&filter_value=en-GB&context=site&get_class_methods=1&properties=1&activeFilters=1

### Example Result

#### JSON Response

```json
{
  "content": {
    "class_name": {
      "ContentModelArticles": {
        "__construct": [
          {
            "name": "config"
          }
        ],
        "getItems": [],
        "getStart": [],
        "getActiveFilters": [],
        "getPagination": [],
        "getTotal": [],
        "getFilterForm": [
          {
            "name": "data"
          },
          {
            "name": "loadData"
          }
        ],
        "getUserStateFromRequest": [
          {
            "name": "key"
          },
          {
            "name": "request"
          },
          {
            "name": "default"
          },
          {
            "name": "type"
          },
          {
            "name": "resetPage"
          }
        ],
        "addIncludePath": [
          {
            "name": "path"
          },
          {
            "name": "prefix"
          }
        ],
        "addTablePath": [
          {
            "name": "path"
          }
        ],
        "getInstance": [
          {
            "name": "type"
          },
          {
            "name": "prefix"
          },
          {
            "name": "config"
          }
        ],
        "getDbo": [],
        "getName": [],
        "getState": [
          {
            "name": "property"
          },
          {
            "name": "default"
          }
        ],
        "getTable": [
          {
            "name": "name"
          },
          {
            "name": "prefix"
          },
          {
            "name": "options"
          }
        ],
        "loadHistory": [
          {
            "name": "version_id"
          },
          {
            "name": "table"
          }
        ],
        "setDbo": [
          {
            "name": "db"
          }
        ],
        "setState": [
          {
            "name": "property"
          },
          {
            "name": "value"
          }
        ],
        "__toString": [],
        "def": [
          {
            "name": "property"
          },
          {
            "name": "default"
          }
        ],
        "get": [
          {
            "name": "property"
          },
          {
            "name": "default"
          }
        ],
        "getProperties": [
          {
            "name": "public"
          }
        ],
        "getError": [
          {
            "name": "i"
          },
          {
            "name": "toString"
          }
        ],
        "getErrors": [],
        "set": [
          {
            "name": "property"
          },
          {
            "name": "value"
          }
        ],
        "setProperties": [
          {
            "name": "properties"
          }
        ],
        "setError": [
          {
            "name": "error"
          }
        ]
      }
    },
    "items": [
      {
        "id": "3",
        "title": "Sample Article 3",
        "alias": "sample-article-3",
        "introtext": "<p>Sample Article 3<\/p>",
        "fulltext": "",
        "checked_out": "0",
        "checked_out_time": "0000-00-00 00:00:00",
        "catid": "2",
        "created": "2017-11-08 21:37:27",
        "created_by": "890",
        "created_by_alias": "",
        "state": "1",
        "modified": "2017-11-09 23:44:44",
        "modified_by": "890",
        "modified_by_name": "Super User",
        "publish_up": "2017-11-08 21:37:27",
        "publish_down": "0000-00-00 00:00:00",
        "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
        "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
        "attribs": "{\"article_layout\":\"\",\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"info_block_show_title\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_associations\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_page_title\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
        "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
        "metakey": "",
        "metadesc": "",
        "access": "3",
        "hits": "0",
        "xreference": "",
        "featured": "0",
        "language": "en-GB",
        "readmore": "0",
        "category_title": "Uncategorised",
        "category_route": "uncategorised",
        "category_access": "1",
        "category_alias": "uncategorised",
        "published": "1",
        "parents_published": "1",
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
        "displayDate": "2017-11-08 21:37:27"
      },
      {
        "id": "2",
        "title": "Sample Article 2",
        "alias": "sample-article-2",
        "introtext": "<p>Sample Article 2<\/p>",
        "fulltext": "",
        "checked_out": "0",
        "checked_out_time": "0000-00-00 00:00:00",
        "catid": "2",
        "created": "2017-11-08 21:37:10",
        "created_by": "890",
        "created_by_alias": "",
        "state": "1",
        "modified": "2017-11-08 21:37:10",
        "modified_by": "0",
        "modified_by_name": null,
        "publish_up": "2017-11-08 21:37:10",
        "publish_down": "0000-00-00 00:00:00",
        "images": "{\"image_intro\":\"\",\"float_intro\":\"\",\"image_intro_alt\":\"\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
        "urls": "{\"urla\":false,\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
        "attribs": "{\"article_layout\":\"\",\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"info_block_show_title\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_associations\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_page_title\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
        "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
        "metakey": "",
        "metadesc": "",
        "access": "2",
        "hits": "0",
        "xreference": "",
        "featured": "0",
        "language": "*",
        "readmore": "0",
        "category_title": "Uncategorised",
        "category_route": "uncategorised",
        "category_access": "1",
        "category_alias": "uncategorised",
        "published": "1",
        "parents_published": "1",
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
        "displayDate": "2017-11-08 21:37:10"
      },
      {
        "id": "1",
        "title": "Sample Article",
        "alias": "sample-article",
        "introtext": "<p>Sample Article<\/p>",
        "fulltext": "",
        "checked_out": "0",
        "checked_out_time": "0000-00-00 00:00:00",
        "catid": "2",
        "created": "2017-04-24 20:13:49",
        "created_by": "891",
        "created_by_alias": "",
        "state": "1",
        "modified": "2017-11-08 21:37:53",
        "modified_by": "890",
        "modified_by_name": "Super User",
        "publish_up": "2017-04-24 20:13:49",
        "publish_down": "0000-00-00 00:00:00",
        "images": "{\"image_intro\":\"images\\\/joomla_black.png\",\"float_intro\":\"\",\"image_intro_alt\":\"Sample Alt Text\",\"image_intro_caption\":\"\",\"image_fulltext\":\"\",\"float_fulltext\":\"\",\"image_fulltext_alt\":\"\",\"image_fulltext_caption\":\"\"}",
        "urls": "{\"urla\":\"https:\\\/\\\/www.google.com\",\"urlatext\":\"\",\"targeta\":\"\",\"urlb\":false,\"urlbtext\":\"\",\"targetb\":\"\",\"urlc\":false,\"urlctext\":\"\",\"targetc\":\"\"}",
        "attribs": "{\"article_layout\":\"\",\"show_title\":\"\",\"link_titles\":\"\",\"show_tags\":\"\",\"show_intro\":\"\",\"info_block_position\":\"\",\"info_block_show_title\":\"\",\"show_category\":\"\",\"link_category\":\"\",\"show_parent_category\":\"\",\"link_parent_category\":\"\",\"show_associations\":\"\",\"show_author\":\"\",\"link_author\":\"\",\"show_create_date\":\"\",\"show_modify_date\":\"\",\"show_publish_date\":\"\",\"show_item_navigation\":\"\",\"show_icons\":\"\",\"show_print_icon\":\"\",\"show_email_icon\":\"\",\"show_vote\":\"\",\"show_hits\":\"\",\"show_noauth\":\"\",\"urls_position\":\"\",\"alternative_readmore\":\"\",\"article_page_title\":\"\",\"show_publishing_options\":\"\",\"show_article_options\":\"\",\"show_urls_images_backend\":\"\",\"show_urls_images_frontend\":\"\"}",
        "metadata": "{\"robots\":\"\",\"author\":\"\",\"rights\":\"\",\"xreference\":\"\"}",
        "metakey": "",
        "metadesc": "",
        "access": "1",
        "hits": "4",
        "xreference": "",
        "featured": "1",
        "language": "*",
        "readmore": "0",
        "category_title": "Uncategorised",
        "category_route": "uncategorised",
        "category_access": "1",
        "category_alias": "uncategorised",
        "published": "1",
        "parents_published": "1",
        "author": "Registered User",
        "author_email": "noemail@annatech.com",
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
        "displayDate": "2017-04-24 20:13:49"
      }
    ],
    "activeFilters": {
      "language": "en-GB"
    },
    "properties": {
      "context": "com_content.articles",
      "query": {},
      "filterBlacklist": [],
      "listBlacklist": [
        "select"
      ],
      "name": "articles",
      "option": "com_content",
      "filter_fields": {
        "filter_articles.xml": {
          "name": [
            "search",
            "published",
            "category_id",
            "level",
            "access",
            "author_id",
            "language",
            "tag"
          ]
        }
      }
    }
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