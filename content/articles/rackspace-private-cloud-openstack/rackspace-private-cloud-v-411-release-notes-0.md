---
node_id: 3685
title: Rackspace Private Cloud v. 4.1.2 Release Notes
permalink: article/rackspace-private-cloud-v-411-release-notes-0
type: article
created_date: '2013-09-16 20:28:12'
created_by: Karin Levenstein
last_modified_date: '2014-08-23 19:5221'
last_modified_by: rose.contreras
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

Rackspace Private Cloud v 4.1.2 has the following changes and
documentation. For the full list of known issues and information from
the Rackspace Private Cloud v 4.0 release, refer to the [Rackspace
Private Cloud v. 4.0 Release
Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-40-release-notes).
[A new known issue has been identified in this release relating to
snapshot deletion in
CentOS](/knowledge_center/article/rackspace-private-cloud-v-40-release-notes#known-cinder-centOS).

Rackspace Private Cloud v 4.1.2 has the following changes.

Cookbook Changes {.title style="clear: both;"}
----------------

The following changes have been made to the Rackspace Private Cloud
cookbooks.

-   The latest cookbook version number is `v4.1.2`{.filename}. This
    change is reflected in the instructions under [Install the Rackspace
    Private Cloud
    Cookbooks](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#install-cookbooks).
-   The override attributes for defining nova-network have changed. This
    change is reflected in the instructions under [Define Network
    Attributes](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#define-override-attrs).

CentOS 6.4 Support
------------------

Rackspace Private Cloud can now be installed on CentOS 6.4.

Changes in HA VIP Attributes {.title style="clear: both;"}
----------------------------

A new configuration block must be used in
`override_attributes`{.filename} to define the virtual router ID and
network for the VIPs. Refer to [Controller Node High
Availability](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#nova-cluster-ha)
for detailed information about this configuration.

If you are upgrading your environment from an older configuration in
which VIP vrid and networks were not defined, you may have to remove the
keepalived configurations in `/etc/keepalived/conf.d/*`{.filename} and
run chef-client before adding the VIP vrid and network definitions to
override\_attributes.

OpenStack Networking HA
-----------------------

OpenStack Networking has been made HA as of Rackspace Private Cloud v
4.1.2, and has been tested on Ubuntu 12.04 and CentOS 6.4. For an HA
configuration, you must configure the OpenStack networking roles on the
Controller node. Do not use a standalone Network node if you require
OpenStack Networking to be HA.

OpenStack Networking Support on CentOS
--------------------------------------

Rackspace Private Cloud can now be used to implement OpenStack
Networking on devices running CentOS 6.4. After applying the
`single-network-node` role to the device, you must reboot it to use the
appropriate version of the CentOS 6.4 kernel.

RabbitMQ Clustering
-------------------

Rackspace Private Cloud v 4.1.2 builds out clustered RabbitMQ by
default. Fresh installations with v 4.1.2 include this feature
automatically, but installations created with Rackspace Private Cloud v
4.0.0 cookbooks will have to be upgraded with the procedure documented
in [Upgrading Your Private
Cloud](http://www.rackspace.com/knowledge_center/article/upgrading-your-private-cloud#upgrade-rabbitmq-v41).

