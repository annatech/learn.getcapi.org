---
title: Overview
taxonomy:
    category:
        - docs
---

##Why build a Joomla RESTful API?##

It's no secret that platform-agnositic web services are taking over the internet and that RESTful APIs are at the forefront of this communications revolution. As a CMS, Joomla nestles itself comfortably between the ease of Wordpress and power of Drupal but has recently lagged behind them both in the realm of JSON-based RESTful APIs.

Simply having access to a wealth of frameworks does not relieve devlopers from the hard work of building tokenization, access-control, api rate-throttling or even the underlying content management system. The end-result still needs to be a fully realized product like, for example, a website driving a mobile app or a core middleware service joined to a corporate domain. The end-user needs more than just a framework and the developer can build faster if all the core components are complete.

cAPI was developed to provide Joomla a ready-to-deploy, natively-compatible yet code-independent platform for building RESTful web services of any complexity. 

##What is cAPI?##

Code named "Constant API", cAPI is the fantastic result of an effort to mesh the [Slim micro-framework](http://) with the Joomla Framework / CMS. Once that goal was accomplished, it soon became obvious that just built a Joomla RESTful API was only the beginning! By leveraging Joomla's advanced "pluggable" architecture and robust ACL, cAPI can transform your website into a true middleware service for anything ranging from SQL servers, MongoDB servers and even Microsoft's Active Directory (think of the SSO possibilities!). 

##How does it work?##

cAPI injects the Slim micro-framework into the Joomla application instance, allowing for service route plugins to be built at any level of the event stack. But that's only the beginning! 

A Services Control Panel manages the creation of access tokens, Slim framework parameters and API rate limitation rules. This allows an administrator to create tokens mapped to specific Joomla users who in turn are assigned unique group permissions using Joomla ACL.

The service routes are built into Joomla plugins which can be enabled / disabled or assigned access permissions individually. This opens the door for development of feature expansions to the core cAPI services to expose 3rd party Joomla extensions, database querying or even remote LDAP as RESTful JSON APIs. 