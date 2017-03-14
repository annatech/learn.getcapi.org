---
title: 'Version 1.1.0'
taxonomy:
    tag:
        - changelog
    category:
        - docs
---

## Overview


* 	Return false for rateLimitServicesSlim() if no token is set.		

* 	Fix token auth so that it overrides and logs out current session if supplied token is invalid.		
 
* 	Modification to token handling in getSlimConfig() to reduce PHP errors.		
 
* 	Modificatinos to all Trashing and Deleting of Content and Categories.		
 
* 	Library and Packages manifest files updated with Phing-parsed version tag.				
  
* 	Version wildcard to be parsed by Phing.				
 
* 	Updated content and category creation service routes to include create, delete and update in the respective URL request.				
* 	Build services routes for getting and updating User Profile data.				
 
* 	Create service route Delete Joomla Content Category by ID.				
 
* 	Continuing developement on Update Joomla Content Category by ID.				
  
* 	Change array key from 'content' to 'article'.	
 
* 	Fixed slim api limitation and overrides.		
 
* 	Improvides to category service routes.		
 
* 	Added version parsed tag (by Phing) to manifest files.		
 
* 	Fixed bug with API Rate Limit override.		
  
* 	Fix code to match proper current com_services version.		
 
* 	Change to "Joomla-Sessionid".				
 
* 	Update RateLimit Retry-After.			
 
* 	Remove unecessary return.			
 
* 	Modfity RateLimit response headers.			
 
* 	Modify RateLimit header response to match Laravel.		
 
* 	Finished work on service call to Update Joomla Content by ID.		
 
* 	Remove some unnecessary line breaks.			
 
* 	Clean-up and improve category and content service routes.			
 
* 	Simplify GET /content JSON output.				
 
* 	Fix POST handling for Content creation.			
  
* 	Fix POST input processing for category creation.			
  
* 	Fix category metadata.			
 
* 	Fix content category designation.			
 
* 	Fixes to new category creation.	
 
* 	Fixed created_time for new category creation.			
 
* 	Replace DB queary with JTable for working with Joomla content and category tables.		
 
* 	Build Create Joomla Content Category route - PUT /category.Additional cleanup on 401 vs 403 responses.		
 
* 	Improved GET /content/:id and expanded category service routes.		
 
* 	Build new Joomla Category and Content service routes.			