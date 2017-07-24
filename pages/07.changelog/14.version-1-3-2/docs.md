---
title: 'version 1.3.2'
---

## Overview
### Released 
2017-05-11

The release of cAPI v1.3.1 includes the following:

* Swagger documentation fixes for Tag service routes.
* BUG FIX - Resolved issue with REST API limitation for token access not working properly since version 1.2.8.

Previous release:

**cAPI v1.3.0 is now fully compatible with Joomla 3.7!**

* Increment to v1.3.0. This is done to accommodate major changes to class autoloading from services plugins helpers. Also includes a minor response scheme change to GET /user route.
* Refactor to register JLoader prefix "Services" to faciliate autoloading of helper classes in services plugins.
* Correction to doc block summary for getTagFields.
* Remove outside array dimension [0] from user getUser response.
* Remove $application->getInstance();
* Change to JUri()->isSSL() for SSL check in swaggerui administrative view.
* Update class name instantiation to ServicesRestHelpersTokenmanage.
* Cross domain access is now fully handled in code.
* BUG: Update GET /token/:token to prevent auth failure when logging in with account matching existing session.
* Updating to resolve compatibility issues with J3.7.
* Update documentation for getTokenByToken.

Updated documentation can be found here:

[http://learn.getcapi.org](http://learn.getcapi.org)

API Doc and Sandbox

[https://getcapi.io](https://getcapi.io)