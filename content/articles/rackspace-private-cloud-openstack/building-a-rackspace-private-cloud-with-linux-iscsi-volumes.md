---
node_id: 3272
title: Building a Rackspace Private Cloud with Linux iSCSI Volumes
type: article
created_date: '2013-01-24 18:19:47'
created_by: alyssah
last_modified_date: '2013-03-27 18:3956'
last_modified_by: Rae D. Cabello
products: Rackspace Private Cloud - OpenStack
body_format: full_html
---

undefined&ndash;then you can add the block devices into the
volume group.

For the compute deployment, we chose the Dell C6220 because it provides
a balance of density and flexibility, while maximizing uptime with four
independent, hot-swappable servers in one chassis. Thus, we can reach
100 physical nodes in the cluster with only 25 x 2U enclosures. The
networking for compute had a number of different requirements.
Specifically, we needed to provide for management and instance traffic
as well as storage traffic. To provide the management and instance
network traffic, we used commodity, layer-2 switches. However, due to
latency, stability, and performance requirements for iSCSI, we isolated
storage traffic to Arista 7050 switches. 

 

Deploying the Storage Infrastructure
------------------------------------

After the Rackspace Private Cloud Software is installed on the
infrastructure, the cinder chef roles must be added to the controller
and storage nodes. For details on this step, review the following
article: [Configuring OpenStack Block
Storage](http://www.rackspace.com/knowledge_center/article/configuring-openstack-block-storage)[\
](http://www.rackspace.com/knowledge_center/article/configuring-openstack-block-storage)

*Note: the storage requirements in the document. All drive devices on
the storage nodes can be added to the cinder-volumes group. This can be
a combination of any storage available on the R515s, both local storage
on the chassis and DAS.*

Caveats
-------

In contrast to traditional shared storage, this system favors horizontal
scaling, rather than vertical scaling. While there are multiple storage
nodes, there is no data clustering used in this design. Thus, losing a
storage node can result in data loss or corruption. We recommend RAID 10
protection on the drives to maximize performance while minimizing data
loss. If, instead, your goal is to maximize usable storage, RAID 6 can
be used to maximize space while minimizing drive failure. For the
storage network, you have many choices for protocols and transports. In
this design, we use twinax for 10 GbE, but CAT6 or fiber can be used
too, as long as the network interface card or fabric adaptor is
compatible with Ubuntu 12.04.

