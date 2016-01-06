---
node_id: 2250
title: Removing Networks from a Cloud Server
permalink: article/disabling-servicenet
type: article
created_date: '2012-09-25 18:40:05'
created_by: David Hendler
last_modified_date: '2014-12-22 22:3450'
last_modified_by: jered.heeschen
products: Cloud Servers
body_format: tinymce
---

Cloud Networks lets you attach an isolated network to new next
generation Cloud Servers (or to existing servers via the [Cloud Servers
API](http://docs.rackspace.com/servers/api/v2/cs-devguide/content/section_virt_ext.html)). You
can choose to attach or remove the following networks to or from a Cloud
Server:

**PublicNet**

Provides access to the Internet, Rackspace services such as Cloud
Monitoring, Managed Cloud Service Level support, RackConnect, and Cloud
Backup, and certain operating system updates.

**ServiceNet**

Provides access to Rackspace services such as Cloud Files, Cloud
Databases, Cloud Backup, and certain packages and patches through an
internal only, multi-tenant network connection within each Rackspace
data center.

**Isolated**

Provides a virtual Layer 2 network that keeps your server separate from
PublicNet, ServiceNet, or both.

**Limitations**
---------------

If you remove your Cloud Server from PublicNet, it no longer has access
to the Internet and some Rackspace products and services. If you remove
ServiceNet from your Cloud Server, it cannot access certain Rackspace
products and services. The graphic below depicts the services that are
not available when these networks are removed from a Cloud Server:

![](/knowledge_center/sites/default/files/field/image/Cloud-Networks-graphic-v2.png)

### More Information on Cloud Networks

[Attach an Isolated Network to a New Cloud
Server](http://www.rackspace.com/knowledge_center/article/create-an-isolated-cloud-network "Attach an Isolated Network to a New Cloud Server")

[Attach an Isolated Network to an Existing Cloud
Server](http://www.rackspace.com/knowledge_center/article/attach-an-existing-cloud-server-to-a-cloud-network "Attach an Isolated Network to an Existing Cloud Server")

[CIDR
Notation](http://www.rackspace.com/knowledge_center/article/using-cidr-notation "CIDR Notation")

[Cloud Networks Developer
Guide](http://docs.rackspace.com/servers/api/v2/cn-devguide/content/ch_overview.html "Cloud Networks Developer Guide")

 

