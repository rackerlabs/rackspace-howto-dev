---
node_id: 3799
title: Rackspace Private Cloud v4.2.1 Release Notes
permalink: article/rackspace-private-cloud-v421-release-notes-0
type: article
created_date: '2013-12-04 15:30:41'
created_by: Karin Levenstein
last_modified_date: '2015-06-10 16:3210'
last_modified_by: kyle.laffoon
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

This article documents the changes in Rackspace Private Cloud v4.2.1 and
v4.2.0 and identified known issues.

For the release notes for previous versions, refer to the following
articles:

-   [Rackspace Private Cloud v4.1.2 Release
    Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-412-release-notes-0)
-   [Rackspace Private Cloud v4.0 Release
    Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-40-release-notes)

**Table of Contents**

[1. Overview](#overview)

[Intended audience](#overview-audience)

[Document change history](#overview-dochistory)

[Additional resources](#overview-resources)

[Contact Rackspace](#contact-rackspace)

[2. What's new in Rackspace Private Cloud v4.2.1](#newfeatures-4.2.1)

[Cookbook version](#cookbook-download-4.2.1)

[LBaaS in OpenStack Networking (Neutron)](#openstack-networking-lbaas)

[Upgrading from v4.1.n to v4.2.1](#upgrade-tool)

[Rackspace Private Cloud Sandbox](#rpc-sandbox)

[3. What's new in Rackspace Private Cloud v4.2.0](#newfeatures-4.2.0)

[OpenStack](#openstack-changes)

[High Availability](#high-availability)

[OpenStack Networking (Neutron)](#openstack-networking)

[OpenStack Block Storage (Cinder)](#cinder)

[Dashboard changes](#other-changes)

[4. Rackspace Private Cloud Object Storage](#openstack-objectstorage)

[5. Known Issues](#known-issues)

[Upgrading from v4.1.3 to v4.2.1](#upgrading-4.1.3-to-4.2.1)

[Upgrading from v4.2.0 to v4.2.1](#upgrading-to-4.2.1)

[Restarting RabbitMQ](#known-rabbitmq-restart)

[Intermittent failover failure](#known-failover-rabbitmq)

[OpenStack Orchestration and instance
names](#known-orchestration-instance-name)

[CentOS and RHEL challenges with advanced OpenStack
Networking](#known-neutron-redhat)

[Snapshot deletion on CentOS](#known-cinder-centOS)

[OpenStack Metering visualization](#known-ceilometer-vis)

[OpenStack service timeouts](#known-openstack-timeouts)

[Ephemeral and swap disks on RHEL](#known-ephemeral-disks)

[Ceilometer packages fail to install](#known-ceilometer-packages)

[Horizon is not installed correctly](#known-horizon-install)

1. Overview {.title}
-----------

Rackspace has developed a fast, free, and easy way to install a
Rackspace Private Cloud powered by OpenStack in any data center. This
method is suitable for anyone who wants to install a stable, tested, and
supportable OpenStack-powered private cloud, and can be used for all
scenarios from initial evaluations to production deployments.

Rackspace Private Cloud v4.2.n supports the [Havana release of
OpenStack](http://www.openstack.org/software/grizzly/).

### Intended audience {.title}

This document describes the updates in Rackspace Private Cloud v4.2.n
and any known issues in the product. You should already be familiar with
Rackspace Private Cloud Software and have prior knowledge of OpenStack
and cloud computing, and basic Linux administration skills.

### Document change history {.title}

This version of the Rackspace Private Cloud Release Notes replaces and
obsoletes all previous versions. The most recent changes are described
in the table below:

Revision Date

Summary of Changes

December 18, 2013

-   Rackspace Private Cloud v4.2.1 release.

November 13, 2013

-   Rackspace Private Cloud v4.2.0 release.

 

### Additional resources {.title}

-   [Rackspace Private Cloud Home
    Page](http://www.rackspace.com/cloud/private/)
-   [Rackspace Private Cloud Knowledge
    Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud)
-   [Rackspace Private Cloud
    Forums](http://privatecloudforums.rackspace.com/)

### Contact Rackspace {.title}

For more information about sales and support, send an email to
[`<`{.email}](mailto:opencloudinfo@rackspace.com)[opencloudinfo@rackspace.com](mailto:opencloudinfo@rackspace.com)[`>`{.email}](mailto:opencloudinfo@rackspace.com).

If you have feedback about the product and the documentation, send and
email to
[`<`{.email}](mailto:RPCFeedback@rackspace.com)[RPCFeedback@rackspace.com](mailto:RPCFeedback@rackspace.com)[`>`{.email}](mailto:RPCFeedback@rackspace.com).
For the documentation, you can also leave a comment at [the Knowledge
Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud).

For more troubleshooting information and user discussion, you can also
inquire at the Rackspace Private Cloud Support Forum at
[`https://community.rackspace.com/products/f/45`{.uri}](https://community.rackspace.com/products/f/45)

2. What's new in Rackspace Private Cloud v4.2.1 {.title}
-----------------------------------------------

In addition to several stability and usability fixes, Rackspace Private
Cloud v4.2.1 has the following changes.

### Cookbook version {.title}

The latest cookbook version number is `v4.2.1`{.filename}. This change
is reflected in the instructions under [Install the Rackspace Private
Cloud
Cookbooks](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#install-cookbooks).

Where Rackspace Private Cloud v4.2.0 was made available as an Early
Access release, Rackspace Private Cloud v4.2.1 is a production-ready
release based on the OpenStack Havana code base. For detailed
information about the Havana release, refer to the [OpenStack Havana
Release Notes](https://wiki.openstack.org/wiki/ReleaseNotes/Havana).

### LBaaS in OpenStack Networking (Neutron) {.title}

Rackspace Private Cloud v4.2.1 adds a technology preview implementation
of Load Balancing as a Service (LBaaS) support with the
`neutron-lbaas-agent`{.filename} recipe, which is part of the
`single-network-node`{.filename} role. The Rackspace Private Cloud
cookbooks currently support only the HAProxy LBaaS service provider.
LBaaS is not currently recommended for Rackspace Private Cloud
production environments.

For more information, refer to [Configuring Load Balancing as a
Service](http://www.rackspace.com/knowledge_center/article/configuring-openstack-networking#neutron-lbaas).

### Upgrading from v4.1.n to v4.2.1 {.title}

Users who want to upgrade from an existing Rackspace Private Cloud
v4.1.n Grizzly cluster to a Havana cluster should upgrade to v4.2.1.
Because of the OpenStack version change and the renaming of attributes
from `quantum`{.filename} to `neutron`{.filename}, this upgrade process
is more complex and is best facilitated with the Rackspace Private Cloud
`mungerator`{.filename} tool. This upgrade process is documented in
[Upgrading from v4.1.n to
v4.2.1](http://www.rackspace.com/knowledge_center/article/upgrading-your-private-cloud#upgrade-v41n-v42n)

The following matrix indicates which upgrade scenarios are supported.

Upgrade Scenario

Supported

Not Supported

v4.2.0 =\> v4.2.n

 

X

v4.1.n =\> v4.2.1

X

 

v4.1.n =\> v4.2.0

 

X

v4.1.n =\> v4.1.n

X

 

v4.0.0 =\> v4.2.n

 

X

v4.0.0 =\> v4.1.n

X

 

v3 (OpenCenter) =\> Any

 

X

v2 (Alamo) =\> Any

 

X

Users who currently have Rackspace Private Cloud v4.0.0 and want to
upgrade to v4.2.1 must first upgrade to v4.1.3.

Note

For users who installed v4.2.0, which was made available only as an
Early Access release, there is a known issue in upgrades from v4.2.0 to
v4.2.1 relating to HAProxy . For more information, see [Upgrading to
from v4.2.0 to
v4.2.1](#upgrading-to-4.2.1 "Upgrading from v4.2.0 to v4.2.1").

### Rackspace Private Cloud Sandbox {.title}

Rackspace Private Cloud Sandbox enables you to install an
OpenStack-powered private cloud for testing or demonstration purposes in
VMWare or VirtualBox. Rackspace Private Cloud Sandbox v1.0 runs
Rackspace Private Cloud v4.2.1 powered by the Havana release of
OpenStack. For information about this product and instructions for using
it, see [Rackspace Private Cloud
Sandbox](/knowledge_center/article/rackspace-private-cloud-sandbox).

3. What's new in Rackspace Private Cloud v4.2.0 {.title}
-----------------------------------------------

In addition to several stability and usability fixes, Rackspace Private
Cloud v4.2.0 has the following changes.

Note

Rackspace Private Cloud was made available as an Early Access release.
Rackspace recommends using Rackspace Private Cloud v4.2.1 for a
Havana-based private cloud and Rackspace Private Cloud v4.1.3 for a
Grizzly-based private cloud.

### OpenStack {.title}

The following changes have been made to OpenStack support in Rackspace
Private Cloud:

-   Rackspace Private Cloud v4.2.0 is based on the Havana release of
    OpenStack. For detailed information about the Havana release, refer
    to the [OpenStack Havana Release
    Notes](https://wiki.openstack.org/wiki/ReleaseNotes/Havana).
-   [OpenStack Metering
    (Ceilometer)](http://docs.openstack.org/developer/ceilometer/overview.html#metering)
    is fully implemented, including access to OpenStack statistics
    through the Horizon dashboard.

    The Rackspace Private Cloud implementation of Metering is based on a
    MySQL framework and uses SQL Alchemy. For more information about the
    parameters involved in this implementation, refer to [the OpenStack
    documentation on Metering configuration
    options](http://docs.openstack.org/developer/ceilometer/configuration.html).
    For a list of database backends and what they support, refer to [the
    OpenStack documentation on choosing a database backend for
    metering](http://docs.openstack.org/developer/ceilometer/install/dbreco.html).

-   [A technology preview presentation of OpenStack Orchestration
    (Heat)](https://developer.rackspace.com/blog/openstack-orchestration-in-depth-part-1-introduction-to-heat/)
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

### Dashboard changes {.title}

You can access [Rackspace Private Cloud documentation on the Knowledge
Center](http://www.rackspace.com/knowledge_center/getting-started/rackspace-private-cloud)
by clicking the Help link on the dashboard.

4. Rackspace Private Cloud Object Storage {.title}
-----------------------------------------

Rackspace has developed an Object Storage offering compatible with the
Rackspace Private Cloud offering.

If you are interested in a deployment of Rackspace Private Cloud Object
Storage, contact your Rackspace support representative for more
information. You can work with Rackspace to have an Object Storage
cluster configured in your data center or in a Rackspace data center.

For an overview of the Rackspace Private Cloud Object Storage
architecture, refer to "Distributed Object Storage" on our [Private
Cloud Architectures
page](http://www.rackspace.com/cloud/private/architecture/).

5. Known Issues {.title}
---------------

The following issues have been identified in Rackspace Private Cloud
v4.2.0 and v4.2.1.

### Upgrading from v4.1.3 to v4.2.1 {.title}

When upgrading from v4.1.3 to v4.2.1, chef-client may fail on the
Compute nodes due to a conflict in python-swiftclient versions. If this
failure occurs, run chef-client a second time.

### Upgrading from v4.2.0 to v4.2.1 {.title}

The implementation of HAProxy VIP routing has changed in v4.2.1. After
an upgrade from v4.2.0 to v4.2.1, the HAProxy VIP must be removed from
the loopback interface (lo). This issue applies **only** to upgrades
from v4.2.0 to v4.2.1.

The following upgrade process ensures that the HAProxy VIP is configured
correctly for v4.2.1, and should prevent you from having to manually
remove the HAProxy VIP.

1.  Log into the Chef server as the root user.
2.  Run the **knife environment edit** command.

    ~~~~ {.screen}
    # knife environment edit <environmentName>
                    
    ~~~~

3.  Edit the environment by changing the
    `do_package_upgrades`{.filename} and `image_upload`{.filename}
    override attributes. This forces the package upgrades and also
    disables image uploading, which enables you to work around issues
    related to Glance.

    ~~~~ {.screen}
        "override_attributes": {
          "osops": {
            "do_package_upgrades": true
          },
          [...]
          "glance": {
            "image_upload": false
          },
          [...]
          }
                            
    ~~~~

4.  Check out the cookbooks and specify **`v4.2.1`**.

    ~~~~ {.screen}
    /root# git clone https://github.com/rcbops/chef-cookbooks.git
    /root# cd chef-cookbooks
    /root/chef-cookbooks# git checkout v4.2.1
    /root/chef-cookbooks# git submodule init
    /root/chef-cookbooks# git submodule sync
    /root/chef-cookbooks# git submodule update
                            
    ~~~~

5.  Upload the cookbooks and the roles to the Chef server.

    ~~~~ {.screen}
    /root/chef-cookbooks# knife cookbook upload -a -o cookbooks

    /root/chef-cookbooks# knife role from file roles/*rb
                            
    ~~~~

6.  Stop the following OpenStack services on the backup Controller node,
    beginning with monit:
    -   monit
    -   keystone
    -   nova
    -   glance
    -   cinder
    -   haproxy
    -   keepalived

7.  Run chef-client on the backup node. You may have to run chef-client
    twice.
8.  After the last chef-client run that completes the upgrade, run the
    following command on the backup node:

    ~~~~ {.screen}
    # ip addr show lo
                                
    ~~~~

    It should generate output similar to the following:

    ~~~~ {.screen}
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN
         link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
         inet 127.0.0.1/8 scope host lo
            valid_lft forever preferred_lft forever 
         inet 169.254.123.1/30 scope host lo
            valid_lft forever preferred_lft forever                                
                                
    ~~~~

    In the correct configuration, shown here, it should include
    `169.254.123.1/30`{.filename}, which is the configured APIPA address
    that a Rackspace Private Cloud environment uses for HAProxy binding
    and communication,

9.  Run the following command on the active node to manually failover to
    the backup node.

    ~~~~ {.screen}
    # service keepalived restart
                                
    ~~~~

10. On the original active node, perform Steps 1-6 of this procedure and
    run chef-client.
11. After the last chef-client run that completes the upgrade, run the
    following command on the original active node:

    ~~~~ {.screen}
    # ip addr show lo
                                
    ~~~~

    As with the backup node in Step 2, it should generate output similar
    to the following:

    ~~~~ {.screen}
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN
         link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
         inet 127.0.0.1/8 scope host lo
            valid_lft forever preferred_lft forever 
         inet 169.254.123.1/30 scope host lo
            valid_lft forever preferred_lft forever                                
                                
    ~~~~

If at any point you need to manually remove the VIP from lo, use the
following command:

~~~~ {.screen}
# ip addr del <HAProxyVIP> dev lo
                            
~~~~

In an environment where the HAProxy VIP was `192.0.2.0/32`{.filename},
the command would be:

~~~~ {.screen}
# ip addr del 192.0.2.0/32 dev lo
                        
~~~~

Run **ip addr show lo** again to verify that the VIP has been removed
and run chef-client on the node again to re-run the upgrade.

### Restarting RabbitMQ {.title}

When a RabbitMQ cluster fails, it must be brought up in the reverse
order in which it went down, or the restart will fail. For example, if
RabbitMQ goes down on `controller1`{.filename} and then on
`controller2`{.filename}, the service should first be started on
`controller2`{.filename}, and then on `controller1`{.filename}.

### Intermittent failover failure {.title}

Occasionally, failover between HA Controller nodes may fail due to
multiple RabbitMQ processes existing on the secondary Controller node.
Restarting RabbitMQ will bring the cluster back online:

~~~~ {.screen}
# pkill -f rabbitmq; service rabbitmq-server restart
                
~~~~

OpenStack Orchestration and instance names {.title}
------------------------------------------

OpenStack Orchestration builds instance names based on the stack name,
which results in long instance names. Instance names that are longer
than 64 characters may cause the stack to fail to build. You should keep
stack names short to avert this issue.

### CentOS and RHEL challenges with advanced OpenStack Networking {.title}

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

### Snapshot deletion on CentOS {.title}

Setting `volume_clear`{.filename} in `cinder.conf`{.filename} to
`shred`{.filename} or `zero`{.filename} will cause snapshot deletion to
fail in OpenStack Grizzly installations on CentOS. Rackspace recommends
you set `volume_clear`{.filename} to `none`{.filename} until this issue
is resolved in OpenStack.

### OpenStack Metering visualization {.title}

Rackspace Private Cloud is currently using the patch referenced in
[Ceilometer bug
\#1093625](https://bugs.launchpad.net/ceilometer/+bug/1093625) to
address issues with OpenStack Metering visualization. If the underlying
packages are updated, you may experience patch issues. We will continue
to monitor the status of this bug for future releases.

### OpenStack service timeouts {.title}

OpenStack service timeouts cannot be configured, which makes it possible
for an OpenStack client to remain connected to a failed service for a
longer period than is desirable. If you cannot wait for the connection
to close, you can restart the service that is holding the connection.
For example, if the nova compute service has failed, restart it with
service nova-compute restart on Ubuntu or **service
openstack-nova-compute restart** on CentOS.

### Ephemeral and swap disks on RHEL {.title}

In RHEL-based clusters, ephemeral and swap disks cannot be used to
create a custom image. If you do so, you will be unable to boot an
instance. This is related to [Nova bug
\#1251152](https://bugs.launchpad.net/nova/+bug/1251152).

### Ceilometer packages fail to install {.title}

In some cases, the Ceilometer packages may not be correctly downloaded
or installed on the Compute nodes. On the primary Controller node,
follow this procedure to clean up the Compute nodes and re-install the
packages.

Note

The procedure as written is designed to be run on the primary Controller
node. The **dsh -g compute -c** command enables you to run the quoted
commands concurrently on all compute nodes. If desired, you can log into
each individual Compute node and run the quoted commands individually,
but this is not recommended in large clusters.

1.  Install the `python-swiftclient`{.filename},
    `python-warlock`{.filename}, and `babel`{.filename} packages.

    ~~~~ {.screen}
    # dsh -g compute -c "apt-get -y install python-swiftclient python-warlock babel"
    ~~~~

2.  Verify the installed packages. Review the output for
    `ERROR`{.computeroutput}. If there are no errors, the packages are
    correctly installed.

    ~~~~ {.screen}
    # dsh -g compute -c "apt-get -f install"
                
    ~~~~

3.  Run the following command to remove unneeded packages from the
    Compute nodes.

    ~~~~ {.screen}
    # dsh -g compute -c "apt-get -y autoremove"
    ~~~~

4.  Run chef-client again:

    ~~~~ {.screen}
    # dsh -g compute -c "chef-client"
                
    ~~~~

### Horizon is not installed correctly {.title}

In some cases on Ubuntu, Horizon packages are not installed correctly.
If Hypervisors tab does not contain pie charts, or if the Stats page on
the Resource Usage tab is not rendering graphs, Horizon has not been
correctly installed. To resolve this issue, you will uninstall Horizon
and django and run chef-client again.

1.  On the primary Controller node, uninstall Horizon and django:

    ~~~~ {.screen}
     # apt-get -y remove openstack-dashboard python-django-horizon && apt-get -y autoremove
                                 
    ~~~~

2.  Run **chef-client**.
3.  Log out of Horizon and log back in again.

You should now see the correct Hypervisors and Stats content.

In rare cases you may need to manually run Horizon's **collectstatic**
command to localize all of the Horizon resources. Run the following
command on the primary Controller node to perform this task.

~~~~ {.screen}
# /usr/share/openstack-dashboard/manage.py collectstatic --noinput
                
~~~~

