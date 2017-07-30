---
title: 'Services Libraries'
taxonomy:
    category:
        - docs
---

These libraries may normally be added to Joomla via Composer, but a recent change since Joomla 3.4 has broken the functionality of the vendor directory autoloader.php. Since this is actually part of a longer term process to eventually fully support Composer installation of Joomla extentions, but is not yet fully realized, the requisite libraries to allow Slim PHP framework autoloading within Joomla have been included here to ensure maximum compatibility across all Joomla 3.4.x installations.
     
_Note that it is still possible to make use of the Slim framework by configuring composer for Joomla 3.4.x._