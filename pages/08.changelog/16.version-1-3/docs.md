---
title: 'version 1.3.5'
taxonomy:
    category:
        - docs
    tag:
        - changelog
---

## Overview
### Released 
2017-11-15

cAPI v1.3.4 introduces basic HTTP authentication via Authorization header and a collection of methods allowing API access to Component Model & Table data.

This release includes the following:

* Improve error trapping for GET component/model/data
* Validate getInstance for getComponentModelData
* Validate JTable::getInstance input for getComponentTableDataById
* Build advanced filtering for getComponentModelData
* Implement Joomla ACL per component and individual asset item.
* New method getComponentModelData
* Complete development on getComponentTableDataById.Include get_class_methods boolean check in URLparameter to allow class methods and associated parameters to be included in the response (requires core.edit for related component).
* Update getComponentTableData to getComponentTableDataById.Method will return table data for single ID request.
* Create method getComponentTableData
* New method getComponentTableFields for returning component fields.
* Initial work completed on getComponentListAll. Returns list of all components, along with table and model classes for "site" and "administrator" contexts.
* Include Basic Authentication SecurityScheme definition.
* Methods to allow Basic Authentication through Authorization header or force HTTP Apache Auth via URL variable basic_auth=true.
* Create new class ServicesJoomlaHelpersComponent().
* Increment to version 1.3.4.

Previous release:

Remove extraneous tag_link_class parameter
Increment cAPI version to 1.3.3
Resolve bug with successful updating of dlid in update_sites table, extra_query field when editing the Download ID parameter in com_services component options.
Updated documentation can be found here:
[http://learn.getcapi.org ](http://learn.getcapi.org )

API Doc and Sandbox

[https://getcapi.io](https://getcapi.io)