---
title: 'GET user/sessions'
taxonomy:
    category:
        - docs
---

Returns list of all current Joomla user sessions for all users.

>>> Currently, this method will only return a user sessions object if the request is made from an authenticated session by a Joomla user who is a Super Admin. This limits the scope of use to access where a persistent session can be maintained with the website on which cAPI is installed. In the future, token-base access will be implemented to allow any remote system to place this request.

### Resource URL
https://yourdomain.com/api/v1/user/sessions

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | YES - Only Super Admins may access this method. |
| Rate limited    | NO |

### Parameters

Method does not accept parameters.


### Example Request

GET
https://yourdomain.com/api/v1/user/sessions

### Example Result

>>>>> Responses have been cleansed to protect private session data.

#### JSON Response

```json
{
  "msg": [
    {
      "session_id": "09330c9f0999649789391191fab99269",
      "client_id": "0",
      "guest": "1",
      "time": "1445780780",
      "data": "__default|a:9:{s:15:\"session.counter\";i:1;s:19:\"session.timer.start\";i:1445780779;s:18:\"session.timer.last\";i:1445780779;s:17:\"session.timer.now\";i:1445780779;s:22:\"session.client.browser\";s:105:\"Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/37.0.2062.120 Safari\/537.36\";s:8:\"registry\";O:24:\"Joomla\\Registry\\Registry\":2:{s:7:\"\\0\\0\\0data\";O:8:\"stdClass\":0:{}s:9:\"separator\";s:1:\".\";}s:4:\"user\";O:5:\"JUser\":29:{s:9:\"\\0\\0\\0isRoot\";b:0;s:2:\"id\";i:0;s:4:\"name\";N;s:8:\"username\";N;s:5:\"email\";N;s:8:\"password\";N;s:14:\"password_clear\";s:0:\"\";s:5:\"block\";N;s:9:\"sendEmail\";i:0;s:12:\"registerDate\";N;s:13:\"lastvisitDate\";N;s:10:\"activation\";N;s:6:\"params\";N;s:6:\"groups\";a:1:{i:0;s:1:\"9\";}s:5:\"guest\";i:1;s:13:\"lastResetTime\";N;s:10:\"resetCount\";N;s:12:\"requireReset\";N;s:10:\"\\0\\0\\0_params\";O:24:\"Joomla\\Registry\\Registry\":2:{s:7:\"\\0\\0\\0data\";O:8:\"stdClass\":0:{}s:9:\"separator\";s:1:\".\";}s:14:\"\\0\\0\\0_authGroups\";a:2:{i:0;i:1;i:1;i:9;}s:14:\"\\0\\0\\0_authLevels\";a:4:{i:0;i:99;i:99;i:99;i:99;i:99;i:99;i:99;}s:15:\"\\0\\0\\0_authActions\";N;s:12:\"\\0\\0\\0_errorMsg\";N;s:13:\"\\0\\0\\0userHelper\";O:18:\"JUserWrapperHelper\":0:{}s:10:\"\\0\\0\\0_errors\";a:0:{}s:3:\"aid\";i:0;}s:13:\"session.token\";s:32:\"99999d9b716999eb369972b9945be999\";s:19:\"eo_piwik_visitor_id\";s:16:\"d9f9096989c9a999\";}",
      "userid": "0",
      "username": ""
    },
      {
      "session_id": "f188888888ffa8fd9f777777779a1f99",
      "client_id": "1",
      "guest": "0",
      "time": "1445783987",
      "data": "__default|a:8:{s:15:\"session.counter\";i:6;s:19:\"session.timer.start\";i:1445783933;s:18:\"session.timer.last\";i:1445783975;s:17:\"session.timer.now\";i:1445783976;s:22:\"session.client.browser\";s:116:\"Mozilla\/5.0 (Macintosh; Intel Mac OS X 10_11_1) AppleWebKit\/601.2.7 (KHTML, like Gecko) Version\/9.0.1 Safari\/601.2.7\";s:8:\"registry\";O:24:\"Joomla\\Registry\\Registry\":2:{s:7:\"\\0\\0\\0data\";O:8:\"stdClass\":2:{s:11:\"application\";O:8:\"stdClass\":1:{s:4:\"lang\";s:5:\"en-GB\";}s:13:\"com_installer\";O:8:\"stdClass\":2:{s:7:\"message\";s:0:\"\";s:17:\"extension_message\";s:0:\"\";}}s:9:\"separator\";s:1:\".\";}s:4:\"user\";O:5:\"JUser\":29:{s:9:\"\\0\\0\\0isRoot\";b:1;s:2:\"id\";s:2:\"43\";s:4:\"name\";s:15:\"Steve Tsiopanos\";s:8:\"username\";s:15:\"steve\";s:5:\"email\";s:21:\"stevetsi@annatech.com\";s:8:\"password\";s:60:\"******************************\";s:14:\"password_clear\";s:0:\"\";s:5:\"block\";s:1:\"0\";s:9:\"sendEmail\";s:1:\"1\";s:12:\"registerDate\";s:19:\"2015-01-01 20:06:58\";s:13:\"lastvisitDate\";s:19:\"2015-10-25 11:32:07\";s:10:\"activation\";s:0:\"\";s:6:\"params\";s:174:\"{\"admin_language\":\"en-GB\",\"language\":\"en-GB\",\"editor\":\"rokpad\",\"helpsite\":\"\",\"timezone\":\"\",\"admin_style\":\"\",\"update_cache_list\":1,\"auth_type\":\"LDAP\",\"auth_domain\":\"Annatech\"}\";s:6:\"groups\";a:8:{i:2;s:1:\"2\";i:8;s:1:\"8\";i:43;s:2:\"44\";i:45;s:2:\"46\";i:99;s:2:\"99\";i:99;s:2:\"99\";i:99;s:2:\"99\";i:99;s:2:\"99\";}s:5:\"guest\";i:0;s:13:\"lastResetTime\";s:19:\"0000-00-00 00:00:00\";s:10:\"resetCount\";s:1:\"0\";s:12:\"requireReset\";s:1:\"0\";s:10:\"\\0\\0\\0_params\";O:24:\"Joomla\\Registry\\Registry\":2:{s:7:\"\\0\\0\\0data\";O:8:\"stdClass\":9:{s:14:\"admin_language\";s:5:\"en-GB\";s:8:\"language\";s:5:\"en-GB\";s:6:\"editor\";s:6:\"rokpad\";s:8:\"helpsite\";s:0:\"\";s:8:\"timezone\";s:0:\"\";s:11:\"admin_style\";s:0:\"\";s:17:\"update_cache_list\";i:1;s:9:\"auth_type\";s:4:\"LDAP\";s:11:\"auth_domain\";s:8:\"Annatech\";}s:9:\"separator\";s:1:\".\";}s:14:\"\\0\\0\\0_authGroups\";a:99:{i:0;i:1;i:1;i:2;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:11;i:45;i:16;i:99;i:21;i:999;i:26;i:99;}s:14:\"\\0\\0\\0_authLevels\";a:99:{i:0;i:1;i:1;i:1;i:2;i:2;i:3;i:3;i:4;i:4;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;i:99;}s:99:\"\\0\\0\\0_authActions\";N;s:12:\"\\0\\0\\0_errorMsg\";N;s:13:\"\\0\\0\\0userHelper\";O:18:\"JUserWrapperHelper\":0:{}s:10:\"\\0\\0\\0_errors\";a:0:{}s:3:\"aid\";i:0;s:6:\"otpKey\";s:0:\"\";s:4:\"otep\";s:0:\"\";s:3:\"gid\";i:1000;}s:13:\"session.token\";s:32:\"f99999821d5f999991e82d7ba44cf77b\";}__koowa|a:3:{s:10:\"__metadata\";a:2:{s:5:\"timer\";a:3:{s:5:\"start\";i:1445783934;s:4:\"last\";i:1445783937;s:3:\"now\";i:1445783975;}s:5:\"token\";s:40:\"d45c619888888888d02fb9488888888459348955\";}s:11:\"__attribute\";a:1:{s:4:\"user\";a:12:{s:2:\"id\";s:2:\"99\";s:5:\"email\";s:21:\"stevetsi@annatech.com\";s:4:\"name\";s:15:\"Steve Tsiopanos\";s:8:\"username\";s:15:\"steve\";s:8:\"password\";s:60:\"*****************************\";s:4:\"salt\";s:0:\"\";s:9:\"authentic\";b:1;s:7:\"enabled\";b:1;s:7:\"expired\";b:1;s:10:\"attributes\";a:9:{s:14:\"admin_language\";s:5:\"en-GB\";s:8:\"language\";s:5:\"en-GB\";s:6:\"editor\";s:6:\"rokpad\";s:8:\"helpsite\";s:0:\"\";s:8:\"timezone\";s:0:\"\";s:11:\"admin_style\";s:0:\"\";s:17:\"update_cache_list\";i:1;s:9:\"auth_type\";s:4:\"LDAP\";s:11:\"auth_domain\";s:8:\"Annatech\";}s:5:\"roles\";a:0:{}s:6:\"groups\";a:0:{}}}s:9:\"__message\";a:0:{}}__wf|a:1:{s:13:\"session.token\";s:32:\"477777778e0943028888888842455555\";}",
      "userid": "99",
      "username": "steve"
    }
  ],
  "error": false,
  "status": 200
}
```
#### Response Headers
```
HTTP/1.1 200 OK
Date: Sun, 25 Oct 2015 14:40:02 GMT
Server: Apache
X-Powered-By: PHP/5.4.39
Access-Control-Allow-Origin: *
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce
Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=50
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json
```