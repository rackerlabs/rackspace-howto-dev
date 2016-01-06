---
node_id: 3545
title: Rackspace Private Cloud v. 4.0 Release Notes
permalink: article/rackspace-private-cloud-v-40-release-notes
type: article
created_date: '2013-06-20 15:24:28'
created_by: Karin Levenstein
last_modified_date: '2015-06-10 18:4956'
last_modified_by: kyle.laffoon
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

Rackspace has developed a fast, free, and easy way to install a
Rackspace Private Cloud powered by OpenStack in any data center. This
method is suitable for anyone who wants to install a stable, tested, and
supportable OpenStack-powered private cloud, and can be used for all
scenarios from initial evaluations to production deployments.

Rackspace Private Cloud v 4.0 supports the [Grizzly release of
OpenStack](http://www.openstack.org/software/grizzly/).

**Note**: Rackspace Private Cloud has been updated to v 4.1.2. [Refer to
the v 4.1.2 release notes for information about the changes made in that
release](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-412-release-notes-0).

Intended Audience
-----------------

This document describes the updates in Rackspace Private Cloud v 4.0 and
any known issues in the product. You should already be familiar with
Rackspace Private Cloud Software and have prior knowledge of OpenStack
and cloud computing, basic Linux administration skills, and a side of
bacon. :)

Document Change History
-----------------------

This version of the Rackspace Private Cloud Release Notes replaces and
obsoletes all previous versions. The most recent changes are described
in the table below:

Revision Date

Summary of Changes

June 25, 2013

-   Rackspace Private Cloud Software v 4.0 release.

July 1, 2013

-   Added information about a known issue related to Knife.

September 4, 2013

-   Added information about a known issue related to CentOS.

Additional Resources
--------------------

