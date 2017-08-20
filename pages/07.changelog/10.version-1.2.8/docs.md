---
title: 'version 1.2.8'
taxonomy:
    category:
        - docs
    tag:
        - changelog
---

## Overview
### Released 
2017-04-15

* Remove unnecessary language item definition.
* Remove unnecessary array definition.
* Remove slim_php_framework view and related files and language parameters as they are no longer needed.
* Symmetrically encrypt swaggerjson path parameter as "cryptoKey" key value store in user session.
* Create service route getSlimSwaggerRemoteByUrl.Update com_services to use this route for the view swaggeruimisc.
* Commit previously unversioned files.
* Menu item parameter configuration for swaggeruimisc view for com_services
* Create swaggeruimisc view for com_services to allow for front-end presentation of any pre-configured Swagger JSON definition file.
* Resolve issues with proper handling of CORS preflight requests.
* Fix bug with proper setting of Access-Control-Allow-Origin with respect to CORS.
* Update token handling for parameter and header value to ensure acceptance.
* Created PUT /tag and DELETE /tag methods.Working on Swagger docs.
* Use jModel for postTag.Improve getTagNameById
* Complete initial work on postTag.TODO: Finish metadata handling and parameters. Finish swagger doc block.
* getTagFields, postTag
* getTagTypes, getTagSearch, getTagNameById
* Build new Tag methods.
* Include "Authorization" in Access-Control-Allow-Headers as per request https://www.annatech.com/forums/capi-wish-list/25-adding-authorization-in-htaccess.html#84
* Update version and year.

Updated documentation can be found here:

[http://learn.getcapi.org](http://learn.getcapi.org)

API Doc and Sandbox

[https://getcapi.io](https://getcapi.io)