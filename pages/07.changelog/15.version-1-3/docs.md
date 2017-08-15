---
title: 'version 1.3.3'
---

## Overview
### Released 
2017-07-22

cAPI v1.3.2 is one of the biggest releases to date, ecompassing not only bug fixes and feature improvements, but also including every component from the fantastic ReactPHP library. This lays the foundation for new functionality including asynchronous event handling, non-blocking I/O operations, high-speed messaging queuing and much more!

This release includes the following:

* Remove updateserver for services/slimjsonapiview plugin.Remove updateserver for services/slimjsonapiview plugin.
* Remove updateserver for services/slimjsonapimiddleware plugin
* Remove updateserver for services/slim
* Remove updateserver for services/rest plugin.
* Remove updateserver for services/joomla
* Remove updateserver for lib_services.
* Remove updateserver for com_services.
* Build component options fields and logic to control view-access to Swagger UI routes for each services plugin.
* Update Swagger definition description for cAPI.
* Bug fixes to authentication for getUserDetailByTypeValue.
* Allow Super Users (or where user's session matches requested user detail) to access getUserDetailByTypeValue
* Return responses for getUserDetailByTypeValue as object instead of as sub-elements of array[0].
* Require Super User permissions for getUserDetailByTypeValue.
* Update Joomla minimum version to 3.6.
* Update cAPI Core Package manifest file to include new include libraries and provide link to learn.getcapi.org.
* Add additional services folders to lib_services.xml manifest.
* Fix 500 error getCategoryListByIdCategories when searching category id which does not exist.
* Update zircote/swagger-php 2.0.10
* Update doctrine/annotations library
* Add symfony/finder libraries
* Fix typo in guzzlehttp vendor library folder name.
* Updated lib_services.xml manifest to include new ReactPHP libraries.
* Update Composer library files to include ReactPHP libraries.
* Add libraries and associated dependencies for ReactPHP
* Update zircote/swagger-php to v2.0.10
* Upgrade Slim Framework to v2.6.3
* Commit remaining unversioned files added to /libararies/services/
* Include web.config in /libraries/services/
* Commit updated symfony vendor library in /libraries/services/symfony to match J37.x
* Included updated psr vendor library in /libraries/services/psr
* Include updated Joomla vendor library in /libraries/services/joomla to match compatibility with Joomla 3.7.x
* Increment Joomla ID to j37

Previous release:

* Swagger documentation fixes for Tag service routes.
* BUG FIX - Resolved issue with REST API limitation for token access not working properly since version 1.2.8.

Updated documentation can be found here:

[http://learn.getcapi.org](http://learn.getcapi.org)

API Doc and Sandbox

[https://getcapi.io](https://getcapi.io)