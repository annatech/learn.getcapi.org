---
title: 'version 1.3.3'
---

## Overview
### Released 
2017-08-12

cAPI v1.3.3 includes a bug fix for the Download ID component parameter and how it populates extra_query field in the update_sites table. It's likely that the previous couple releases may not automatically update via the Joomla Updater (even with your Download ID configured). If that is the case, you should download and install cAPI Core v1.3.3, manually.

This release includes the following:

* Remove extraneous tag_link_class parameter
* Increment cAPI version to 1.3.3
* Resolve bug with successful updating of dlid in update_sites table, extra_query field when editing the Download ID parameter in com_services component options.

Previous release:

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

Updated documentation can be found here:

[http://learn.getcapi.org](http://learn.getcapi.org)

API Doc and Sandbox

[https://getcapi.io](https://getcapi.io)