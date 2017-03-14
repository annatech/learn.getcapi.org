---
title: 'GET slim/swagger'
---

Returns Swagger definition JSON

### Resource URL
https://yourdomain.com/api/v1/slim/swagger

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | NO |
| Rate limited    | NO |

### Parameters

Method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/slim/swagger

### Example Result

#### JSON Response

```json
{
    "swagger": "2.0",
    "info": {
        "title": "cAPI Core Package",
        "description": "Code named \"Constant API\", cAPI is the fantastic result of an effort to mesh the Slim micro-framework with the Joomla Framework / CMS. Once that goal was accomplished, it soon became obvious that just built a Joomla RESTful API was only the beginning! By leveraging Joomla's advanced \"pluggable\" architecture and robust ACL, cAPI can transform your website into a true middleware service for anything ranging from SQL servers, MongoDB servers and even Microsoft's Active Directory.",
        "termsOfService": "https://www.annatech.com",
        "contact": {
            "name": "Steve Tsiopanos",
            "url": "https://www.annatech.com",
            "email": "steve.tsiopanos@annatech.com"
        },
        "license": {
            "name": "GNU General Public License version 2 or later",
            "url": "http://www.gnu.org/licenses/gpl-2.0.html GNU/GPL"
        },
        "version": "1.2.5"
    },
    "host": "capi.local.annatech.com/api/v1",
    "basePath": "",
    "schemes": [
        "https"
    ],
    "produces": [
        "application/json"
    ],
    "paths": {
        "ars/dlid": {
            "get": {
                "tags": [
                    "ARS"
                ],
                "summary": "Facilitates secure AJAX update of Akeeba Release System download ID for websites where cAPI is installed.",
                "description": "This method allows cAPI Core and extensions to properly authenticate against the repository server when looking for and attempting to download updates via Joomla Updater.\n\nThis is a limited use-case method because, right now, it is only implemented within the cAPI options view. It relies on a unique nonce, based off the Joomla sessions, to ensure the request to update the DLID (Akeeba Release System Download ID) comes from an authorized source. It also requires a Super Admin Joomla session.\nAlso note that because the DLID is passed through the HTTP header, it is not subject to logging by Apache (or other web server log tools). Always secure your Joomla backend with HTTPS.\n\nBeyond just updating the DLID, this method showcases a proof-of-concept for developing a secure method for implementing browser-based AJAX calls to the web server (although there much more work to be done on this concept, overall).\n\n### Additional Information\n\nSince this method only has a single intended use case, documentation is not provided for other uses, although it is certainly a possiblity.\n\nFor those interested, this is the javascript required to faciliate the AJAX update of the DLID field in the Services Control Panel Options page.",
                "operationId": "postArsDlidByHeaderNonceDlid",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "dlid",
                        "in": "header",
                        "description": "Download ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "nonce",
                        "in": "header",
                        "description": "Nonce",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Download ID update successful."
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/content/list/all": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "Return list of all Joomla content",
                "operationId": "getContentListAll",
                "responses": {
                    "200": {
                        "description": "List of all content"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/content/item/{id}": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "Get Joomla content by ID",
                "operationId": "getContentItemById",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Content ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "List content item"
                    },
                    "401": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not found"
                    }
                }
            }
        },
        "/content/create": {
            "post": {
                "tags": [
                    "Content"
                ],
                "summary": "Create new Joomla content item",
                "operationId": "postContentCreate",
                "parameters": [
                    {
                        "name": "title",
                        "in": "query",
                        "description": "Article title",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "alias",
                        "in": "query",
                        "description": "Article title alias",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "introtext",
                        "in": "query",
                        "description": "Article introtext",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "fulltext",
                        "in": "query",
                        "description": "Article fulltext",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "catid",
                        "in": "query",
                        "description": "Category ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "created_by_alias",
                        "in": "query",
                        "description": "Article author alias",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "access",
                        "in": "query",
                        "description": "Access level",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "language",
                        "in": "query",
                        "description": "Language ID ex. en-GB",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "state",
                        "in": "query",
                        "description": "Set article state: unpublished, published or trashed",
                        "required": true,
                        "type": "integer",
                        "format": "double",
                        "enum": [
                            0,
                            1,
                            -2
                        ]
                    },
                    {
                        "name": "robots",
                        "in": "query",
                        "description": "Robots",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "author",
                        "in": "query",
                        "description": "Metadata: author",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "rights",
                        "in": "query",
                        "description": "Metadata: content rights",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "xreference",
                        "in": "query",
                        "description": "Metadata: x-reference",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Return new content item object"
                    },
                    "401": {
                        "description": "Error"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/content/update/{id}": {
            "put": {
                "tags": [
                    "Content"
                ],
                "summary": "Update Joomla content item by ID",
                "operationId": "putContentUpdateByID",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Article ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "title",
                        "in": "query",
                        "description": "Article title",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "alias",
                        "in": "query",
                        "description": "Article title alias",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "introtext",
                        "in": "query",
                        "description": "Article introtext",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "fulltext",
                        "in": "query",
                        "description": "Article fulltext",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "catid",
                        "in": "query",
                        "description": "Category ID",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "created_by_alias",
                        "in": "query",
                        "description": "Article author alias",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "access",
                        "in": "query",
                        "description": "Access level",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "language",
                        "in": "query",
                        "description": "Language ID ex. en-GB",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "state",
                        "in": "query",
                        "description": "Set article state: unpublished, published or trashed",
                        "required": false,
                        "type": "integer",
                        "format": "double",
                        "enum": [
                            0,
                            1,
                            -2
                        ]
                    },
                    {
                        "name": "robots",
                        "in": "query",
                        "description": "Robots - NOT CURRENTLY IMPLEMENTED",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "author",
                        "in": "query",
                        "description": "Metadata: author - NOT CURRENTLY IMPLEMENTED",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "rights",
                        "in": "query",
                        "description": "Metadata: content rights - NOT CURRENTLY IMPLEMENTED",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "xreference",
                        "in": "query",
                        "description": "Metadata: x-reference - NOT CURRENTLY IMPLEMENTED",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Return update content item object"
                    },
                    "401": {
                        "description": "Error"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/content/delete/{id}": {
            "delete": {
                "tags": [
                    "Content"
                ],
                "summary": "Delete Joomla content item by ID",
                "operationId": "deleteContentDeleteByID",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Article ID",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Content deleted successfully"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "404": {
                        "description": "Not found"
                    }
                }
            }
        },
        "/content/fields": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "List all Joomla content item fields",
                "operationId": "getContentFields",
                "responses": {
                    "200": {
                        "description": "Lists content fields"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/category/list/all": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "List all Joomla Content Categories",
                "operationId": "getCategoryListAll",
                "responses": {
                    "200": {
                        "description": "Lists all content categories"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/category/single/{id}": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "Return Joomla content category by ID",
                "operationId": "getCategorySingleById",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Category ID",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Lists Joomla content category"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/category/list/{id}/categories": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "List Joomla Content Sub-Categories by Parent ID",
                "description": "Note: Does not recurse into sub-levels below designated list",
                "operationId": "getCategoryListByIdCategories",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Category ID",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Lists Joomla content sub-categories"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/category/list/{id}/content": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "List Joomla Content in Category by Category ID",
                "description": "",
                "operationId": "getCategoryListByIdContent",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Category ID",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Lists Joomla content in category"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/category/create": {
            "post": {
                "tags": [
                    "Content"
                ],
                "summary": "Create Joomla Content Category",
                "description": "",
                "operationId": "postCategoryCreate",
                "parameters": [
                    {
                        "name": "title",
                        "in": "query",
                        "description": "Category title",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "alias",
                        "in": "query",
                        "description": "Category title alias",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "description",
                        "in": "query",
                        "description": "Article description",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "parent_id",
                        "in": "query",
                        "description": "Parent ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "published",
                        "in": "query",
                        "description": "Set category published state: unpublished, published or trashed",
                        "required": true,
                        "type": "integer",
                        "format": "double",
                        "enum": [
                            0,
                            1,
                            -2
                        ]
                    },
                    {
                        "name": "access",
                        "in": "query",
                        "description": "Access level",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "robots",
                        "in": "query",
                        "description": "Metadata: robots",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "author",
                        "in": "query",
                        "description": "Metadata: author",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "metadesc",
                        "in": "query",
                        "description": "Metadata description",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "metakey",
                        "in": "query",
                        "description": "Metakey",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "language",
                        "in": "query",
                        "description": "Language ID ex. en-GB",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns created category title"
                    },
                    "401": {
                        "description": "Error"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/category/update/{id}": {
            "put": {
                "tags": [
                    "Content"
                ],
                "summary": "Update Joomla Content Category by ID",
                "description": "",
                "operationId": "putCategoryUpdateById",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Category ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "title",
                        "in": "query",
                        "description": "Category title",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "alias",
                        "in": "query",
                        "description": "Category title alias",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "description",
                        "in": "query",
                        "description": "Article description",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "parent_id",
                        "in": "query",
                        "description": "Parent ID",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "published",
                        "in": "query",
                        "description": "Set category published state: unpublished, published or trashed",
                        "required": false,
                        "type": "integer",
                        "format": "double",
                        "enum": [
                            0,
                            1,
                            -2
                        ]
                    },
                    {
                        "name": "access",
                        "in": "query",
                        "description": "Access level",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "metadesc",
                        "in": "query",
                        "description": "Metadata description",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "metakey",
                        "in": "query",
                        "description": "Metakey",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "language",
                        "in": "query",
                        "description": "Language ID ex. en-GB",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns created category title"
                    },
                    "401": {
                        "description": "Error"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/category/delete/{id}": {
            "delete": {
                "tags": [
                    "Content"
                ],
                "summary": "Delete Joomla Content Category by ID",
                "description": "",
                "operationId": "deleteCategoryDeleteId",
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Category ID",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Category ID deleted successfully"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Error deleting category ID"
                    }
                }
            }
        },
        "/category/fields": {
            "get": {
                "tags": [
                    "Content"
                ],
                "summary": "List all Joomla Content Category Fields",
                "description": "",
                "operationId": "getCategoryFields",
                "responses": {
                    "200": {
                        "description": "Category ID deleted successfully"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/user": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get current logged in user or display if accessing web service as guest.",
                "operationId": "getUser",
                "responses": {
                    "200": {
                        "description": "Returns user object or welcomes guest"
                    }
                }
            }
        },
        "/user/detail/{type}/{value}": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get user detail by user ID, username, email or token ID",
                "description": "",
                "operationId": "getUserDetail",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "type",
                        "in": "path",
                        "description": "Can be id, username, email or token",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "value",
                        "in": "path",
                        "description": "Value should match the defined type",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK"
                    },
                    "400": {
                        "description": "Bad Request: Illegal request type."
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/user/login/{username}/{password}": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Login user",
                "description": "User login authentication via Joomla authentication plugins with username and password. Note that since credentials are passed into the URL, be aware that they can be stored in server logs.\nAPI traffic must traverse a secure (HTTPS) connection.",
                "operationId": "getLoginByUsernamePassword",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "username",
                        "in": "path",
                        "description": "Joomla username",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "value",
                        "in": "path",
                        "description": "Joomla password",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Welcomes logged in user"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/user/logout/{user}/{session}": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Logout user",
                "description": "User logout action via Joomla authentication plugins with username and session ID. Note that since the session ID and username are passed into the URL, be aware that they can be stored in server logs.\nAPI traffic must traverse a secure (HTTPS) connection.",
                "operationId": "getLogoutByUsernamePassword",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "username",
                        "in": "path",
                        "description": "Joomla username",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "session",
                        "in": "path",
                        "description": "Joomla session id",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Confirms successful user logout"
                    },
                    "403": {
                        "description": "Cannot logout user"
                    }
                }
            }
        },
        "/user/edit": {
            "post": {
                "tags": [
                    "User"
                ],
                "summary": "Create user",
                "description": "Create new Joomla user account.",
                "operationId": "postUserEdit",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "name",
                        "in": "query",
                        "description": "Full name",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "username",
                        "in": "query",
                        "description": "User name",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "email",
                        "in": "query",
                        "description": "User email",
                        "required": true,
                        "type": "string",
                        "format": "email"
                    },
                    {
                        "name": "groups",
                        "in": "query",
                        "description": "User groups",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns user id"
                    },
                    "400": {
                        "description": "Could not save user"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "409": {
                        "description": "Could not bind data."
                    }
                }
            }
        },
        "/user/edit/{id}": {
            "put": {
                "tags": [
                    "User"
                ],
                "summary": "Update user",
                "description": "Update existing Joomla user account.",
                "operationId": "putUserEdit",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "User ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "name",
                        "in": "query",
                        "description": "Full name",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "username",
                        "in": "query",
                        "description": "User name",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "email",
                        "in": "query",
                        "description": "User email",
                        "required": false,
                        "type": "string",
                        "format": "email"
                    },
                    {
                        "name": "groups",
                        "in": "query",
                        "description": "User groups",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "block",
                        "in": "query",
                        "description": "Block",
                        "required": false,
                        "type": "integer",
                        "format": "int32"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns user id of updated user"
                    },
                    "400": {
                        "description": "Could not save user"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "409": {
                        "description": "Could not bind data."
                    }
                }
            },
            "delete": {
                "tags": [
                    "User"
                ],
                "summary": "Delete user",
                "description": "Delete existing Joomla user account.",
                "operationId": "deleteUserEdit",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "User ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "mode",
                        "in": "query",
                        "description": "Must use mode=override parameter to authorize deletion of core.admin id.",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns successful response \"Deleted user: [id]\""
                    },
                    "400": {
                        "description": "Error deleting user: [id]"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "410": {
                        "description": "User id does not exist: id"
                    }
                }
            }
        },
        "/user/group/edit": {
            "post": {
                "tags": [
                    "User"
                ],
                "summary": "Create new Joomla user group",
                "description": "Method restricted to users with core.admin permission.",
                "operationId": "postUserGroupEdit",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "parent_id",
                        "in": "query",
                        "description": "Group parent ID",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "title",
                        "in": "query",
                        "description": "Group Title",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "401": {
                        "description": "Error",
                        "schema": {
                            "type": "string",
                            "example": "<p>\"Error: Incorrect format.\"</p><p>\"Error: Group exists.\"</p><p>\"Error: Duplicate title or alias.\"</p>"
                        }
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/group/edit/{id}": {
            "put": {
                "tags": [
                    "User"
                ],
                "summary": "Update existing Joomla user group",
                "description": "Method restricted to users with core.admin permission.",
                "operationId": "putUserGroupEditById",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Group  ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "parent_id",
                        "in": "query",
                        "description": "Group parent ID",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "title",
                        "in": "query",
                        "description": "Group Title",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object",
                            "example": "{\"id\": \"41\",\"parent_id\": 1,\"title\": \"Test Group A1\",\"error\": false,\"status\": 200}"
                        }
                    },
                    "401": {
                        "description": "Error",
                        "schema": {
                            "type": "string",
                            "example": "<p>\"Error: Incorrect format.\"</p><p>\"Error: Group exists.\"</p><p>\"Error: Duplicate title or alias.\"</p>"
                        },
                        "headers": {
                            "Access-Control-Allow-Headers": {
                                "description": "Allowed headers",
                                "type": "string"
                            },
                            "Access-Control-Allow-Methods": {
                                "description": "Allowed methods",
                                "type": "string"
                            }
                        }
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            },
            "delete": {
                "tags": [
                    "User"
                ],
                "summary": "Delete existing Joomla user group",
                "description": "Method restricted to users with core.admin permission.",
                "operationId": "deleteUserGroupEditById",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Group  ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "string",
                            "example": "Deleted group: id"
                        }
                    },
                    "401": {
                        "description": "Error",
                        "schema": {
                            "type": "string",
                            "enum": [
                                "Error: Incorrect format.",
                                "Error: Group exists.",
                                "Error: Duplicate title or alias."
                            ]
                        },
                        "headers": {
                            "Access-Control-Allow-Headers": {
                                "description": "Allowed headers",
                                "type": "string"
                            },
                            "Access-Control-Allow-Methods": {
                                "description": "Allowed methods",
                                "type": "string"
                            }
                        }
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/group/list/all": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "List all Joomla user groups",
                "description": "Lists all Joomla user groups",
                "operationId": "getUserGroupListAll",
                "produces": [
                    "application/json"
                ],
                "responses": {
                    "200": {
                        "description": "OK"
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/group/list/users/{id}": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get list of users by group id",
                "description": "Get list of Joomla users assigned to a group id.\n### mode=0\nMethod to return a list of user Ids contained in a Group.\n### mode=1\nMethod to return a list of user Ids contained in a Group. Recursively include all child groups.",
                "operationId": "getUserGroupListUsersById",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Group  ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "mode",
                        "in": "query",
                        "description": "Mode",
                        "required": false,
                        "type": "integer",
                        "format": "double",
                        "enum": [
                            0,
                            1
                        ]
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns list of users",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/group/list/{id}": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get list of groups by user id",
                "description": "Get list of Joomla groups assigned to a user id.\n### mode=0\nMethod to return a list of user groups mapped to a user. The returned list can optionally hold only\nthe groups explicitly mapped to the user or all groups both explicitly mapped and inherited by the user.\n\n### mode=1\nMethod to return a list of user groups mapped to a user. The returned list can optionally hold only\nthe groups explicitly mapped to the user or all groups both explicitly mapped and inherited by the user.\nInclude inherited user groups.\n\n### mode=2\nMethod to return a list of user groups mapped to a user. Does not include inherited user groups.\nInclude id, title.\n\n### mode=3\nMethod to return a list of user groups mapped to a user. Does not include inherited user groups.\nInclude id, parent_id, title\n\nNull mode or out of bounds value defaults to zero.",
                "operationId": "getUserGroupListById",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "Group ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "mode",
                        "in": "query",
                        "description": "Mode",
                        "required": false,
                        "type": "integer",
                        "format": "double",
                        "enum": [
                            0,
                            1,
                            2,
                            3
                        ]
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns list of users",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/sessions": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get user sessions",
                "description": "Get list of Joomla user sessions",
                "operationId": "getUserSessions",
                "produces": [
                    "application/json"
                ],
                "responses": {
                    "200": {
                        "description": "Returns list of users",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "403": {
                        "description": "Forbidden",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/profile": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get profile from current user session",
                "description": "Get list of Joomla user sessions",
                "operationId": "getUserProfile",
                "produces": [
                    "application/json"
                ],
                "responses": {
                    "200": {
                        "description": "Returns user profile",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "404": {
                        "description": "Profile details not found. May need to save them first.",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            },
            "put": {
                "tags": [
                    "User"
                ],
                "summary": "Update profile from current user session",
                "description": "Updates and returns user profile by current user session.",
                "operationId": "putUserProfile",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "profile_aboutme",
                        "in": "query",
                        "description": "About Me",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_address1",
                        "in": "query",
                        "description": "Address 1",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_address2",
                        "in": "query",
                        "description": "Address 2",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_city",
                        "in": "query",
                        "description": "City",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_country",
                        "in": "query",
                        "description": "Country",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_dob",
                        "in": "query",
                        "description": "Date of Birth",
                        "required": false,
                        "type": "string",
                        "format": "date-time"
                    },
                    {
                        "name": "profile_favoritebook",
                        "in": "query",
                        "description": "Favorite Book",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_phone",
                        "in": "query",
                        "description": "Phone",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_postal_code",
                        "in": "query",
                        "description": "Postal Code",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_region",
                        "in": "query",
                        "description": "Region",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_website",
                        "in": "query",
                        "description": "Website",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns user profile",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "403": {
                        "description": "Not authorized",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "404": {
                        "description": "Profile details not found. May need to save them first.",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/user/profile/{id}": {
            "get": {
                "tags": [
                    "User"
                ],
                "summary": "Get user profile by ID",
                "description": "Returns user profile by ID",
                "operationId": "getUserProfileById",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "User ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns user profile",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "403": {
                        "description": "Not authorized",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "404": {
                        "description": "Profile details not found. May need to save them first.",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            },
            "put": {
                "tags": [
                    "User"
                ],
                "summary": "Update profile by ID",
                "description": "Updates and returns user profile by current user session.",
                "operationId": "putUserProfileById",
                "produces": [
                    "application/json"
                ],
                "parameters": [
                    {
                        "name": "profile_aboutme",
                        "in": "query",
                        "description": "About Me",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_address1",
                        "in": "query",
                        "description": "Address 1",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_address2",
                        "in": "query",
                        "description": "Address 2",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_city",
                        "in": "query",
                        "description": "City",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_country",
                        "in": "query",
                        "description": "Country",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_dob",
                        "in": "query",
                        "description": "Date of Birth",
                        "required": false,
                        "type": "string",
                        "format": "date-time"
                    },
                    {
                        "name": "profile_favoritebook",
                        "in": "query",
                        "description": "Favorite Book",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_phone",
                        "in": "query",
                        "description": "Phone",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_postal_code",
                        "in": "query",
                        "description": "Postal Code",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_region",
                        "in": "query",
                        "description": "Region",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "profile_website",
                        "in": "query",
                        "description": "Website",
                        "required": false,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Returns user profile",
                        "schema": {
                            "type": "object",
                            "example": ""
                        }
                    },
                    "403": {
                        "description": "Not authorized",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "404": {
                        "description": "Profile details not found. May need to save them first.",
                        "schema": {
                            "type": "string"
                        }
                    }
                }
            }
        },
        "/token/{token}": {
            "get": {
                "tags": [
                    "Token"
                ],
                "summary": "Token authentication",
                "description": "Authenticate access to API by token id",
                "operationId": "getTokenByToken",
                "parameters": [
                    {
                        "name": "token",
                        "in": "path",
                        "description": "Token",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Authenticated"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/token/manage/all": {
            "get": {
                "tags": [
                    "Token"
                ],
                "summary": "Get all tokens",
                "description": "Returns list of all tokens",
                "operationId": "getTokenManageAll",
                "responses": {
                    "200": {
                        "description": "List of tokens"
                    },
                    "403": {
                        "description": "Unauthorized"
                    },
                    "404": {
                        "description": "No tokens found"
                    }
                }
            }
        },
        "/token/manage/": {
            "get": {
                "tags": [
                    "Token"
                ],
                "summary": "Get tokens by current user session",
                "description": "Returns list of all tokens associated with the current user's session",
                "operationId": "getTokenManage",
                "responses": {
                    "200": {
                        "description": "List of tokens"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            },
            "post": {
                "tags": [
                    "Token"
                ],
                "summary": "Create token",
                "description": "Create token by current user session.",
                "operationId": "postTokenManageByUserid",
                "parameters": [
                    {
                        "name": "mode",
                        "in": "query",
                        "description": "Mode",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "debug",
                        "in": "query",
                        "description": "Debug",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "log_level",
                        "in": "query",
                        "description": "Log Level",
                        "required": true,
                        "type": "string",
                        "default": "EMERGENCY",
                        "enum": [
                            "EMERGENCY",
                            "ALERT",
                            "CRITICAL",
                            "ERROR",
                            "WARN",
                            "NOTICE",
                            "INFO",
                            "DEBUG",
                            "inherit"
                        ]
                    },
                    {
                        "name": "log_enabled",
                        "in": "query",
                        "description": "Log Enabled",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_encrypt",
                        "in": "query",
                        "description": "Cookies Encrypt",
                        "required": false,
                        "type": "string",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_domain",
                        "in": "query",
                        "description": "Cookies Domain",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "cookies_secure",
                        "in": "query",
                        "description": "Cookies Secure",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_secret_key",
                        "in": "query",
                        "description": "Cookies Secret Key",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "http_version",
                        "in": "query",
                        "description": "HTTP Version",
                        "required": true,
                        "type": "number",
                        "format": "float",
                        "default": "1.10"
                    },
                    {
                        "name": "api_rate_limit",
                        "in": "query",
                        "description": "API Rate Limit",
                        "required": false,
                        "type": "integer",
                        "format": "int32",
                        "default": "0"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successfully created token"
                    },
                    "401": {
                        "description": "Bad request"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "User ID not found"
                    }
                }
            }
        },
        "/token/manage/{type}/{value}": {
            "get": {
                "tags": [
                    "Token"
                ],
                "summary": "Get token(s) by userid, username, email or token",
                "description": "Returns list of all tokens associated with a userid, username, email address or token",
                "operationId": "getTokenManageByTypeValue",
                "parameters": [
                    {
                        "name": "type",
                        "in": "path",
                        "description": "Parameter type",
                        "required": true,
                        "type": "string",
                        "enum": [
                            "id",
                            "username",
                            "email",
                            "token"
                        ]
                    },
                    {
                        "name": "value",
                        "in": "path",
                        "description": "Parameter value",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "List of tokens"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "No tokens found"
                    }
                }
            }
        },
        "/token/manage/userid/{userid}": {
            "post": {
                "tags": [
                    "Token"
                ],
                "summary": "Create token by user ID",
                "description": "Create token by user ID.",
                "operationId": "postTokenManageByUserid",
                "parameters": [
                    {
                        "name": "userid",
                        "in": "path",
                        "description": "User ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "mode",
                        "in": "query",
                        "description": "Mode",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "debug",
                        "in": "query",
                        "description": "Debug",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "log_level",
                        "in": "query",
                        "description": "Log Level",
                        "required": true,
                        "type": "string",
                        "default": "EMERGENCY",
                        "enum": [
                            "EMERGENCY",
                            "ALERT",
                            "CRITICAL",
                            "ERROR",
                            "WARN",
                            "NOTICE",
                            "INFO",
                            "DEBUG",
                            "inherit"
                        ]
                    },
                    {
                        "name": "log_enabled",
                        "in": "query",
                        "description": "Log Enabled",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_encrypt",
                        "in": "query",
                        "description": "Cookies Encrypt",
                        "required": false,
                        "type": "string",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_domain",
                        "in": "query",
                        "description": "Cookies Domain",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "cookies_secure",
                        "in": "query",
                        "description": "Cookies Secure",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_secret_key",
                        "in": "query",
                        "description": "Cookies Secret Key",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "http_version",
                        "in": "query",
                        "description": "HTTP Version",
                        "required": true,
                        "type": "number",
                        "format": "float",
                        "default": "1.10"
                    },
                    {
                        "name": "api_rate_limit",
                        "in": "query",
                        "description": "API Rate Limit",
                        "required": false,
                        "type": "integer",
                        "format": "int32",
                        "default": "0"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successfully created token"
                    },
                    "401": {
                        "description": "Bad request"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "User ID not found"
                    }
                }
            }
        },
        "/token/manage/tokenid/{tokenid}": {
            "put": {
                "tags": [
                    "Token"
                ],
                "summary": "Update token by ID",
                "description": "Update token parameters by token ID.",
                "operationId": "putTokenManageByTokenid",
                "parameters": [
                    {
                        "name": "tokenid",
                        "in": "path",
                        "description": "Token ID",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "token",
                        "in": "query",
                        "description": "Token Reset",
                        "required": false,
                        "type": "string",
                        "default": "",
                        "enum": [
                            "",
                            "reset"
                        ]
                    },
                    {
                        "name": "state",
                        "in": "query",
                        "description": "State",
                        "required": false,
                        "type": "integer",
                        "format": "double",
                        "default": "1",
                        "enum": [
                            0,
                            1,
                            -2
                        ]
                    },
                    {
                        "name": "mode",
                        "in": "query",
                        "description": "Mode",
                        "required": false,
                        "type": "integer",
                        "format": "double"
                    },
                    {
                        "name": "debug",
                        "in": "query",
                        "description": "Debug",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "log_level",
                        "in": "query",
                        "description": "Log Level",
                        "required": true,
                        "type": "string",
                        "default": "EMERGENCY",
                        "enum": [
                            "EMERGENCY",
                            "ALERT",
                            "CRITICAL",
                            "ERROR",
                            "WARN",
                            "NOTICE",
                            "INFO",
                            "DEBUG",
                            "inherit"
                        ]
                    },
                    {
                        "name": "log_enabled",
                        "in": "query",
                        "description": "Log Enabled",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_encrypt",
                        "in": "query",
                        "description": "Cookies Encrypt",
                        "required": false,
                        "type": "string",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_domain",
                        "in": "query",
                        "description": "Cookies Domain",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "cookies_secure",
                        "in": "query",
                        "description": "Cookies Secure",
                        "required": false,
                        "type": "string",
                        "default": "false",
                        "enum": [
                            "true",
                            "false"
                        ]
                    },
                    {
                        "name": "cookies_secret_key",
                        "in": "query",
                        "description": "Cookies Secret Key",
                        "required": false,
                        "type": "string"
                    },
                    {
                        "name": "http_version",
                        "in": "query",
                        "description": "HTTP Version",
                        "required": true,
                        "type": "number",
                        "format": "float",
                        "default": "1.10"
                    },
                    {
                        "name": "api_rate_limit",
                        "in": "query",
                        "description": "API Rate Limit",
                        "required": false,
                        "type": "integer",
                        "format": "int32",
                        "default": "0"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successfully deleted token"
                    },
                    "400": {
                        "description": "Bad request"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Token not found"
                    },
                    "409": {
                        "description": "Conflict: Cannot change token used to access this service method"
                    }
                }
            },
            "delete": {
                "tags": [
                    "Token"
                ],
                "summary": "Delete token by ID",
                "description": "Delete token for user ID or current user by session.",
                "operationId": "deleteTokenManageByTokenid",
                "parameters": [
                    {
                        "name": "tokenid",
                        "in": "path",
                        "description": "Token ID",
                        "required": true,
                        "type": "integer",
                        "format": "double"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Successfully deleted token"
                    },
                    "400": {
                        "description": "Bad request"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Token not found"
                    },
                    "409": {
                        "description": "Conflict: Cannot change token used to access this service method"
                    }
                }
            }
        },
        "/slim/routes": {
            "get": {
                "tags": [
                    "Slim"
                ],
                "summary": "Returns list of all configured Slim service methods",
                "operationId": "getSlimRoutes",
                "produces": [
                    "application/json"
                ],
                "responses": {
                    "200": {
                        "description": "OK"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        },
        "/slim/swagger": {
            "get": {
                "tags": [
                    "Slim"
                ],
                "summary": "Returns Swagger definition JSON",
                "responses": {
                    "200": {
                        "description": "OK"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                }
            }
        }
    },
    "definitions": {},
    "securityDefinitions": {
        "token": {
            "type": "apiKey",
            "name": "token",
            "in": "header"
        }
    },
    "externalDocs": {
        "description": "Find out more about cAPI",
        "url": "https://getcapi.io"
    }
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Fri, 16 Sep 2016 22:00:57 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.6.25
Access-Control-Allow-Origin: *
Joomla-Sessionid: ph5dtdd5994h8prkd0r524b153
Set-Cookie: joomla_user_state=logged_in; path=/
Set-Cookie: joomla_user_state=logged_in; path=/
Set-Cookie: bfec76bff79ab0f46afd38930989604a=ph5dtdd5994h8prkd0r524b153; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json

```