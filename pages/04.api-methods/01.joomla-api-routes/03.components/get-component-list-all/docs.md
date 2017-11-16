---
title: 'GET component/list/all'
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

Returns list of all components.

>>> Requires core.edit permission on com_content component.

### Resource URL
https://yourdomain.com/api/v1/component/list/all

### Resource Information

| Option | Description |
| ------ | ----------- |
| Response formats   | JSON |
| Requires authentication | Yes - core.edit |
| Rate limited    | YES (token only)|

### Parameters

|  Name  |  Details  |  
|  :-----          |  :-----          |
|  **context** | <ul><li>required</li><li>string</li><li>"administrator","site"</li></ul> |

### Example Request

GET
https://yourdomain.com/api/v1/component/list/all

### Example Result

#### JSON Response

```json
{
  "components": [
    {
      "extension_id": "3",
      "package_id": "0",
      "name": "com_admin",
      "type": "component",
      "element": "com_admin",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_admin",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_ADMIN_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "help": "AdminModelHelp",
        "profile": "AdminModelProfile",
        "sysinfo": "AdminModelSysInfo"
      }
    },
    {
      "extension_id": "31",
      "package_id": "0",
      "name": "com_ajax",
      "type": "component",
      "element": "com_ajax",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_ajax",
        "type": "component",
        "creationDate": "August 2013",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.2.0",
        "description": "COM_AJAX_XML_DESCRIPTION",
        "group": "",
        "filename": "ajax"
      }
    },
    {
      "extension_id": "34",
      "package_id": "0",
      "name": "com_associations",
      "type": "component",
      "element": "com_associations",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_associations",
        "type": "component",
        "creationDate": "Januar 2017",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.7.0",
        "description": "COM_ASSOCIATIONS_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "association": "AssociationsModelAssociation",
        "associations": "AssociationsModelAssociations"
      }
    },
    {
      "extension_id": "4",
      "package_id": "0",
      "name": "com_banners",
      "type": "component",
      "element": "com_banners",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_banners",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_BANNERS_XML_DESCRIPTION",
        "group": "",
        "filename": "banners"
      },
      "tables": {
        "banner": "BannersTableBanner",
        "client": "BannersTableClient"
      },
      "models": {
        "banner": "BannersModelBanner",
        "banners": "BannersModelBanners",
        "client": "BannersModelClient",
        "clients": "BannersModelClients",
        "download": "BannersModelDownload",
        "tracks": "BannersModelTracks"
      }
    },
    {
      "extension_id": "5",
      "package_id": "0",
      "name": "com_cache",
      "type": "component",
      "element": "com_cache",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_cache",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CACHE_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "cache": "CacheModelCache"
      }
    },
    {
      "extension_id": "6",
      "package_id": "0",
      "name": "com_categories",
      "type": "component",
      "element": "com_categories",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_categories",
        "type": "component",
        "creationDate": "December 2007",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CATEGORIES_XML_DESCRIPTION",
        "group": ""
      },
      "tables": {
        "category": "CategoriesTableCategory"
      },
      "models": {
        "categories": "CategoriesModelCategories",
        "category": "CategoriesModelCategory"
      }
    },
    {
      "extension_id": "7",
      "package_id": "0",
      "name": "com_checkin",
      "type": "component",
      "element": "com_checkin",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_checkin",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CHECKIN_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "checkin": "CheckinModelCheckin"
      }
    },
    {
      "extension_id": "23",
      "package_id": "0",
      "name": "com_config",
      "type": "component",
      "element": "com_config",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_config",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CONFIG_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "application": "",
        "component": ""
      }
    },
    {
      "extension_id": "8",
      "package_id": "0",
      "name": "com_contact",
      "type": "component",
      "element": "com_contact",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_contact",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CONTACT_XML_DESCRIPTION",
        "group": "",
        "filename": "contact"
      },
      "tables": {
        "contact": "ContactTableContact"
      },
      "models": {
        "contact": "ContactModelContact",
        "contacts": "ContactModelContacts"
      }
    },
    {
      "extension_id": "22",
      "package_id": "0",
      "name": "com_content",
      "type": "component",
      "element": "com_content",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_content",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CONTENT_XML_DESCRIPTION",
        "group": "",
        "filename": "content"
      },
      "tables": {
        "featured": "ContentTableFeatured"
      },
      "models": {
        "article": "ContentModelArticle",
        "articles": "ContentModelArticles",
        "feature": "ContentModelFeature",
        "featured": "ContentModelFeatured"
      }
    },
    {
      "extension_id": "30",
      "package_id": "0",
      "name": "com_contenthistory",
      "type": "component",
      "element": "com_contenthistory",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_contenthistory",
        "type": "component",
        "creationDate": "May 2013",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.2.0",
        "description": "COM_CONTENTHISTORY_XML_DESCRIPTION",
        "group": "",
        "filename": "contenthistory"
      },
      "models": {
        "compare": "ContenthistoryModelCompare",
        "history": "ContenthistoryModelHistory",
        "preview": "ContenthistoryModelPreview"
      }
    },
    {
      "extension_id": "9",
      "package_id": "0",
      "name": "com_cpanel",
      "type": "component",
      "element": "com_cpanel",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_cpanel",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_CPANEL_XML_DESCRIPTION",
        "group": ""
      }
    },
    {
      "extension_id": "33",
      "package_id": "0",
      "name": "com_fields",
      "type": "component",
      "element": "com_fields",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_fields",
        "type": "component",
        "creationDate": "March 2016",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.7.0",
        "description": "COM_FIELDS_XML_DESCRIPTION",
        "group": "",
        "filename": "fields"
      },
      "tables": {
        "field": "FieldsTableField",
        "group": "FieldsTableGroup"
      },
      "models": {
        "field": "FieldsModelField",
        "fields": "FieldsModelFields",
        "group": "FieldsModelGroup",
        "groups": "FieldsModelGroups"
      }
    },
    {
      "extension_id": "27",
      "package_id": "0",
      "name": "com_finder",
      "type": "component",
      "element": "com_finder",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_finder",
        "type": "component",
        "creationDate": "August 2011",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_FINDER_XML_DESCRIPTION",
        "group": "",
        "filename": "finder"
      },
      "tables": {
        "filter": "FinderTableFilter",
        "link": "FinderTableLink",
        "map": "FinderTableMap"
      },
      "models": {
        "filter": "FinderModelFilter",
        "filters": "FinderModelFilters",
        "index": "FinderModelIndex",
        "indexer": "FinderModelIndexer",
        "maps": "FinderModelMaps",
        "statistics": "FinderModelStatistics"
      }
    },
    {
      "extension_id": "10015",
      "package_id": "10016",
      "name": "com_gantry5",
      "type": "component",
      "element": "com_gantry5",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_gantry5",
        "type": "component",
        "creationDate": "July  6, 2017",
        "author": "RocketTheme, LLC",
        "copyright": "(C) 2005 - 2017 RocketTheme, LLC. All rights reserved.",
        "authorEmail": "support@rockettheme.com",
        "authorUrl": "http:\/\/www.rockettheme.com",
        "version": "5.4.14",
        "description": "COM_GANTRY5_DESCRIPTION",
        "group": "",
        "filename": "gantry5"
      }
    },
    {
      "extension_id": "10",
      "package_id": "0",
      "name": "com_installer",
      "type": "component",
      "element": "com_installer",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_installer",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_INSTALLER_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "database": "InstallerModelDatabase",
        "discover": "InstallerModelDiscover",
        "extension": "InstallerModel",
        "install": "InstallerModelInstall",
        "languages": "InstallerModelLanguages",
        "manage": "InstallerModelManage",
        "update": "InstallerModelUpdate",
        "updatesites": "InstallerModelUpdatesites",
        "warnings": "InstallerModelWarnings"
      }
    },
    {
      "extension_id": "28",
      "package_id": "0",
      "name": "com_joomlaupdate",
      "type": "component",
      "element": "com_joomlaupdate",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_joomlaupdate",
        "type": "component",
        "creationDate": "February 2012",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.6.2",
        "description": "COM_JOOMLAUPDATE_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "default": "JoomlaupdateModelDefault"
      }
    },
    {
      "extension_id": "11",
      "package_id": "0",
      "name": "com_languages",
      "type": "component",
      "element": "com_languages",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_languages",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_LANGUAGES_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "installed": "LanguagesModelInstalled",
        "language": "LanguagesModelLanguage",
        "languages": "LanguagesModelLanguages",
        "override": "LanguagesModelOverride",
        "overrides": "LanguagesModelOverrides",
        "strings": "LanguagesModelStrings"
      }
    },
    {
      "extension_id": "12",
      "package_id": "0",
      "name": "com_login",
      "type": "component",
      "element": "com_login",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_login",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_LOGIN_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "login": "LoginModelLogin"
      }
    },
    {
      "extension_id": "1",
      "package_id": "0",
      "name": "com_mailto",
      "type": "component",
      "element": "com_mailto",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_mailto",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.\t",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_MAILTO_XML_DESCRIPTION",
        "group": "",
        "filename": "mailto"
      }
    },
    {
      "extension_id": "13",
      "package_id": "0",
      "name": "com_media",
      "type": "component",
      "element": "com_media",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_media",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_MEDIA_XML_DESCRIPTION",
        "group": "",
        "filename": "media"
      },
      "models": {
        "list": "MediaModelList",
        "manager": "MediaModelManager"
      }
    },
    {
      "extension_id": "14",
      "package_id": "0",
      "name": "com_menus",
      "type": "component",
      "element": "com_menus",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_menus",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_MENUS_XML_DESCRIPTION",
        "group": ""
      },
      "tables": {
        "menu": "MenusTableMenu"
      },
      "models": {
        "item": "MenusModelItem",
        "items": "MenusModelItems",
        "menu": "MenusModelMenu",
        "menus": "MenusModelMenus",
        "menutypes": "MenusModelMenutypes"
      }
    },
    {
      "extension_id": "15",
      "package_id": "0",
      "name": "com_messages",
      "type": "component",
      "element": "com_messages",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_messages",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_MESSAGES_XML_DESCRIPTION",
        "group": ""
      },
      "tables": {
        "message": "MessagesTableMessage"
      },
      "models": {
        "config": "MessagesModelConfig",
        "message": "MessagesModelMessage",
        "messages": "MessagesModelMessages"
      }
    },
    {
      "extension_id": "16",
      "package_id": "0",
      "name": "com_modules",
      "type": "component",
      "element": "com_modules",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_modules",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_MODULES_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "module": "ModulesModelModule",
        "modules": "ModulesModelModules",
        "positions": "ModulesModelPositions",
        "select": "ModulesModelSelect"
      }
    },
    {
      "extension_id": "17",
      "package_id": "0",
      "name": "com_newsfeeds",
      "type": "component",
      "element": "com_newsfeeds",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_newsfeeds",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_NEWSFEEDS_XML_DESCRIPTION",
        "group": "",
        "filename": "newsfeeds"
      },
      "tables": {
        "newsfeed": "NewsfeedsTableNewsfeed"
      },
      "models": {
        "newsfeed": "NewsfeedsModelNewsfeed",
        "newsfeeds": "NewsfeedsModelNewsfeeds"
      }
    },
    {
      "extension_id": "18",
      "package_id": "0",
      "name": "com_plugins",
      "type": "component",
      "element": "com_plugins",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_plugins",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_PLUGINS_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "plugin": "PluginsModelPlugin",
        "plugins": "PluginsModelPlugins"
      }
    },
    {
      "extension_id": "32",
      "package_id": "0",
      "name": "com_postinstall",
      "type": "component",
      "element": "com_postinstall",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_postinstall",
        "type": "component",
        "creationDate": "September 2013",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.2.0",
        "description": "COM_POSTINSTALL_XML_DESCRIPTION",
        "group": ""
      },
      "models": {
        "messages": "PostinstallModelMessages"
      }
    },
    {
      "extension_id": "24",
      "package_id": "0",
      "name": "com_redirect",
      "type": "component",
      "element": "com_redirect",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_redirect",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_REDIRECT_XML_DESCRIPTION",
        "group": ""
      },
      "tables": {
        "link": "RedirectTableLink"
      },
      "models": {
        "link": "RedirectModelLink",
        "links": "RedirectModelLinks"
      }
    },
    {
      "extension_id": "19",
      "package_id": "0",
      "name": "com_search",
      "type": "component",
      "element": "com_search",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_search",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_SEARCH_XML_DESCRIPTION",
        "group": "",
        "filename": "search"
      },
      "models": {
        "searches": "SearchModelSearches"
      }
    },
    {
      "extension_id": "10026",
      "package_id": "10034",
      "name": "com_services",
      "type": "component",
      "element": "com_services",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_services",
        "type": "component",
        "creationDate": "November 15, 2017",
        "author": "Steve Tsiopanos",
        "copyright": "Copyright (C) 2017 Annatech LLC. All rights reserved.",
        "authorEmail": "steve.tsiopanos@annatech.com",
        "authorUrl": "https:\/\/www.annatech.com",
        "version": "1.3.4",
        "description": "Manage our RESTful APIs which turn Joomla into a backend service provider for other enterprise applications and mobile devices. Developed by Steve Tsiopanos, Annatech LLC. Powered by Slim PHP Framework.",
        "group": "",
        "filename": "services"
      },
      "tables": {
        "token": "ServicesTableToken"
      },
      "models": {
        "slimphpframework": "ServicesModelSlimphpframework",
        "swaggerui": "ServicesModelSwaggerui",
        "token": "ServicesModelToken",
        "tokens": "ServicesModelTokens"
      }
    },
    {
      "extension_id": "29",
      "package_id": "0",
      "name": "com_tags",
      "type": "component",
      "element": "com_tags",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_tags",
        "type": "component",
        "creationDate": "December 2013",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.1.0",
        "description": "COM_TAGS_XML_DESCRIPTION",
        "group": "",
        "filename": "tags"
      },
      "tables": {
        "tag": "TagsTableTag"
      },
      "models": {
        "tag": "TagsModelTag",
        "tags": "TagsModelTags"
      }
    },
    {
      "extension_id": "20",
      "package_id": "0",
      "name": "com_templates",
      "type": "component",
      "element": "com_templates",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_templates",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_TEMPLATES_XML_DESCRIPTION",
        "group": ""
      },
      "tables": {
        "style": "TemplatesTableStyle"
      },
      "models": {
        "style": "TemplatesModelStyle",
        "styles": "TemplatesModelStyles",
        "template": "TemplatesModelTemplate",
        "templates": "TemplatesModelTemplates"
      }
    },
    {
      "extension_id": "25",
      "package_id": "0",
      "name": "com_users",
      "type": "component",
      "element": "com_users",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_users",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_USERS_XML_DESCRIPTION",
        "group": "",
        "filename": "users"
      },
      "tables": {
        "note": "UsersTableNote"
      },
      "models": {
        "debuggroup": "UsersModelDebuggroup",
        "debuguser": "UsersModelDebugUser",
        "group": "UsersModelGroup",
        "groups": "UsersModelGroups",
        "level": "UsersModelLevel",
        "levels": "UsersModelLevels",
        "mail": "UsersModelMail",
        "note": "UsersModelNote",
        "notes": "UsersModelNotes",
        "user": "UsersModelUser",
        "users": "UsersModelUsers"
      }
    },
    {
      "extension_id": "2",
      "package_id": "0",
      "name": "com_wrapper",
      "type": "component",
      "element": "com_wrapper",
      "enabled": "1",
      "manifest_cache": {
        "name": "com_wrapper",
        "type": "component",
        "creationDate": "April 2006",
        "author": "Joomla! Project",
        "copyright": "(C) 2005 - 2017 Open Source Matters. All rights reserved.\n\t",
        "authorEmail": "admin@joomla.org",
        "authorUrl": "www.joomla.org",
        "version": "3.0.0",
        "description": "COM_WRAPPER_XML_DESCRIPTION",
        "group": "",
        "filename": "wrapper"
      }
    }
  ],
  "error": false,
  "status": 200
}
```

#### Response Headers
```
HTTP/1.1 200 OK
Date: Thu, 16 Nov 2017 12:19:52 GMT
Server: Apache/2.4.6
X-Powered-By: PHP/7.0.25
Joomla-Sessionid: 3aa0enpsfonvgnbjpuhuss5ufv
Set-Cookie: d01caba7bc5c20bda9610d1fdd9da85=3ja0enpvgonvgnbjpuhumb5uf4; path=/; HttpOnly
Set-Cookie: joomla_user_state=logged_in; path=/; HttpOnly
Access-Control-Allow-Headers: X-Requested-With, Origin, Content-Type, token, dlid, nonce, Authorization
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, OPTIONS
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/json

```