---
title: 'GET slim/routes'
published: true
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: false
child_type: default
routable: true
cache_enable: true
visible: true
---

Returns list of all configured Slim service methods

### Resource URL
https://yourdomain.com/api/v1/slim/routes

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | YES - core.admin |
| Rate limited    | NO |

### Parameters

Method does not accept parameters.

### Example Request

GET
https://yourdomain.com/api/v1/slim/routes

### Example Result

#### JSON Response

```json
{
  "0": "getTokenByToken : \/token\/:token",
  "1": "getTokenManageAll : \/token\/manage\/all",
  "2": "getTokenManage : \/token\/manage\/",
  "3": "getTokenManageByTypeValue : \/token\/manage\/:type\/:value",
  "4": "postTokenManageByUserid : \/token\/manage(\/(userid\/:userid))",
  "5": "putTokenManageByTokenid : \/token\/manage\/tokenid\/:tokenid",
  "6": "deleteTokenManageByTokenid : \/token\/manage\/tokenid\/:tokenid",
  "7": "getTokenByToken : \/token\/:token",
  "8": " : \/slim\/swagger",
  "9": "getSlimRoutes : \/slim\/routes",
  "10": " : \/ars\/dlid",
  "11": " : \/ars\/dlid",
  "12": " : \/content\/list\/all",
  "13": "getContentItemById : \/content\/item\/:id",
  "14": "postContentCreate : \/content\/create",
  "15": "putContentUpdateByID : \/content\/update\/:id",
  "16": "deleteContentDeleteByID : \/content\/delete\/:id",
  "17": "getContentFields : \/content\/fields",
  "18": "getCategoryListAll : \/category\/list\/all",
  "19": "getCategorySingleById : \/category\/single\/:id",
  "20": "getCategoryListByIdCategories : \/category\/list\/:id\/categories",
  "21": "getCategoryListByIdContent : \/category\/list\/:id\/content",
  "22": "postCategoryCreate : \/category\/create",
  "23": "putCategoryUpdateById : \/category\/update\/:id",
  "24": " : \/category\/delete\/:id",
  "25": "getCategoryFields : \/category\/fields",
  "26": " : \/content\/list\/all",
  "27": "getContentItemById : \/content\/item\/:id",
  "28": "postContentCreate : \/content\/create",
  "29": "putContentUpdateByID : \/content\/update\/:id",
  "30": "deleteContentDeleteByID : \/content\/delete\/:id",
  "31": "getContentFields : \/content\/fields",
  "32": "getCategoryListAll : \/category\/list\/all",
  "33": "getCategorySingleById : \/category\/single\/:id",
  "34": "getCategoryListByIdCategories : \/category\/list\/:id\/categories",
  "35": "getCategoryListByIdContent : \/category\/list\/:id\/content",
  "36": "postCategoryCreate : \/category\/create",
  "37": "putCategoryUpdateById : \/category\/update\/:id",
  "38": " : \/category\/delete\/:id",
  "39": "getCategoryFields : \/category\/fields",
  "40": "getUser : \/user",
  "41": "getUserDetail : \/user\/detail\/:type\/:value",
  "42": "getLoginByUsernamePassword : \/user\/login\/:username\/:password",
  "43": "getLogoutByUsernamePassword : \/user\/logout\/:user\/:session",
  "44": "postUserEdit : \/user\/edit",
  "45": "putUserEdit : \/user\/edit\/:id",
  "46": "deleteUserEdit : \/user\/edit\/:id",
  "47": "postUserGroupEdit : \/user\/group\/edit",
  "48": "putUserGroupEditById : \/user\/group\/edit\/:id",
  "49": "deleteUserGroupEditById : \/user\/group\/edit\/:id",
  "50": "getUserGroupListAll : \/user\/group\/list\/all",
  "51": "getUserGroupListUsersById : \/user\/group\/list\/users\/:id",
  "52": "getUserGroupListById : \/user\/group\/list\/:id",
  "53": "getUserSessions : \/user\/sessions",
  "54": "getUserProfile : \/user\/profile",
  "55": "getUserProfileById : \/user\/profile\/:id",
  "56": "putUserProfile : \/user\/profile",
  "57": "putUserProfileById : \/user\/profile\/:id",
  "58": "getUser : \/user",
  "59": "getUserDetail : \/user\/detail\/:type\/:value",
  "60": "getLoginByUsernamePassword : \/user\/login\/:username\/:password",
  "61": "getLogoutByUsernamePassword : \/user\/logout\/:user\/:session",
  "62": "postUserEdit : \/user\/edit",
  "63": "putUserEdit : \/user\/edit\/:id",
  "64": "deleteUserEdit : \/user\/edit\/:id",
  "65": "postUserGroupEdit : \/user\/group\/edit",
  "66": "putUserGroupEditById : \/user\/group\/edit\/:id",
  "67": "deleteUserGroupEditById : \/user\/group\/edit\/:id",
  "68": "getUserGroupListAll : \/user\/group\/list\/all",
  "69": "getUserGroupListUsersById : \/user\/group\/list\/users\/:id",
  "70": "getUserGroupListById : \/user\/group\/list\/:id",
  "71": "getUserSessions : \/user\/sessions",
  "72": "getUserProfile : \/user\/profile",
  "73": "getUserProfileById : \/user\/profile\/:id",
  "74": "putUserProfile : \/user\/profile",
  "75": "putUserProfileById : \/user\/profile\/:id",
  "76": " : \/cms",
  "77": " : \/cms",
  "78": " : \/return",
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Fri, 16 Sep 2016 21:53:46 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.6.25
Access-Control-Allow-Origin: *
Joomla-Sessionid: *************************
Set-Cookie: joomla_user_state=logged_in; path=/
Set-Cookie: joomla_user_state=logged_in; path=/
Set-Cookie: bfec76bff79ab0f46afd38930989604a=uo290fju5oi1m7rhoss4tqbp41; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json
```