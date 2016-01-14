---
node_id: 307
title: Connecting to CloudFiles
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2013-12-30 20:3001'
last_modified_by: kyle.laffoon
product: Cloud Files
body_format: tinymce
---

Rackspace Cloud Servers can connect to Cloud Files without bandwidth
charges when the server and the Cloud Files account are in the same data
center. This connection is made by using the internal IP address that
your server comes with on the internal Rackspace network, ServiceNet.

If you are not familiar with Cloud Files, see the product information at
[www.rackspace.com/cloud/cloud\_hosting\_products/files/](http://www.rackspace.com/cloud/cloud_hosting_products/files/).

To view or download the Cloud Files API documentation, go to
docs.rackspace.com/api/. You can also access the documentation and some
code samples from docs.rackspace.com/sdks/guide/content/intro.html. Code
samples are available for PHP, Python, and Java.

### How to Connect

To connect, you must use the internal network host name. The host name
is the Cloud Files storage URL with **snet-** prepended to it. Be aware
that even though you are not chared for bandwidth when you use
ServiceNet to connect, you are still charged for requests and storage.

You can locate your Cloud Server data center in the following ways:

-   [Cloud Control Panel](https://mycloud.rackspace.com/) &mdash;On the main
    Cloud Files page in the Control Panel, locate your Cloud Files data
    center in the **Region** column.
-   Through the API&mdash; Your Cloud Files data center is located in the
    storage URL that is returned when you authenticate to Cloud Files.
    For more information, see [Retrieving the Authentication
    Token](http://docs.rackspace.com/cas/api/v1.0/autoscale-devguide/content/Retrieving_Auth_Token.html).

 

