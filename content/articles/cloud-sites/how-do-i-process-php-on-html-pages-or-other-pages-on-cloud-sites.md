---
node_id: 637
title: How Do I Process PHP On HTML Pages Or Other Pages on Cloud Sites?
permalink: article/how-do-i-process-php-on-html-pages-or-other-pages-on-cloud-sites
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-06-23 20:2322'
last_modified_by: kelly.holcomb
products: Cloud Sites
body_format: tinymce
---

You can cause PHP to be processed on HTM and HTML pages by setting those
extensions to be served by the PHP handler. You can enable PHP
processing on **.htm** and **.html** in your .htaccess with the
following directives:

~~~~ {.p1}
AddHandler application/x-httpd-php php htm html
AddType text/html php
~~~~

Following the above example, if you wanted to process PHP on files with
the extension **.test**, you could do so using:

~~~~ {.p1}
AddHandler application/x-httpd-php php test
AddType text/html php
~~~~

You can find more information on *AddHandler* and *AddType* at [Apache's
website](http://httpd.apache.org/docs/2.0/mod/mod_mime.html).

**Note**: We recommend using just the PHP extension for PHP pages.

