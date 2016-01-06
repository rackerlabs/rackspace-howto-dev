---
node_id: 2030
title: Cloud Server images for use with RackConnect v2.0
permalink: article/rackconnect-compatibility-with-first-gen-cloud-servers-images
type: article
created_date: '2012-08-21 20:03:02'
created_by: David Hendler
last_modified_date: '2015-07-23 21:4125'
last_modified_by: kelly.holcomb
products: RackConnect
body_format: tinymce
---

**APPLIES TO**: RackConnect v2.0

To create new servers, you can use Cloud Server images that are
available in the MyRackspace Portal, the Cloud Control Panel, or the
Cloud Servers API. To ensure that you are using a Cloud Server image
that is compatible with RackConnect, we recommend that you use the
MyRackspace Portal when creating your servers. This article provides
details about Cloud Server images compatible with RackConnect.

**MyRackspace
Portal:**[https://my.rackspace.com/](https://my.rackspace.com/)

**Cloud Control Panel:**
[https://mycloud.rackspace.com/](https://mycloud.rackspace.com/)\
** **

 

**Managed Infrastructure Images**
---------------------------------

Some Cloud Server images are incompatible with RackConnect at the
Managed Infrastructure level.  Do *not* use the following base images
with RackConnect:

![](/knowledge_center/sites/default/files/field/image/Core.SL_.Incompatible.Images_0.png) 
 

** **

**Windows Managed Infrastructure Images**
-----------------------------------------

*Note: You cannot use the [Cloud Control
Panel](https://mycloud.rackspace.com/)to create Managed Infrastructure
Windows Cloud Servers for use with RackConnect.  Use the
[MyRackspace](https://my.rackspace.com/)Portal or the Cloud Servers API
instead.*\
\
Some Managed Infrastructure Windows Cloud Server images available via
the Cloud Servers API cannot be used with RackConnect.  If you are
interacting directly with the API, you need to use the Image IDs to look
up the recommended images because they do not appear in the image list
via the API.  They are available only as **hidden** images.  If you are
use the Managed Infrastructure, you should use the equivalent image
listed in the following table.  The suggested images allow the
RackConnect automation to run properly.

![](/knowledge_center/sites/default/files/field/image/Core.SL_.Compatible.Windows.Images_0.png)\
\
The difference between the RackConnect and non-RackConnect images is a
slight change in the Windows Firewall, which allows access for the
automation systems. \
\
If you are using the [MyRackspace](https://my.rackspace.com/)Portal to
create Cloud Servers on a Cloud Account with RackConnect, you will
automatically see the correct Windows images, and no additional action
is required.  You might not see the Image IDs through the
[MyRackspace](https://my.rackspace.com/)Portal.\
\

 

**Managed Operations Images**
-----------------------------

All standard base images available via the API and
[MyRackspace](https://my.rackspace.com/)Portal are compatible with
RackConnect at the Managed Operations level.

[Using Cloud Load Balancers with
RackConnect](http://www.rackspace.com/knowledge_center/article/using-cloud-load-balancers-with-rackconnect)
\<---Previous | Next ---\> [RackConnect Compatibility with Cloud Server
Images](http://www.rackspace.com/knowledge_center/article/rackconnect-compatibility-with-cloud-server-images)

