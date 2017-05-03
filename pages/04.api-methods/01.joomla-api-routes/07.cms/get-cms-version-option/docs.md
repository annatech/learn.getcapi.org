---
title: 'GET cms/version/:option'
taxonomy:
    category:
        - docs
---

Return Joomla CMS version information in different formats.

#### Additional Information

##### shortversion
Gets a PHP standardized version string for the current Joomla.

##### longversion
Gets a version string for the current Joomla with all release information.

##### useragent
Returns the user agent.

##### helpversion
Method to get the help file version.


### Resource URL
https://yourdomain.com/api/v1/cms/version/:option

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | No |
| Rate limited    | NO |

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **option** | <ul><li>required</li><li>string</li></ul> |

### Example Request

GET
https://yourdomain.com/api/v1/cms/version/shortversion

### Example Result

#### JSON Response

##### Guest
```json
{
  "msg": "Guests cannot view version information.",
  "error": false,
  "status": 403
}
```
##### Logged In
```json
{
  "shortVersion": "3.7.0",
  "error": false,
  "status": 200
}
```
```json
{
  "longVersion": "Joomla! 3.7.0 Stable [ Amani ] 25-April-2017 15:36 GMT",
  "error": false,
  "status": 200
}
```
```json
{
  "userAgent": "Mozilla/5.0 Joomla!/3.7.0 Framework/3.7",
  "error": false,
  "status": 200
}
```
```json
{
  "helpVersion": ".37",
  "error": false,
  "status": 200
}
```

#### Response Headers
```
{
  "server": "Apache/2.4.6",
  "content-type": "application/json",
  "date": "Wed, 03 May 2017 02:19:43 GMT",
  "connection": "Keep-Alive",
  "access-control-allow-origin": "https://getcapi.io",
  "content-length": "51",
  "keep-alive": "timeout=5, max=100"
}
```