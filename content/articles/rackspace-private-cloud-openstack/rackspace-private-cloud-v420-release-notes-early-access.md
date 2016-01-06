---
node_id: 3748
title: Rackspace Private Cloud v4.2.0 Release Notes - Early Access
permalink: article/rackspace-private-cloud-v420-release-notes-early-access
type: article
created_date: '2013-10-30 20:04:27'
created_by: Karin Levenstein
last_modified_date: '2014-11-07 20:4528'
last_modified_by: ross.diaz
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

This article documents the changes in Rackspace Private Cloud v4.2.0 and
identified known issues.

For the release notes for previous versions, refer to the following
articles:

-   [Rackspace Private Cloud v4.1.2 Release
    Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-412-release-notes-0)
-   [Rackspace Private Cloud v4.0 Release
    Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-40-release-notes)

Contents
--------

[1. Overview](#overview)

[Intended Audience](#overview-audience)

[Document Change History](#overview-dochistory)

[Additional Resources](#overview-resources)

[Contact Rackspace](#contact-rackspace)

[2. What's New in Rackspace Private Cloud v4.2.0](#newfeatures-4.2.0)

[Cookbook Version](#cookbook-download-4.2)

[OpenStack](#openstack-changes)

[High Availability](#high-availability)

[OpenStack Networking (Neutron)](#openstack-networking)

[OpenStack Block Storage (Cinder)](#cinder)

[Dashboard Changes](#other-changes)

[3. Rackspace Private Cloud Object Storage](#openstack-objectstorage)

[4. Known Issues](#known-issues)

[Restarting RabbitMQ](#known-rabbitmq-restart)

[Intermittent Failover Failure](#known-failover-rabbitmq)

[OpenStack Orchestration and Instance
Names](#known-orchestration-instance-name)

[CentOS and RHEL Challenges With Advanced OpenStack
Networking](#known-neutron-redhat)

[Snapshot Deletion on CentOS](#known-cinder-centOS)

[OpenStack Metering Visualization](#known-ceilometer-vis)

Chapter 1. Overview {.title}
-------------------

Rackspace has developed a fast, free, and easy way to install a
Rackspace Private Cloud powered by OpenStack in any data center. This
method is suitable for anyone who wants to install a stable, tested, and
supportable OpenStack-powered private cloud, and can be used for all
scenarios from initial evaluations to production deployments.

Rackspace Private Cloud v4.2.*`n`* supports the [Havana release of
OpenStack](http://www.openstack.org/software/grizzly/).

### Intended Audience {.title}

This document describes the updates in Rackspace Private Cloud
v4.2.*`n`* and any known issues in the product. You should already be
familiar with Rackspace Private Cloud Software and have prior knowledge
of OpenStack and cloud computing, basic Linux administration skills, and
a side of bacon. :)

### Document Change History {.title}

This version of the Rackspace Private Cloud Release Notes replaces and
obsoletes all previous versions. The most recent changes are described
in the table below:

Revision Date

Summary of Changes

November 13, 2013

-   Rackspace Private Cloud v4.2.0 release.

### Additional Resources {.title}

-   [Rackspace Private Cloud Home
    Page](http://www.rackspace.com/cloud/private/)
-   [Rackspace Private Cloud Knowledge
    Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud)
-   [Rackspace Private Cloud
    Forums](http://privatecloudforums.rackspace.com/)

### Contact Rackspace {.title}

For more information about sales and support, contact us at
[opencloudinfo@rackspace.com](mailto:opencloudinfo@rackspace.com).

For feedback on the product and the documentation, contact us at
[RPCFeedback@rackspace.com](mailto:RPCFeedback@rackspace.com).

For the documentation, you can also leave a comment at [the Knowledge
Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud).

Chapter 2. What's New in Rackspace Private Cloud v4.2.0 {.title}
-------------------------------------------------------

In addition to several stability and usability fixes, Rackspace Private
Cloud v4.2.0 has the following changes.

### Cookbook Version {.title}

The latest cookbook version number is `v4.2.0`{.filename}. This change
is reflected in the instructions under [Install the Rackspace Private
Cloud
Cookbooks](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#install-cookbooks).

**NOTE**: Rackspace Private Cloud v4.2.0 is based on the OpenStack
Havana code base, and is being made available as an Early Access release
to customers who want to deploy it in a proof-of-concept or other
non-production environment. Rackspace Private Cloud v4.1.2, based on the
OpenStack Grizzly code base, is recommended for production environments.

### OpenStack {.title}

The following changes have been made to OpenStack support in Rackspace
Private Cloud:

-   Rackspace Private Cloud v4.2.0 is based on the Havana release of
    OpenStack. For detailed information about the Havana release, refer
    to the [OpenStack Havana Release
    Notes](https://wiki.openstack.org/wiki/ReleaseNotes/Havana).
-   [OpenStack Metering
    (Ceilometer)](http://www.rackspace.com/knowledge_center/article/openstack-metering)
    is fully implemented, including access to OpenStack statistics
    through the Horizon dashboard.

    The Rackspace Private Cloud implementation of Metering is based on a
    MySQL framework and uses the SQL Alchemy. For more information about
    the parameters involved in this implementation, refer to [the
    OpenStack documentation on Metering configuration
    options](http://docs.openstack.org/developer/ceilometer/configuration.html).
    For a list of database backends and what they support, refer to [the
    OpenStack documentation on choosing a database backend for
    metering](http://docs.openstack.org/developer/ceilometer/install/dbreco.html).

-   [A technology preview presentation of OpenStack Orchestration
    (Heat)](http://www.rackspace.com/knowledge_center/article/openstack-orchestration)
    is available. This tool enables you to manage infrastructure and
    applications within OpenStack clouds. The Rackspace Private Cloud
    implementation of Orchestration includes the following components:

    -   The standard Heat API
    -   The heat-api-cfn API
    -   The CloudWatch API, which enables metric collection

    OpenStack Orchestration is not installed by default in the
    all-in-one or controller cookbooks, but can be installed afterward
    by applying the Heat roles to the Controller node.

### High Availability {.title}

The following changes have been made to High Availability in Rackspace
Private Cloud:

-   Increased reliability under a wider range of circumstances, such as
    manual failover for maintenance, power loss, and network isolation.
-   Messages with lost messages during rabbitmq failover have been
    resolved.
-   OpenStack Networking availability in failure scenarios has been
    increased. The RPCDaemon tool improves OpenStack Networking
    scheduling of DHCP agents and L3 agents.

### OpenStack Networking (Neutron) {.title}

The following changes have been made to OpenStack Networking in
Rackspace Private Cloud:

-   The Rackspace Private Cloud v4.2.0 cookbooks have been updated to
    change packages and attributes from `quantum`{.filename} to
    `neutron`{.filename}, reflecting the OpenStack project name change.
-   L3 agent support is now available, which enables floating IPs and
    routers. For more information about L3 routing, refer to ["L3
    Routing and NAT" in the OpenStack Networking Administration
    Guide](http://docs.openstack.org/network-admin/admin/content/l3_workflow.html).

### OpenStack Block Storage (Cinder) {.title}

The following changes have been made to OpenStack Block Storage in
Rackspace Private Cloud:

-   LVM provider is now used by default, which provides better
    performance and reliability.
-   Standard paste configuration is now used, to provide the same
    configuration on CentOS/RHEL and Ubuntu.

Dashboard Changes {.title}
-----------------

You can access [Rackspace Private Cloud documentation on the Knowledge
Center](http://www.rackspace.com/knowledge_center/getting-started/rackspace-private-cloud)
by clicking the Help link on the dashboard.

Chapter 3. Rackspace Private Cloud Object Storage {.title}
-------------------------------------------------

Rackspace has developed an Object Storage offering compatible with the
Rackspace Private Cloud offering.

If you are interested in a deployment of Rackspace Private Cloud Object
Storage, contact your Rackspace support representative for more
information. You can work with Rackspace to have an Object Storage
cluster configured in your data center or in a Rackspace data center.
Contact Rackspace for more information.

OpenStack Object Storage is available as a General Access feature rather
than an Early Access feature. For an overview of the Rackspace Private
Cloud Object Storage architecture, refer to "Distributed Object Storage"
on our [Private Cloud Architectures
page](http://www.rackspace.com/cloud/private/architecture/).

Chapter 4. Known Issues {.title}
-----------------------

The following issues have been identified in Rackspace Private Cloud
v4.2.0.

### Restarting RabbitMQ {.title}

When a RabbitMQ cluster fails, it must be brought up in the reverse
order in which it went down, or the restart will fail. For example, if
RabbitMQ goes down on `controller1`{.filename} and then on
`controller2`{.filename}, the service should first be started on
`controller2`{.filename}, and then on `controller1`{.filename}.

### Intermittent Failover Failure {.title}

Occasionally, failover between HA Controller nodes may fail due to
multiple RabbitMQ processes existing on the secondary Controller node.
Restarting RabbitMQ will bring the cluster back online:

~~~~ {.screen}
# pkill -f rabbitmq; service rabbitmq-server restart
                
~~~~

### OpenStack Orchestration and Instance Names {.title}

OpenStack Orchestration builds instance names based on the stack name,
which results in long instance names. Instance names that are longer
than 64 characters may cause the stack to fail to build. You should keep
stack names short to avert this issue.

### CentOS and RHEL Challenges With Advanced OpenStack Networking {.title}

When using OpenStack Networking (Neutron), Controller nodes with
Networking features and standalone Networking nodes require namespace
kernel features that are not available in the default kernel shipped
with CentOS 6.4, RHEL 6.4, and older versions of these operating
systems. More information about Neutron limitations is available in the
[OpenStack
documentation](http://docs.openstack.org/grizzly/openstack-network/admin/content/ch_limitations.html),
and more information about RedHat-derivative kernel limitations is
provided in the [RDO
FAQ](http://openstack.redhat.com/Frequently_Asked_Questions#For_which_distributions_does_RDO_provide_packages.3F).

Rackspace recommends that you upgrade to the latest RDO kernel if you
are going to use CentOS or RHEL for networking nodes.

### Snapshot Deletion on CentOS {.title}

Setting `volume_clear`{.filename} in `cinder.conf`{.filename} to
`shred`{.filename} or `zero`{.filename} will cause snapshot deletion to
fail in OpenStack Grizzly installations on CentOS. Rackspace recommends
you set `volume_clear`{.filename} to `none`{.filename} until this issue
is resolved in OpenStack.

### OpenStack Metering Visualization {.title}

Rackspace Private Cloud is currently using the patch referenced in
[Ceilometer bug
\#1093625](https://bugs.launchpad.net/ceilometer/+bug/1093625) to
address issues with OpenStack Metering visualization. If the underlying
packages are updated, you may experience patch issues. We will continue
to monitor the status of this bug for future releases.

