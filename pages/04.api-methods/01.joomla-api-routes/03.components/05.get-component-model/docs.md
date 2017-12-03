---
title: 'GET component/model'
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

>>> Requires basic logged-in access. Access to get_class_methods also requires core.edit permissions for component.

### Resource URL
https://yourdomain.com/api/v1/component/model

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes - Registered users. "core.edit" required on given component for get_class_methods|
| Rate limited    | YES (token only)|

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **option** | <ul><li>required</li><li>string</li></ul> |
|  **type** | <ul><li>required</li><li>string</li></ul> |
|  **prefix** | <ul><li>required</li><li>string</li></ul> |
|  **context** | <ul><li>optional</li><li>string</li><li>administrator(default),site</ul> |
|  **get_class_methods** | <ul><li>optional</li><li>string</li><li>0,1</li></ul> |
|  **properties** | <ul><li>optional</li><li>string</li><li>0,1</li></ul> |

### Example Request

GET
https://yourdomain.com/api/v1/component/model?option=Content&type=Articles&prefix=ContentModel&context=administrator&get_class_methods=1&properties=1

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
                "getAuthors": [],
                "getItems": [],
                "getActiveFilters": [],
                "getPagination": [],
                "getTotal": [],
                "getStart": [],
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
        "properties": {
            "context": "com_content.articles",
            "query": [],
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
                        "access",
                        "author_id",
                        "language",
                        "tag",
                        "level",
                        "form_submited"
                    ]
                },
                "filter_featured.xml": {
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
Date: Tue, 2 Dec 2017 16:42:01 GMT
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