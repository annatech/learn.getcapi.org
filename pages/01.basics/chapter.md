---
title: 'Getting Started'
metadata:
    keywords: 'php, rest, api, joomla, webservices'
    description: 'REST API for Joomla - Powered by Slim micro-framework - cAPI is an extensible platform for building robust RESTful web services powered by the Joomla CMS.'
taxonomy:
    category:
        - docs
---

### Chapter 1

# Getting Started
cAPI is an extensible platform for building robust REST web services with the Joomla CMS. <span class="fa fa-arrow-right"></span> cAPI Core v<span id="getversion"></span> [released!](https://www.annatech.com/capi-core.html)

*** 100% *** GPL Open Source - The software is yours to keep, _forever_   <span class="fa fa-heart"></span> !

*** $150 annual *** subscription gets you *** one year*** of upgrades and updates to the *** entire cAPI Core Package ***,  including the Control Panel and all current / new Joomla & Slim API methods.

<div style="text-align:center;"><a href="https://www.annatech.com/signup/get-started-with-joomla-restful-web-services.html"><i class="fa fa-cart-arrow-down fa-4x"></i></a></div>
### [&nbsp;&nbsp;Ready to Buy?](https://www.annatech.com/signup/get-started-with-joomla-restful-web-services.html)

Now listed in the Joomla! Extensions Directory.
[![](capi-logo-v2-333333-128.png)](https://extensions.joomla.org/extensions/extension/capi-core-rest-api)

[![](joomla-extensions-developer.png)](https://extensions.joomla.org/profile/profile/details/293249/)

<script type="text/javascript">
    jQuery(document).ready(function(){
        var request= "https://www.annatech.com/api/v1/slim/swagger";
        jQuery.ajax({
            url: request,
            type: "GET",
            success: function (result) {             
                jQuery( "#getversion" ).append(result.info.version).html;
            },
            error: function (jqXHR, textStatus, errorThrown) {
                jQuery( "#getversion" ).append('1.x').html;
            },
            timeout: 120000
        });
    });
    </script>