-   [Rackspace Private Cloud Software Home
    Page](http://www.rackspace.com/cloud/private/)
-   [Rackspace Private Cloud Knowledge
    Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud)
-   [Rackspace Private Cloud
    Forums](http://privatecloudforums.rackspace.com/)

Contact Rackspace
-----------------

For more information about sales and support, contact us at
[opencloudinfo@rackspace.com](mailto:opencloudinfo@rackspace.com). For
feedback on the product and the documentation, contact us at
[RPCFeedback@rackspace.com](mailto:RPCFeedback@rackspace.com). For the
documentation, you can also leave a comment at [the Knowledge
Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud).

What's New in Rackspace Private Cloud v 4.0
-------------------------------------------

Rackspace Private Cloud v 4.0 has the following new features.

-   [Installing Rackspace Private
    Cloud](#installing "Installing Rackspace Private Cloud")
-   [OpenStack Grizzly](#grizzly "OpenStack Grizzly")
-   [OpenStack Networking](#quantum "OpenStack Networking")
-   [OpenStack Identity v2 with Active Directory and
    LDAP](#keystone-ldap-ad "OpenStack Identity v2 with Active Directory and LDAP")
-   [OpenStack Block Storage Third-Party
    Vendors](#cinder "OpenStack Block Storage Third-Party Vendors")
-   [VMWare VMDK Image
    Import](#vmware-vmdk "VMWare VMDK Conversion and Amazon AMI Image Import")
-   [Cloud Files with OpenStack Image
    Storage](#glance-cloud-files "Cloud Files with OpenStack Image Storage")
-   [OpenStack Ceilometer](#ceilometer "OpenStack Ceilometer")

### Installing Rackspace Private Cloud

Rackspace Private Cloud v 4.0 is deployed through a series of bash
scripts in the following stages:

1.  Install Chef server on a node in the environment.
2.  Download the latest cookbooks to the Chef server.
3.  Install chef-client on each node that will be managed by Chef in
    your OpenStack cluster.
4.  Use Chef to create Controller nodes, Compute nodes, and more.

For a detailed description of the prerequisites and process, refer to
[Installation Prerequisites and
Concepts](http://docs.rackspace.com/rpc/api/v4/rackspace-private-cloud-installation/content/rpc-getstarted-prereqs.html)
and the [Rackspace Private Cloud Installation
Guide](http://docs.rackspace.com/rpc/api/v4/rackspace-private-cloud-installation/content/rpc-common-front.html).

The OpenCenter installer scripts are still available; however,
OpenCenter only supports the Folsom release. An environment installed
with OpenCenter can be upgraded to Grizzly, but the results have not
been tested. For more information, refer to [Upgrading Your Private
Cloud](http://www.rackspace.com/knowledge_center/article/upgrading-your-private-cloud).

### OpenStack Grizzly

Rackspace Private Cloud Software now installs and supports the OpenStack
Grizzly release. Existing Folsom environments installed with the
Rackspace Private Cloud cookbooks can also be updated to Grizzly with
the procedure documented in [Upgrading Your Private
Cloud](http://www.rackspace.com/knowledge_center/article/upgrading-your-private-cloud).

For detailed information about what is included in Grizzly, refer to the
[Grizzly release
notes](https://wiki.openstack.org/wiki/ReleaseNotes/Grizzly).

### OpenStack Networking

Rackspace Private Cloud Software now supports OpenStack Networking
(Neutron, formerly Quantum). The Networking configuration provided by
the Rackspace Private Cloud cookbooks allows you to choose between VLAN
or GRE isolated networks, both provider- and tenant-specific. From the
provider side, an administrator can also create a flat network. Concepts
and configuration are described in [Configuring OpenStack
Networking](http://www.rackspace.com/knowledge_center/article/configuring-openstack-networking).

Currently, you cannot use Neutron routers, and the quantum-server
service is not HA.

### OpenStack Identity v2 with Active Directory and LDAP

Rackspace Private Cloud Software now supports using Active Directory and
LDAP as a backend for OpenStack Identity (Keystone). For instructions
about configuring your environment for Active Directory and LDAP, refer
to [Active Directory and LDAP
Integration](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-active-directory-and-ldap-integration).

### OpenStack Block Storage Third-Party Vendors

Rackspace Private Cloud Software supports using OpenStack Block Storage
(Cinder) with the following third-party storage vendors:

-   EMC
-   NetApp
-   Solidfire

For instructions about configuring your environment for these vendors,
refer to [Configuring OpenStack Block
Storage](http://www.rackspace.com/knowledge_center/article/configuring-openstack-block-storage).

### VMWare VMDK Conversion and Amazon AMI Image Import

Rackspace has developed a tool to convert single-disk Linux VMDK images
to OpenStack-compatible qcow2 images. The conversion is accomplished by
means of a Python script available at
[`https://github.com/rcbops/support-tools/tree/master/vmdk-conversion`{.uri}](https://github.com/rcbops/support-tools/tree/master/vmdk-conversion).
For instructions about using the tool, refer to [Converting VMDK Linux
Images](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-software-creating-an-instance-in-the-cloud#vmdk-image).

Multi-disk and Windows image conversions are not available at this time.

Amazon AMI images can also be imported into Glance. For instructions
about importing AMI images, refer to [Uploading AMI
Images](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-software-creating-an-instance-in-the-cloud#ami-image).

### Cloud Files with OpenStack Image Storage

You can configure Rackspace Cloud Files as a backend for OpenStack Image
Storage (Glance). For instructions about configuring your environment
for Cloud Files, refer to [Configuring OpenStack Image
Storage](http://www.rackspace.com/knowledge_center/article/configuring-openstack-image-storage).

### OpenStack Ceilometer

The Rackspace Private Cloud installation includes OpenStack Ceilometer
for the OpenStack cluster. In this installation, Ceilometer is only
accessible through the API. For information about the Ceilometer API,
refer to the [Ceilometer Developer
Documentation](http://docs.openstack.org/developer/ceilometer/).
Ceilometer is automatically included when you create your Controller and
Compute nodes, and no additional configuration is required.

**NOTE**: The Ceilometer API cannot co-exist on a node with haproxy.

Known Issues
------------

The following issues have been identified in Rackspace Private Cloud v.
4.0 and v 4.1.2.

### Updating Cookbooks with knife cookbook upload -a -o

When updating to the v 4.0.0 cookbooks, Chef Server might fail to upload
the cookbooks on the first attempt. If this happens, run
`knife cookbook upload -a -o again`. This is related to [known Chef
issue CHEF-4330](http://tickets.opscode.com/browse/CHEF-4330).

### RHEL and CentOS Challenges With Advanced OpenStack Networking {.title}

When using OpenStack Networking (Neutron), Controller nodes with
Networking features and standalone Networking nodes require namespace
kernel features that are not available in the default kernel shipped
with RHEL 6.4, CentOS 6.4, and older versions of these operating
systems. More information about Neutron limitations is available in the
[OpenStack
documentation](http://docs.openstack.org/grizzly/openstack-network/admin/content/ch_limitations.html),
and more information about RedHat-derivative kernel limitations is
provided in the [RDO
FAQ](http://openstack.redhat.com/Frequently_Asked_Questions#For_which_distributions_does_RDO_provide_packages.3F).

If you require OpenStack Networking using these features, Rackspace
recommends that you consider the RHEL and CentOS patches, or use Ubuntu
12.04 for the Controller and Networking nodes.

### Snapshot Deletion on CentOS

Setting **volume\_clear** in `cinder_conf` to **shred** or **zero** will
cause snapshot deletion to fail in OpenStack Grizzly installations on
CentOS. Rackspace recommends you set **volume\_clear** to none until
this issue is resolved in OpenStack.

### OpenStack Service Timeouts

OpenStack service timeouts cannot be configured, which makes it possible
for an OpenStack client to remain connected to a failed service for a
longer period than is desirable. If you cannot wait for the connection
to close, you can restart the service that is holding the connection.
For example, if the nova compute service has failed, restart it with
**service nova-compute restart** on Ubuntu or **service
openstack-nova-compute restart** on CentOS.

Resolved Issues
---------------

The following issues have been resolved in Rackspace Private Cloud v 4.0
and v 4.1.2.

### HA MySQL Replication Issues

An issue with MySQL replication that was caused by logging has been
resolved. (Issue \#327)

### HA Glance Replication Issues

An issue that prevented successful HA Glance replication has been
resolved. (Issue \#328)

### Horizon Dashboard Admin Cookie Issues

Cookie issues associated with the admin user were resolved in the
Grizzly release of OpenStack.

### Intermittent collectd Issues

Issues with intermittent collectd failures with monitoring processes or
after performing a failover have been resolved, that these failures
should no longer occur.

### Keystone Connection Issues for Nova, Cinder, and Glance APIs

An issue that caused Nova, Cinder, and Glance APIs to attempt to connect
to Keystone on an invalid IP has been resolved. (Issue \#368 and \#369)

### Ubuntu and Kernel Version Compatibility With KVM

Issues with OpenStack Ubuntu and KVM where a kernel version of 3.2.n was
required for Ubuntu 12.04 and 12.04.1 have been resolved. This issue was
related to [Ubuntu bug
\#1029430](https://bugs.launchpad.net/ubuntu/+source/libvirt/+bug/1029430).

### VNC and HA Infrastructure

Instance VNC in the Horizon dashboard now works correctly in
environments with HA Infrastructure nodes.

