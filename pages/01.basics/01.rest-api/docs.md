---
title: 'REST API'
published: true
taxonomy:
    category:
        - docs
---

### REST APIs
The REST APIs provide programmatic access to read and write data to your Joomla web application. Create pages, managed users, build SSO and more. The REST API identifies Joomla applications and users using both basic user / password authentication or API tokens; responses are available in JSON.

[Click here to access our Methods documentation.](../../api-methods)

### Latest Updates
Visit our changelog for details on our latest update for [cAPI v1.3.1](../../changelog/version-1-3-1).

#### Token Management API
As of version v1.2.5, cAPI exposed a collection of service routes to allow complete remote management of access tokens.
* GET /token/{token} Token authentication
* GET /token/manage/all Get all tokens
* GET /token/manage/ Get tokens by current user session
* POST /token/manage/ Create token
* GET /token/manage/{type}/{value} Get token(s) by userid, username, email or token
* POST /token/manage/userid/{userid} Create token by user ID
* DELETE /token/manage/tokenid/{tokenid} Delete token by ID

Check out our Swagger UI documentation for Token methods here:
[https://demo1.getcapi.io/api-docs#!/Token](https://demo1.getcapi.io/api-docs#!/Token)

#### Authentication
cAPI now supports either standard Joomla user authentication or token authentication. The Services Control Panel allows for creation of tokens on a per-user basis (or even multiple tokens per Joomla user).  Note that token authentication is required for some routes and to allow granular control over access parameters.

#### Rate Limiting
cAPI now allows the end user to configure the Slim micro-framework parameters and even include a threshold for the API rate-limiting functionality (currently based on requests-per-minute). It provides live feedback on the state of the API rate threshold within the response header.

#### Feedback and next steps
If you find any issues with any version of the API, please use our forums or contact page to send your feedback.