---
title: capi
published: true
taxonomy:
    category:
        - docs
---

#### Overview

Experimental library currently implemented for secure AJAX form field update of Download ID (required by Akeeba Release Systems to provide Joomla Updater functionality).

#### Code

>>>>> This library contains a PHP function which checks to see if critical cAPI plugins have been enabled and alerts the user when first visiting the Options page for the Services Control Panel.

The complete code for this function is included below for educational purposes.

``` php
	/**
    * @return string
    */
    protected function getInactiveCapiPlugins(){
        $disabledPlugins = array();
        $servicesPlugins = array(
            'joomla'                =>  'cAPI - Services Joomla Plugin\n',
            'slim'                  =>  'cAPI - Services Slim Configuration Plugin\n',
            'rest'                  =>  'cAPI - Services REST Plugin\n',
            'slimjsonapiview'       =>  'cAPI - Slim JSON API View Plugin\n',
            'slimjsonapimiddleware' =>  'cAPI - Slim JSON API Middleware Plugin\n'
        );

        $i = 0;
        foreach ($servicesPlugins as $k => $v) {
            if(JPluginHelper::isEnabled('services', $k) == ''){
                $disabledPlugins[$i] = $v;
                $i++;
            }
        }

        if($i >0) {
            $disabledPlugins = implode('', $disabledPlugins);
            $disabledPluginsString = "***IMPORTANT***" . '\n\n' . "The following plugins still need to be enabled:" . '\n\n' . $disabledPlugins;
            return $disabledPluginsString;
        }
        return false;
    }
```