---
node_id: 3150
title: Removing Networks from a Cloud Server
permalink: article/removing-networks-from-a-cloud-server-0
type: article
created_date: '2012-10-30 12:34:45'
created_by: Susan Million
last_modified_date: '2016-01-05 22:0642'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

**NOTE**: Cloud Networks is production ready but will be available to
customers in a phased release. Therefore, it might not be visible when
you log into the Cloud Control Panel. To request access to Cloud
Networks now,
click [here](http://www.iwantcloudnetworks.com "I Want Cloud Networks").

Cloud Networks lets you attach an isolated network to new next
generation Cloud Servers. You can choose to attach or remove the
following networks to or from a Cloud Server:

**PublicNet**

Provides access to the Internet, Rackspace services such as Cloud
Monitoring, Managed Cloud Support, RackConnect, Cloud Backup, and
certain operating system updates.

**ServiceNet**

Provides access to Rackspace services such as Cloud Files, Cloud
Databases, Cloud Backup, and certain packages and patches through an
internal only, multi-tenant network connection within each Rackspace
data center.

**Isolated**

Provides a virtual Layer 2 network that keeps your server separate from
PublicNet, ServiceNet, or both.

Limitations
-----------

If you remove your Cloud Server from PublicNet, it no longer has access
to the Internet and some Rackspace products and services. If you remove
ServiceNet from your Cloud Server, it cannot access certain Rackspace
products and services. The graphic below depicts the services that are
not available when these networks are removed from a Cloud Server:

![Removing Networks from a Cloud
Server](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/cloud-networks-infographic-revised4.png)

### More Information on Cloud Networks

[Attach an Isolated Network to a New Cloud
Server](http://www.rackspace.com/knowledge_center/article/create-an-isolated-cloud-network "Attach an Isolated Network to a New Cloud Server")

[Attach a Cloud Network to an Existing Cloud
Server](http://www.rackspace.com/knowledge_center/article/attach-a-cloud-network-to-an-existing-cloud-server "Attach an Isolated Network to an Existing Cloud Server")

[Using CIDR notation in Cloud
Networks](http://www.rackspace.com/knowledge_center/article/using-cidr-notation-in-cloud-networks "CIDR Notation")

[Cloud Networks Developer
Guide](http://docs.rackspace.com/servers/api/v2/cn-devguide/content/ch_overview.html "Cloud Networks Developer Guide")

 

