---
node_id: 4227
title: RackConnect v3.0 compatibility
type: article
created_date: '2014-09-08 17:37:56'
created_by: juan.perez
last_modified_date: '2015-10-30 15:4257'
last_modified_by: rose.coste
product: RackConnect
body_format: tinymce
---

**Applies to**: RackConnect v3.0

This article outlines RackConnect v3.0's compatibility with other
Rackspace products and offerings. The following tables are provided:

-   [Table 1: RackConnect v3.0 compatibility with Rackspace public cloud
    offerings](#table1)
-   [Table 2: RackConnect v3.0 compatibility with Rackspace dedicated
    network device offerings](#table2)
-   [Table 3: RackConnect v3.0 compatibility with Rackspace dedicated
    offerings](#table3)

Table 1 lists and describes the Rackspace public cloud products that are
compatible with RackConnect v3.0.  The **Requirements** column lists the
requirements that your RackConnect v3.0 cloud servers must meet for them
to work with the listed product. For example, "ServiceNet" means that
your cloud servers must be provisioned with ServiceNet interfaces for
them to work with the designated product.

**Note:** Cloud Load Balancers and OnMetal Servers are not compatible
with RackConnect v3.0.

 

 [**Table 1&mdash; RackConnect v3.0 compatibility with Rackspace public cloud
offerings**]

RackConnect v3.0 compatibility matrix
-------------------------------------

###  Product

### Requirements

### Details

### Product support 

**Auto Scale**

None

Auto Scale is an API-based tool that automatically scales resources in
response to an increase or decrease in overall workload based on
user-defined thresholds. Auto Scale enables you to automatically scale
your RackConnect cloud servers resources to adjust to customer demand.

See the [Cloud Bursting with
RackConnectV3](http://docs.rackspace.com/cas/api/v1.0/autoscale-devguide/content/RCv3.html)
section of the [Rackspace Auto Scale Developer
Guide](http://docs.rackspace.com/cas/api/v1.0/autoscale-devguide/content/Overview.html)
for details on using Auto Scale with RackConnect v3.0.

[Auto Scale Getting Started
Guide](http://docs.rackspace.com/cas/api/v1.0/autoscale-gettingstarted/content/Overview.html)

[Auto Scale Developer
Guide](http://docs.rackspace.com/cas/api/v1.0/autoscale-devguide/content/Overview.html)

[Cloud Bursting with
RackConnectV3](http://docs.rackspace.com/cas/api/v1.0/autoscale-devguide/content/RCv3.html)

**Cloud Backup**

ServiceNet

Cloud Backup is a file-based backup application that enables you to
choose which files and folders to back up from your cloud servers. You
can choose to restore your whole system with all of its folders and
files, or individual files or folders from a given date, to restore to
an entirely different server. 

[Getting Started with Rackspace Cloud
Backup](http://www.rackspace.com/knowledge_center/getting-started/cloud-backup)

**Cloud Block Storage**

None

 Cloud Block Storage is a block-level storage solution that enables you
to expand the storage capacity of your Rackspace Next Generation Cloud
Servers.

[Getting Started with Cloud Block
Storage](http://www.rackspace.com/knowledge_center/getting-started/cloud-block-storage)

**Cloud Databases**

ServiceNet

Cloud Databases is a stand-alone, API-based relational database service
built on the OpenStac&reg; cloud that enables you to easily provision and
manage multiple MySQL database instances. Instances are provisioned in a
single-tenant, container-based environment per account.

-   RackConnect v3.0 is **compatible** with MySQL Cloud Databases
    instances.
-   **Note:** Cloud Databases is compatible with cloud servers only and
    cannot be used directly with dedicated servers.

[Getting Started with Cloud
Databases](http://www.rackspace.com/knowledge_center/getting-started/cloud-databases)

**Cloud Files**

ServiceNet 

Cloud Files, powered
by [OpenStack](http://www.rackspace.com/cloudbuilders/openstack/),
provides an easy-to-use online storage for files and media that can be
delivered globally at fast speeds over the Akamai content delivery
network (CDN). 

[Getting Started with Cloud
Files](http://www.rackspace.com/knowledge_center/getting-started/cloud-files)

****Cloud Monitoring****

Provisioned public IP address

Cloud Monitoring provides you with timely and accurate information about
how your resources are performing. You can quickly create multiple
monitors that use predefined checks such as PING, HTTPS and SMTP to
track your cloud resources and receive instant notification when a
resource needs your attention.

[Getting Started with Cloud
Monitoring](http://www.rackspace.com/knowledge_center/getting-started/cloud-monitoring)

****Cloud Networks****

None

RackConnect v3.0 depends on and leverages Cloud Networks to connect from
your RackConnect cloud servers to your dedicated environment. You use
Cloud Networks to create and manage secure, isolated networks in the
cloud.  These networks are fully single tenant and you have complete
control over the network topology, IP addressing, and which cloud
servers are attached. Cloud networks are regional in scope and can be
attached to any of your cloud servers in a given region. 

[Getting Started with Cloud
Networks](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-networks)

**Cloud Orchestration**

None

Rackspace Cloud Orchestration helps you set up projects and servers with
just a few clicks instead of lengthy installations. You can usually be
up and running in less than five minutes, depending on the template that
you choose and other factors. Cloud Orchestration provides templates for
a LAMP stack to get your web server up and running quickly, a Minecraft
server, and a WordPress blog, just to name a few.

[Quick set up with Rackspace Cloud
Orchestration](http://www.rackspace.com/knowledge_center/article/quick-set-up-with-rackspace-cloud-orchestration)

**Hadoop**

Provisioned public IP address & ServiceNet

Hadoop is an open source project that provides a platform to store and
process massive amounts of data. Hadoop uses the Map Reduce paradigm to
split large tasks into many smaller chunks and executes them in
parallel. Each of these tasks are executed close to the data in the
Hadoop Distributed File System.

[Getting Started with Apache Hadoop on Rackspace
Cloud](http://www.rackspace.com/knowledge_center/article/getting-started-with-apache-hadoop-on-rackspace-cloud)

****Managed Operations support level****

 ServiceNet

Managed Operations provides support beyond Managed Infrastructure,
including direct assistance with resizes, snapshots, host machine
issues, adding and removing servers, and managing IP addresses. To
ensure ***Fanatical Suppor&reg;***, Rackspace provides support for specific
software and server configurations on Cloud Servers with Managed
Operations support. 

 [Cloud Servers with Managed Operations support for
Linux](http://www.rackspace.com/knowledge_center/article/cloud-servers-with-managed-operations-support-for-linux)

**ObjectRocket**

ServiceNet

The ObjectRocket platform is built for scalability, speed, and safety.
It provides fully managed instances of MongoDB and Redis in data centers
across the globe.

Fast, scalable, reliable, and automated MongoDB & Redis

-   RackConnect v3.0 is **compatible** with **ObjectRocket
    Redis**instances that have a ServiceNet IP address in the
    10.188.0.0/15 range. If an instance has a ServiceNet IP address that
    is not in this range, contact ObjectRocket support .
-   RackConnect v3.0 is **compatible** with **MonogoDB**.

[ObjectRocket Getting Started
Guide](https://docs.objectrocket.com/getting_started.html)

 

Table 2 lists the dedicated network device offerings that are compatible
with RackConnect v3.

 [**Table 2*&mdash; **RackConnect v3.0 compatibility with Rackspace dedicated
network device offerings**]

+--------------------------------------+--------------------------------------+
| ### **Network device**               | ### **More information**             |
+--------------------------------------+--------------------------------------+
| **Cisco ASA Firewalls**              | [RackConnect Network Device          |
|                                      | Comparison](http://www.rackspace.com |
|                                      | /knowledge_center/article/rackconnec |
|                                      | t-network-device-comparison)         |
+--------------------------------------+--------------------------------------+
| **Cisco ASA X Series Firewalls**     | [RackConnect Network Device          |
|                                      | Comparison](http://www.rackspace.com |
|                                      | /knowledge_center/article/rackconnec |
|                                      | t-network-device-comparison)         |
+--------------------------------------+--------------------------------------+
| **BIG-IP F5 Load Balancers**         | [Using Dedicated Load Balancers with |
|                                      | RackConnect](http://www.rackspace.co |
|                                      | m/knowledge_center/article/using-ded |
|                                      | icated-load-balancers-with-rackconne |
|                                      | ct)                                  |
+--------------------------------------+--------------------------------------+
| **Brocade Load Balancers**           | [Using Dedicated Load Balancers with |
|                                      | RackConnect](http://www.rackspace.co |
|                                      | m/knowledge_center/article/using-ded |
|                                      | icated-load-balancers-with-rackconne |
|                                      | ct)                                  |
+--------------------------------------+--------------------------------------+

** **Table 3 lists the dedicated offerings that are compatible with
RackConnect v3.0. Compatibility with dedicated offerings is based on
network connectivity from these offerings to and from your RackConnect
v3.0 cloud networks. The correct routes to allow this traffic can be set
up by your Network Security team. 

 [**Table 3*&mdash; **RackConnect v3.0 compatibility with Rackspace dedicated
offerings**]

+--------------------------+--------------------------+--------------------------+
| ### **Network offering** | ### **Compatible**       | ### **Further details**  |
+--------------------------+--------------------------+--------------------------+
| **Managed Colocation**   | Network devices in a     | [Managed                 |
|                          | Managed Colocation       | Colocation](https://www. |
|                          | environment are          | rackspace.com/managed_ho |
|                          | supported only if the    | sting/managed_colocation |
|                          | network devices are      | /)                       |
|                          | managed by the Network   |                          |
|                          | Security team.           |                          |
|                          | Customer-managed network |                          |
|                          | devices are not          |                          |
|                          | supported.               |                          |
+--------------------------+--------------------------+--------------------------+
| **Managed                | The Managed Storage      | [Managed                 |
| Storage                  | offering is compatible   | Storage](https://www.rac |
|       **                 | only with dedicated      | kspace.com/managed_hosti |
|                          | servers in a RackConnect | ng/services/storage/)    |
|                          | configured dedicated     |                          |
|                          | environment.  The        |                          |
|                          | Managed Storage offering |                          |
|                          | cannot be used directly  |                          |
|                          | with cloud servers.      |                          |
+--------------------------+--------------------------+--------------------------+
| **Managed                | Yes                      | [Managed                 |
| Virtualization**         |                          | Virtualization](https:// |
|                          |                          | www.rackspace.com/cloud/ |
|                          |                          | private/managed_virtuali |
|                          |                          | zation/)                 |
+--------------------------+--------------------------+--------------------------+
| **Private Cloud**        | Yes                      | [Private                 |
|                          |                          | Cloud](https://www.racks |
|                          |                          | pace.com/cloud/private/) |
|                          |                          | .                        |
+--------------------------+--------------------------+--------------------------+

 

If you have questions, reach out to us. Contact information is available
on the [Contact Us](http://www.rackspace.com/knowledge_center/support)
page.

 

