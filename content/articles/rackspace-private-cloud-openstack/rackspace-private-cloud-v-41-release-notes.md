---
node_id: 3652
title: Rackspace Private Cloud v. 4.1.1 Release Notes
permalink: article/rackspace-private-cloud-v-41-release-notes
type: article
created_date: '2013-08-20 15:53:03'
created_by: Karin Levenstein
last_modified_date: '2014-10-30 18:2955'
last_modified_by: jered.heeschen
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

Rackspace Private Cloud v 4.1.1 has the following changes and
documentation. For the full list of known issues and information from
the Rackspace Private Cloud v 4.0 release, refer to the [Rackspace
Private Cloud v. 4.0 Release
Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-40-release-notes).

Rackspace Private Cloud v 4.1.1 has the following changes and
documentation.

-   Changes to Cookbook Download Instructions
-   Changes in HA VIP Attributes

Cookbook Changes {.title}
----------------

The following changes have been made to the Rackspace Private Cloud
cookbooks.

-   The latest cookbook version number is `v4.1.1`{.filename}. This
    change is reflected in the instructions under [Install the Rackspace
    Private Cloud
    Cookbooks](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#install-cookbooks).
-   The override attributes for defining nova-network have changed. This
    change is reflected in the instructions under [Define Network
    Attributes](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#define-override-attrs).

Changes in HA VIP Attributes {.title}
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

RabbitMQ Clustering
-------------------

Rackspace Private Cloud v 4.1.1 builds out clustered RabbitMQ by
default. Fresh installations with v 4.1.1 include this feature
automatically, but installations created with Rackspace Private Cloud v
4.0.0 cookbooks will have to be upgraded with the procedure documented
in [Upgrading Your Private
Cloud](http://www.rackspace.com/knowledge_center/article/upgrading-your-private-cloud#upgrade-rabbitmq-v41).

