---
node_id: 307
title: Connecting to CloudFiles
type: article
created_date: '2011-03-16'
created_by: Rackspace Support
last_modified_date: '2013-12-30'
last_modified_by: Kyle Laffoon
product: Cloud Files
body_format: tinymce
---

[](){#Introduction}<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">Rackspace
Cloud Servers can connect to Cloud Files without bandwidth charges when
the server and the Cloud Files account are in the same data center. This
connection is made by using the internal IP address that your server
comes with on the internal Rackspace network, ServiceNet.</span>

<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">If
you are not familiar with Cloud Files, see the product information
at</span> [<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial;">www.rackspace.com/cloud/cloud\_hosting\_products/files/</span>](http://www.rackspace.com/cloud/cloud_hosting_products/files/)<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial;">.</span>

<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">To
view or download the Cloud Files API documentation, go to </span><span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #c50022;">docs.rackspace.com/api/</span><span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">.
You can also access the documentation and some code samples from
</span><span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #c50022;">docs.rackspace.com/sdks/guide/content/intro.html</span><span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">.
Code samples are available for PHP, Python, and Java.</span>

[](){#Connection_Information}

### <span class="mw-headline">How to Connect</span>

<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">To
connect, you must use the internal network host name. The host name is
the Cloud Files storage URL with **snet-** prepended to it. Be aware
that even though you are not chared for bandwidth when you use
ServiceNet to connect, you are still charged for requests and
storage.</span>

<span
style="font-size: 12.0pt; mso-bidi-font-family: Arial; color: #333333;">You
can locate your Cloud Server data center in the following ways</span>:

-   [Cloud Control Panel](https://mycloud.rackspace.com/) <span
    style="font-size: 12.0pt; line-height: 115%; font-family: Calibri; mso-ascii-theme-font: minor-latin; mso-fareast-font-family: Calibri; mso-fareast-theme-font: minor-latin; mso-hansi-theme-font: minor-latin; mso-bidi-font-family: Arial; color: #333333; mso-ansi-language: EN-US; mso-fareast-language: EN-US; mso-bidi-language: AR-SA;">&mdash;On
    the main Cloud Files page in the Control Panel, locate your Cloud
    Files data center in the **Region** column</span>.
-   Through the API<span
    style="font-size: 12.0pt; line-height: 115%; font-family: Calibri; mso-ascii-theme-font: minor-latin; mso-fareast-font-family: Calibri; mso-fareast-theme-font: minor-latin; mso-hansi-theme-font: minor-latin; mso-bidi-font-family: Arial; color: #333333; mso-ansi-language: EN-US; mso-fareast-language: EN-US; mso-bidi-language: AR-SA;">&mdash;
    Your Cloud Files data center is located in the storage URL that is
    returned when you authenticate to Cloud Files. For more information,
    see </span>[<span
    style="font-size: 12.0pt; line-height: 115%; font-family: Calibri; mso-ascii-theme-font: minor-latin; mso-fareast-font-family: Calibri; mso-fareast-theme-font: minor-latin; mso-hansi-theme-font: minor-latin; mso-bidi-font-family: Arial; color: #c50022; mso-ansi-language: EN-US; mso-fareast-language: EN-US; mso-bidi-language: AR-SA;">Retrieving
    the Authentication
    Token</span>](http://docs.rackspace.com/cas/api/v1.0/autoscale-devguide/content/Retrieving_Auth_Token.html).



