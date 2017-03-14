---
title: 'Version 1.2.1'
---

## Overview

cAPI Core v1.2.1 introduces new methods for performing CRUD (Create, Read, Update, Delete) operations on users and groups.

Updated documentation can be found here:
http://learn.getcapi.org 

NOTE: 

New methods:

### POST /user/edit
### PUT /user/edit/:id
### DELETE /user/edit/:id
### POST /user/group/edit
### PUT /user/group/edit/:id
### DELETE /user/group/edit/:id
### GET /user/group/list/all
### GET /user/group/list/users/:id
### GET /user/group/list/:id

v1.2 branch GIT commits listed below. 

* Change from "==" "===". 9 mins ago  
* Fix "Delete group" validation. Yesterday  
* Clean up docblocks. Yesterday  
* Change to === Yesterday  
* Clean up docblocks. Yesterday  
* Set error code to 410 for "User does not exist." Yesterday  
* Fix validation for existing user on "Delete user" method. Yesterday  
* Working on "Delete user" method.Also fixed a typo in a comment block. Yesterday  
* Finished "Delete group" method. 2 days ago  
* Working on "Update group" method. 2 days ago  
* Remove lft and rgt in "Create group" method response. 2 days ago  
* Include lft and rgt in "Create group" method response. 2 days ago  
* Fix parent_id validation in "Create group" method. 2 days ago  
* Fix to ensure "Create group" does not set a parent_id Fix to ensure "Create group" does not set a parent_id < 1. 2 days ago  
* Add parent_id to "Create group" response. 2 days ago  
* Finish building "Create group" method. 2 days ago  
* Finish building "Get list of users by group id".Includes 2 mode parameters to customize response. 4 days ago  
* Finish building "Get list of groups by user id".Includes 4 mode parameters to customize response. 4 days ago  
* Working on group list service methods. 5 days ago  
* Working on group list service methods. 5 days ago  
* Build user group list methods. 5 days ago  
* Finished "Get list of groups by user id" 6 days ago  
* Removed unecessary jimport( 'joomla.user.helper') 6 days ago  

