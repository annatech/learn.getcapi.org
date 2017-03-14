---
title: 'version 1.2.5'
---

## Overview


* Finish changes to token manage methods.
* Update GET /user/profile to check if user is Guest and prompt to log in first.
* Update annotationand params calls for postCategoryUpdateById
* Finish building all CRUD token service methods.
* Update random token generation algorithm.
* Remove http scheme from doc
* Update token generation code.
* Add CryptoLib package to Services library
* Working on new service method postTokenManageById
* Changed filter for token generation.
* Remove random number appended to generated token.
* Update annotation all docblock annotations for service routes with Doctrine syntax to faciliate Swagger.json generation
* Point swagger.json location to corresponding service method /slim/swagger
* Fix some annotation formatting
* Correction to ARS annotation
* Update file header annotation
* Create Swagger annotation for postArsDlidByHeaderNonceDlid
* Update annotation for getTokenManageByTypeValue
* Update annotation for getTokenManageByTypeValue
* Fix token annotation
* Create Swagger annotation for getTokenManageByTypeValue
* Create Swagger annotation for getTokenManage
* Create Swagger annotation for getTokenManageAll
* Create Swagger annotation for getTokenByToken
* Create Swagger annotation for getCategoryFields and fix a few other annotation errors
* Update annotations and params calls for putCategoryUpdateById
* Create Swagger annotation for postCategoryUpdateById
* Create Swagger annotation for postCategoryCreate
* Create Swagger annotation for getCategoryListByIdContent
* Create Swagger annotation for getCategoryListByIdCategories
* Create Swagger annotation for getCategoryListByIdCategories
* Create Swagger annotation for getCategorySingleById
* Create Swagger annotation for getCategoryListAll
* Create Swagger annotation for getContentFields
* Create Swagger annotation for deleteContentDeleteByID
* Update Swagger annotation for putContentUpdateByID
* Create Swagger annotation for putContentUpdateByID and fix some other content methods.
* Swagger annotation for postContentCreate along with fixes to the create content code.
* Create Swagger annotation for postContentCreate
* Corrections to Swagger annotation for getContentItemById
* Change path for getContentItemById to /content/item/{id}
* Create Swagger annotation getContentSingleById
* Create Swagger annotation for getContentListAll
* Create Swagger annotation for putUserProfileById
* Create Swagger annotation for putUserProfile
* Create Swagger annotation for getUserProfileById
* Create Swagger annotation for getUserProfile
* Create Swagger annotation for getUserSessions
* Update getUserGroupListUsersById
* Create Swagger annotation for getUserGroupListAll.
* Create Swagger annotation for deleteUserGroupEditById
* Update annotation.
* Point Swagger UI to locally generated Swagger.json at /api/v1/slim/swagger
* Fix Swagger base path generation.
* Create Swagger annotation deleteUserEdit
* Create Swagger annotation for putUserEdit
* Create postUserEdit annotation
* Create annotation getLogoutByUsernamePassword
* Update annotations for getUser and getUserDetail
* Update swagger json path.
* Add composer file.
* Add new libraries to lib_services and update composer files for services directory.
* Configure inline Swagger annotation.
* Fix install script so it updates the contents of the api folder on subsequent reinstalls.
* Add %%licensename%% regex pattern.
* Add symfony vendor folder to lib_services.
* Add palanik vendor library to lib_services
* Increment version to 1.2.5.
* Add doctrine and zircote vendor libraries to lib_services.
* Create service method /token/manage/all to return list of all tokens.
* Fix bugs in /token/manage services route.
* Fix getUserIdbyToken to accomodate + symbol in token.TODO: Should eventually disallow + from token value creation.
* Build tokenManage service methods.
* Create service methods for retrieving collections of tokens by userid, username, email, token or current session.
* Expose protected and private functions to public.
* Build method to retrieve user details by id, email, username or token.
* Building token read and create service methods.
* Updates to Get user details by user ID, username, email or token ID
* Find user by username in GET /user/detail/:type/:value
* Create method GET /user/detail/:type/:value
* Remove aid from GET /user response.
* Update GET /user to include user object details.