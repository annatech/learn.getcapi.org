---
title: slim
taxonomy:
    category:
        - docs
---

# Slim Framework

[![Build Status](https://travis-ci.org/slimphp/Slim.svg?branch=master)](https://travis-ci.org/slimphp/Slim)

Slim is a PHP micro framework that helps you quickly write simple yet powerful web applications and APIs.
Slim is easy to use for both beginners and professionals. Slim favors cleanliness over terseness and common cases
over edge cases. Its interface is simple, intuitive, and extensively documented â€” both online and in the code itself.
Thank you for choosing the Slim Framework for your next project. I think you're going to love it.

## Features

* Powerful router
    * Standard and custom HTTP methods
    * Route parameters with wildcards and conditions
    * Route redirect, halt, and pass
    * Route middleware
* Resource Locator and DI container
* Template rendering with custom views
* Flash messages
* Encrypt cookie data
* HTTP caching
* Logging with custom log writers
* Error handling and debugging
* Middleware and hook architecture
* Simple configuration

## Getting Started

### Install

You may install the Slim Framework with Composer (recommended) or manually.

[Read how to install Slim](http://docs.slimframework.com/#Installation)

### System Requirements

You need **PHP >= 5.3.0**. If you use encrypted cookies, you'll also need the `mcrypt` extension.

### Hello World Tutorial

Instantiate a Slim application:
```php
$app = new \Slim\Slim();
```
Define a HTTP GET route:
```php
$app->get('/hello/:name', function ($name) {
    echo "Hello, $name";
});
```
Run the Slim application:
```php
$app->run();
```
### Setup your web server

#### Apache

Ensure the `.htaccess` and `index.php` files are in the same public-accessible directory. The `.htaccess` file
should contain this code:
```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ index.php [QSA,L]
```
Additionally, make sure your virtual host is configured with the AllowOverride option so that the .htaccess rewrite rules can be used:
```
AllowOverride All
```
#### Nginx

The nginx configuration file should contain this code (along with other settings you may need) in your `location` block:
```
try_files $uri $uri/ /index.php?$args;
```
This assumes that Slim's `index.php` is in the root folder of your project (www root).

#### HipHop Virtual Machine for PHP

Your HipHop Virtual Machine configuration file should contain this code (along with other settings you may need).
Be sure you change the `ServerRoot` setting to point to your Slim app's document root directory.
```
Server {
    SourceRoot = /path/to/public/directory
}

ServerVariables {
    SCRIPT_NAME = /index.php
}

VirtualHost {
    * {
        Pattern = .*
        RewriteRules {
                * {
                        pattern = ^(.*)$
                        to = index.php/$1
                        qsa = true
                }
        }
    }
}
```
#### lighttpd ####

Your lighttpd configuration file should contain this code (along with other settings you may need). This code requires
lighttpd >= 1.4.24.
```
url.rewrite-if-not-file = ("(.*)" => "/index.php/$0")
```
This assumes that Slim's `index.php` is in the root folder of your project (www root).

#### IIS

Ensure the `Web.config` and `index.php` files are in the same public-accessible directory. The `Web.config` file should contain this code:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <system.webServer>
        <rewrite>
            <rules>
                <rule name="slim" patternSyntax="Wildcard">
                    <match url="*" />
                    <conditions>
                        <add input="{REQUEST_FILENAME}" matchType="IsFile" negate="true" />
                        <add input="{REQUEST_FILENAME}" matchType="IsDirectory" negate="true" />
                    </conditions>
                    <action type="Rewrite" url="index.php" />
                </rule>
            </rules>
        </rewrite>
    </system.webServer>
</configuration>
```
#### Google App Engine

Two steps are required to successfully run your Slim application on Google App Engine. First, ensure the `app.yaml` file includes a default handler to `index.php`:
```
application: your-app-name
version: 1
runtime: php
api_version: 1

handlers:
# ...
- url: /.*
  script: public_html/index.php
```
Next, edit your `index.php` file so Slim knows about the incoming URI:
```php
$app = new Slim();

// Google App Engine doesn't set $_SERVER['PATH_INFO']
$app->environment['PATH_INFO'] = $_SERVER['REQUEST_URI'];

// ...
$app->run();
```
   
## Documentation

<http://docs.slimframework.com/>

## How to Contribute


*NOTE: We are only accepting security fixes for Slim 2 (master branch). All development is concentrated on Slim 3 which is on the develop branch.*


### Pull Requests

1. Fork the Slim Framework repository
2. Create a new branch for each feature or improvement
3. Send a pull request from each feature branch to the **develop** branch

It is very important to separate new features or improvements into separate feature branches, and to send a pull
request for each branch. This allows me to review and pull in new features or improvements individually.

### Style Guide

All pull requests must adhere to the [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) standard.

### Unit Testing

All pull requests must be accompanied by passing unit tests and complete code coverage. The Slim Framework uses
`phpunit` for testing.

[Learn about PHPUnit](https://github.com/sebastianbergmann/phpunit/)

## Community

### Forum and Knowledgebase

Visit Slim's official forum and knowledge base at <http://help.slimframework.com> where you can find announcements,
chat with fellow Slim users, ask questions, help others, or show off your cool Slim Framework apps.

### Twitter

Follow [@slimphp](http://www.twitter.com/slimphp) on Twitter to receive news and updates about the framework.

## Author

The Slim Framework is created and maintained by [Josh Lockhart](http://www.joshlockhart.com). Josh is a senior
web developer at [New Media Campaigns](http://www.newmediacampaigns.com/). Josh also created and maintains
[PHP: The Right Way](http://www.phptherightway.com/), a popular movement in the PHP community to introduce new
PHP programmers to best practices and good information.

## License

The Slim Framework is released under the MIT public license.

<https://github.com/slimphp/Slim/blob/master/LICENSE>

# Slim Framework Extras

This repository contains extra resources that complement the Slim Framework, a PHP micro framework that helps
you quickly write simple yet powerful web applications.

## Custom Views

This repository contains custom views for your Slim Framework applications. Custom views let you easily
use popular third-party templating frameworks, like [Twig](http://twig.sensiolabs.org/) or
[Smarty](http://www.smarty.net/), with your Slim Framework application.

* Smarty
* Twig
* Mustache
* Haml
* Haanga
* Blitz
* Dwoo
* Sugar
* Savant
* Rain
* H2o

This example demonstrates how to use the custom Twig view in your Slim Framework application:

    <?php
    // Setup custom Twig view
    $twigView = new \Slim\Extras\Views\Twig();

    // Instantiate application
    $app = new \Slim\Slim(array(
        'view' => $twigView
    ));

This example assumes you are autoloading dependencies using [Composer](http://getcomposer.org/). If you are not
using Composer, you must manually `require` the custom view class before instantiating it.

Read the [Slim Framework documentation](http://docs.slimframework.com/pages/view-custom/) to learn how to write
your own custom view.

## Middleware

This repository also contains middleware for your Slim Framework application. This
example demonstrates how to apply HTTP basic authentication to a Slim Framework application:

    <?php
    $app = new \Slim\Slim();
    $app->add(new \Slim\Extras\Middleware\HttpBasicAuth('username', 'password'));

This example assumes you are autoloading dependencies using [Composer](http://getcomposer.org/). If you are not
using Composer, you must manually `require` the custom middleware class before instantiating it.

## Log Writers

This repository also contains custom log writers for your Slim Framwork application. This example
demonstrates how to use the custom `DateTimeLogWriter` to write rolling log files from your Slim Framework application:

    <?php
    $app = new \Slim\Slim(array(
        'log.writer' => new \Slim\Extras\Log\DateTimeFileWriter(array(
            'path' => './logs',
            'name_format' => 'Y-m-d',
            'message_format' => '%label% - %date% - %message%'
        ))
    ));

This example assumes you are autoloading dependencies using [Composer](http://getcomposer.org/). If you are not
using Composer, you must manually `require` the log writer class before instantiating it.

## Author

The Slim Framework is created and maintained by [Josh Lockhart](https://www.joshlockhart.com). Josh is a senior
web developer at [New Media Campaigns](http://www.newmediacampaigns.com/). Josh also created and maintains
[PHP: The Right Way](http://www.phptherightway.com/), a popular movement in the PHP community to introduce new
PHP programmers to best practices and good information.

The Slim Framework Extras repository is maintained by [Andrew Smith](https://github.com/silentworks).

## License

The Slim Framework is released under the MIT public license.

<http://www.slimframework.com/license>