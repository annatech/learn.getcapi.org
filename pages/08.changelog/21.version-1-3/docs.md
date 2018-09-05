---
title: 'version 1.3.5.1'
taxonomy:
    category:
        - docs
    tag:
        - changelog
---

## Overview
### Released 
2018-02-21

#### cAPI v1.3.5
* 	Fix GET /tag/types response to JSON decode any encoded fields.
* 	Add en-GB language definition for COM_SERVICES_ITEM_DELETED_SUCCESSFULLY
* 	Add en-GB language definitions for token views.
* 	Add en-GB definition for COM_SERVICES_TOKENS_ACTIONS
* 	Update docblocks to parameterize license, copyright, author and version for build plan.
* 	Temporary update to improve compatibility with CORS on different browsers until a more granular solution is implemented.
* 	Allow for blank or null dlid values.
* 	Create validation rule class JFormRuleCapidlid for capidlid and move function setDlid() into this validation rule.This allows for dlid updates on save and save & close and ensures only validated input is saved.
* 	Resolve bug which prevented the cAPI download ID from properly being assigned to the extension update site.* Remove dedicated capi/dlid library and associated ARS dlid API methods and refactor that functionality into a custom Joomla field for com_services administration.
* 	Remove Akeeba Release System (ARS) API method GET /ars/dlid
* 	Update downloadid field schema
* 	Remove dlid from capi services and add capidlid.php custom field class to com_services models.
* 	Resolve issues with token and tokens views and configure administrator custom field token.xml
* 	Token custom field for administrator and site token edit view.Userid for site token edit view, required to force pre-population of userid of current session.
* 	Resolve bug with status icon in tokens list.
* 	Remove mode and debug from tokens administrative view.
* 	Update com_services admin images
* 	Update language definitions.
* 	Remove api_throttle front-end filter item
* 	Add userid.php class to /administrator/com_services/models/fields/
* 	Compatibility updates to /administrator/components/com_services/views/token/tmpl/edit.php
* 	Create com_services administrative model field class token.php
* 	Compatibility updates to /administrator/components/com_services/views/token/view.html.php
* 	Compatibility updates to /administrator/components/com_services/views/tokens/tmpl/default.php
* 	Update docblocks with variablized fields.
* 	Compatibility updates to /administrator/components/com_services/views/tokens/view.html.php
* 	Update docblocks with variablized fields.
* 	Corrections to controller.php docblock
* 	Remove history from component configuration.
* 	Create custom read-only front-end field userid.php to populate tokenform.
* 	Create custom front-end field type: token
* 	Remove fixed default token value in front-end view and make read-only
* 	Include front-end view classes for tokens.
* 	Update joomla-packager.xml to prevent errant deletion of build directory folder.
* 	Include installer structure.xml with com_services component.
* 	Compatibility updates to com_services services.xml
* 	Update joomla-packager to place media files in correct location in compiled package and updated services.xml to include parameters for media file installation.
* 	Increment version to 1.3.5 and updated copyright date to 2018.
* 	Resolve bug which results in the following error when any level of error reporting is enabled."NOTICE: Trying to get property of non-object"
* 	Include postflight() function in com_services script.php to automatically enable services plugins, included with pkg_capi_core, after they have been installed.
* 	Revert work on package manifest installer script.Move functionality into component installer script.
* 	Update joomla-packager.xml to handle Package install scripts.
* 	Update package script name and manifest reference to pkg_capi_core.php
* 	Include reference to package script file pkg_script.php
* 	Removed commented-out parameters from com_services services.xml
* 	Remove plugin install function from script.php
* 	Revert changes to language file folder definition.
* 	Ensure /installer/structure.xml is created in build, but removed from original directory /administrator/installer/
* 	Updated to accommodate structure.xml
* 	Compatibility updates to /components/com_services/services.php
* 	Compatibility updates to /components/com_services/router.php
* 	Compatibility updates to /components/com_services/controller.php
* 	Update copyright year in doc blocks
* 	Compatibility updates to /components/com_services/views/swaggeruimisc/view.html.php
* 	Compatibility updates to /components/com_services/views/swaggerui/view.html.php
* 	Compatibility updates to /components/com_services/views/slimphpframework/tmpl/default_filter.php
* 	Compatibility updates to /components/com_services/views/slimphpframework/view.html.php
* 	Compatibility updates to all front-end model fields. Includes two new fields:filemultiple.php modifiedby.php
* 	Add token form and filter xml files to front-end model forms.
* 	Compatibility updates to /components/com_services/models/slimphpframework.php
* 	Add front end models for token management.
* 	Compatibility update to /components/com_services/helpers/services.php
* 	Add front-end controllers for token management.
* 	Compatibility update to /components/com_services/controllers/slimphpframework.php
* 	Compatibility update to /plugins/search/services/services.xml
* 	Compatibility update to /plugins/search/services/services.php
* 	Add com_services media to component
* 	Update config.xml with comment block including latest examples of fields.
* 	Compatibility update to /administrator/components/com_services/script.php
* 	Compatibility update to com_services config.xml
* 	Compatibility updates to /administrator/components/com_services/controller.php
* 	Compatibility updates to /administrator/components/com_services/services.php
* 	New administrator model field modifiedby.php
* 	New administrator model field filemultiple.php
* 	Compatibility update to services.css
* 	Compatibility updates to /administrator/components/com_services/controllers/token.php
* 	Compatibility updates to /administrator/components/com_services/controllers/tokens.php
* 	New com_servers administrator helper class listhelper.php
* 	Compatibility updates to /administrator/components/com_services/helpers/services.php
* 	Compatibility updates to /administrator/components/com_services/models/fields/timeupdated.php
* 	Compatibility updates to /administrator/components/com_services/models/fields/timecreated.php
* 	Compatibility updates to /administrator/components/com_services/models/fields/foreignkey.php
* 	Compatibility updates to /administrator/components/com_services/models/fields/custom_field.php
* 	Compatibility updates to /administrator/components/com_services/models/fields/createdby.php
* 	Compatibility update: include /administrator/components/com_services/models/forms/filter_tokens.xml
* 	Remove token default setting in token.xml
* 	Compatiblity updates to /administrator/components/com_services/models/forms/token.xml
* 	TODO: These administrator model classes will needs to be updated in a future release:- slimphpframework.php - swaggerui.php
* 	Compatibility updates to /administrator/components/com_services/models/token.php
* 	Compatibility updates to /administrator/components/com_services/models/tokens.php
* 	New sql update script: update.mysql.utf8.sql
* 	Remove default time for checked_out_time and last_used.
* 	Update class ServicesTabletoken to match current Joomala development guidelines.
* 	Updated GET /token/manage/all to required either general core.admin or com_services core.admin in order to list all tokens.IMPORTANT: Within Service Control Panel > options > permissions, a group should NOT be given "Configure ACL & Options" privilege if the administrator does not intend that group to have core.admin privilege on com_services.
* 	Updated security on updateTokenServicesRestManage() and deleteTokenServicesRestManage() - restrict to core.edit.own privilege on specified $tokenid
* 	Remove check preventing requester from deleting the same token used to authenticate access to the method.Updated permissions to allow non-core.admin users to delete their own tokens.
* 	Update tokenServicesRestManage() to allow own-token updates in current session.


Updated documentation can be found here:
[http://learn.getcapi.org ](http://learn.getcapi.org )

API Doc and Sandbox

[https://getcapi.io](https://getcapi.io)