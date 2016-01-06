---
node_id: 632
title: How do I optimize SugarCRM on Cloud Sites?
permalink: article/how-do-i-optimize-sugarcrm-on-cloud-sites
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-06-23 17:2415'
last_modified_by: kelly.holcomb
products: Cloud Sites
body_format: tinymce
---

**This guide is intended for advanced users.**

For optimization techniques of any web application, The Rackspace Cloud
highly recommends consulting the vendors of the application. However,
SugarCRM does have detailed documentation on their [Support
Wiki](http://www.sugarcrm.com/kb/index.php?title=Sugar_Support_Wiki "http://www.sugarcrm.com/kb/index.php?title=Sugar_Support_Wiki"),
some of which we have made available here.

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 Quick Guide](#Quick_Guide)                                        |
|     -   [1.1 .htaccess](#htaccess)                                       |
|     -   [1.2 config\_override.php](#config_overridephp)                  |
| -   [2 Developer Tools](#Developer_Tools)                                |
| -   [3 External Links](#External_Links)                                  |
+--------------------------------------------------------------------------+

Quick Guide
-----------

Below is the quick guide to modifying your SugarCRM configuration for
improved performance in the cloud.

### .htaccess

Add the following PHP configuration directives to your *.htaccess* file:

    php_value memory_limit 80M
    php_value post_max_size 75M
    php_value upload_max_filesize 75M
    php_value max_execution_time 601
    php_value timeout 601

The PHP5 section of your *.htaccess* should look something like the
following example when done:

    # PHP 5, Apache 1 and 2.
    <IfModule mod_php5.c>
    php_value magic_quotes_gpc 0
    php_value register_globals 0
    php_value session.auto_start 0
    php_value mbstring.http_input pass
    php_value mbstring.http_output pass
    php_value mbstring.encoding_translation 0
    php_value memory_limit 80M
    php_value post_max_size 75M
    php_value upload_max_filesize 75M
    php_value max_execution_time 601
    php_value timeout 601
    </IfModule>

### config\_override.php

**The below configuration options should improve the performance of your
SugarCRM installation, but may change the way some of the front-end
looks.** For a detailed explanation of the below configuration options,
please see [SugarCRM's Performance Tweaks
page](http://www.sugarcrm.com/wiki/index.php?title=Performance_Tweaks_for_Large_Systems "http://www.sugarcrm.com/wiki/index.php?title=Performance_Tweaks_for_Large_Systems").

Add the following SugarCRM configuration options to your
*config\_override.php* file:

    $sugar_config['disable_count_query'] = true;
    $sugar_config['disable_vcr'] = true;
    $sugar_config['hide_subpanels'] = true;
    $sugar_config['hide_subpanels_on_login'] = true;
    $sugar_config['save_query'] = 'populate_only';
    $sugar_config['verify_client_ip'] = false;

Developer Tools
---------------

The [SugarDev.net Developer
Tools](http://www.sugarforge.org/projects/sugardevtools/ "http://www.sugarforge.org/projects/sugardevtools/")
also provide some performance options you may find useful.

External Links
--------------

-   [SugarCRM Support
    Wiki](http://www.sugarcrm.com/wiki/index.php?title=Sugar_Support_Wiki "http://www.sugarcrm.com/wiki/index.php?title=Sugar_Support_Wiki")
-   [SugarCRM Support Wiki: Performance Tweaks for Large
    Systems](http://www.sugarcrm.com/kb/index.php?title=Performance_Tweaks_for_Large_Systems "http://www.sugarcrm.com/kb/index.php?title=Performance_Tweaks_for_Large_Systems")
-   [SugarDev.net Developer
    Tools](http://www.sugarforge.org/projects/sugardevtools/ "http://www.sugarforge.org/projects/sugardevtools/")


