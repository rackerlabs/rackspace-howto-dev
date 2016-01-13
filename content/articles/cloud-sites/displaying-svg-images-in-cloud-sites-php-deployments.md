---
node_id: 3837
title: Displaying SVG Images In Cloud Sites PHP Deployments
type: article
created_date: '2013-12-18 19:09:32'
created_by: bryon.farris
last_modified_date: '2013-12-19 21:1322'
last_modified_by: ross.diaz
products: Cloud Sites
body_format: tinymce
---

***Note: As of Wordpress 3.8, Wordpress employs an SVG logo for the
administration page logo, the following fix will also allow this image
to properly show.***

In order to properly show SVG image types within the Cloud Sites PHP
environment, the following line will need to be added to your .htaccess
file:

`AddType image/svg+xml svg`

This will tell the Apache instance the proper MIME type to use when
serving requests for SVG style image files.

For a very extensive list of what MIME Type Apache supports, please
review:\
[http://svn.apache.org/repos/asf/httpd/httpd/trunk/docs/conf/mime.types](http://svn.apache.org/repos/asf/httpd/httpd/trunk/docs/conf/mime.types)\
\
*Note: The following link may not be fully formatted correctly for the
.htaccess*

 

