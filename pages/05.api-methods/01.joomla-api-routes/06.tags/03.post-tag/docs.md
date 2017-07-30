---
title: 'POST tag'
published: false
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

Create new Joomla content via POST

>>>>> TODO: Upcoming versions will include ability to automatically check for base64 endcoded content. This will faciliate passing content with special characters to the web service.

### Resource URL
https://yourdomain.com/api/v1/content/create

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes, session-based or custom header token |
| Rate limited    | YES |

### Request Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **title** | <ul><li>required</li></ul> |
|  **alias** | <ul><li>optional</li>alpha-numeric, no spaces</ul> |
|  **introtext** | <ul><li>required</li></ul> |
|  **fulltext** | <ul><li>required</li></ul> |
|  **catid** | <ul><li>required</li></ul> |
|  **created_by_alias** | <ul><li>optional</li></ul> |
|  **state** | <ul><li>required</li></ul> |
|  **access** | <ul><li>required</li></ul> |
|  **robots** | <ul><li>optional</li></ul> |
|  **author** | <ul><li>optional</li></ul> |
|  **rights** | <ul><li>optional</li></ul> |
|  **xreference** | <ul><li>optional</li></ul> |
|  **language** | <ul>*, en-GB or other language code<li>required</li></ul> |



### Example Request

>>>> You will need to character-encode your input to retain spaces and ensure special characters are not processed.

```
POST https://yourdomain.com/api/v1/content/create
?title=New Article Title
&introtext=Short introduction for your article.
&fulltext=This is the main content of your article.
&catid=7
&created_by_alias=
&state=1
&access=1
&robots=
&author=
&rights=
&xreference=
&language=en-GB
```

### Example Result

#### JSON Response

```json
{
	"msg":" Created: New Article Title",
	"error": false, 
	"status": 200
}
```
#### Response Headers

>>>>> The following response headers follow a successful article posting when using token authentication via custom header. Note the Rate Limitation headers which are included be cause a token authenticated this session.

```
HTTP/1.1 200 OK
Date: Sun, 25 Oct 2015 21:57:50 GMT
Server: Apache/2.2.15
X-Powered-By: PHP/5.4.45
Joomla-Sessionid: 3o993p9k9tf9cd99k99999q4p6
X-Rate-Calls-Remaining: 0
X-Rate-Limit-Limit: 0
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: origin, x-requested-with, content-type, token
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Connection: close
Transfer-Encoding: chunked
Content-Type: application/json
```