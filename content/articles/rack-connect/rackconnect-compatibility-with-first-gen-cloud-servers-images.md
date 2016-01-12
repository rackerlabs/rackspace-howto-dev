---
node_id: 2030
title: Cloud Server images for use with RackConnect v2.0
permalink: article/rackconnect-compatibility-with-first-gen-cloud-servers-images
type: article
created_date: '2012-08-21 20:03:02'
created_by: David Hendler
last_modified_date: '2016-01-06 20:5142'
last_modified_by: catherine.richardson
products: RackConnect
body_format: tinymce
---

**Applies to:** RackConnect v2.0

To create new servers, you can use Cloud Servers images that are
available in the [MyRackspace Portal](https://my.rackspace.com/), the
[Cloud Control Panel](https://mycloud.rackspace.com/), or the Cloud
Servers API. To ensure that you are using a Cloud Servers image that is
compatible with RackConnect, we recommend that you use the MyRackspace
Portal when creating your servers. This article provides details about
the compatibility of Cloud Servers images with RackConnect.

Managed Infrastructure images
-----------------------------

Some Cloud Servers images are incompatible with RackConnect at the
Managed Infrastructure service level. If you have the Managed
Infrastructure service level, do *not* use the following base images
with RackConnect:

  Image name                                           Image ID
  ---------------------------------------------------- ----------
  Oracle EL R5U3 JEOS                                  41
  Windows Server 2008 SP2 Enterprise 64-bit            24
  Windows Server 2008 SP2 Enterprise 32-bit            31
  Windows Server 2008 SP2 Enterprise 32-bit with SQL   56
  Windows Server 2008 SP2 Enterprise 64-bit with SQL   57
  Arch 2011.10                                         100
  FreeBSD 9.0                                          107
  Gentoo 11.0                                          108
  openSUSE 12                                          109

Managed Infrastructure Windows images
-------------------------------------

**Note:** You cannot use the Cloud Control Panel to create Managed
Infrastructure Windows cloud servers for use with RackConnect. Use the
MyRackspace Portal or the Cloud Servers API instead.

Some Managed Infrastructure Windows Cloud Servers images that are
available via the Cloud Servers API cannot be used with RackConnect. If
you are interacting directly with the API, you must use the image IDs to
look up the recommended images because they do not appear in the image
list via the API. These images are available only as *hidden* images. If
you are using the Managed Infrastructure service level, use the
equivalent image listed in the following table. The suggested images
enable the RackConnect automation to run properly.

+--------------------------------------+--------------------------------------+
| Image typically used                 | Hidden image to use instead          |
+======================================+======================================+
| Image ID: 85\                        | Image ID: 30\                        |
|  Image name: Windows Server 2008 R2  |  Image name: Windows Server 2008 R2  |
| x64                                  | x64 RC                               |
+--------------------------------------+--------------------------------------+
| Image ID: 86\                        | Image ID: 32\                        |
|  Image name: Windows Server 2008 R2  |  Image name: Windows Server 2008 R2  |
| x64 + SQL Server 2008 R2 Standard    | x64 - MSSQL2K8R2                     |
+--------------------------------------+--------------------------------------+
| Image ID: 89\                        | Image ID: 34\                        |
|  Image name: Windows Server 2008 R2  |  Image name: Windows Server 2008 R2  |
| x64 + SQL Server 2008 R2 Web         | x64 - SQL Web RC                     |
+--------------------------------------+--------------------------------------+

The difference between the RackConnect and non-RackConnect images is a
small change in the Windows firewall, which allows access for the
automation systems.

If you are using the MyRackspace Portal to create cloud servers on a
Cloud account with RackConnect, you will automatically see the correct
Windows images, and no additional action is required. You might not see
the image IDs through the MyRackspace Portal.

Managed Operations images
-------------------------

All standard base images that are available through the API and
MyRackspace Portal are compatible with RackConnect at the Managed
Operations service level.

[Using Cloud Load Balancers with
RackConnect](http://www.rackspace.com/knowledge_center/article/using-cloud-load-balancers-with-rackconnect)
\< Previous | Next \> [RackConnect compatibility with Cloud Servers
Images](http://www.rackspace.com/knowledge_center/article/rackconnect-v20-compatibility-with-cloud-server-images)

