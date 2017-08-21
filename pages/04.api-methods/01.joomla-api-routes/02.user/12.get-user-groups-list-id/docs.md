---
title: 'GET user/group/list/:id'
taxonomy:
    category:
        - docs
---

Get list of groups by user id.
         
 @param mode
 mode=0: Method to return a list of user groups mapped to a user. The returned list can optionally hold only
 the groups explicitly mapped to the user or all groups both explicitly mapped and inherited by the user.

 mode=1: Method to return a list of user groups mapped to a user. The returned list can optionally hold only
 the groups explicitly mapped to the user or all groups both explicitly mapped and inherited by the user.
 Include inherited user groups.

 mode=2: Method to return a list of user groups mapped to a user. Does not include inherited user groups.
 Include id, title.

 mode=3: Method to return a list of user groups mapped to a user. Does not include inherited user groups.
 Include id, parent_id, title

 Null mode or out of bounds value defaults to zero.

>>> UNDER CONSTRUCTION - PAGE INCOMPLETE