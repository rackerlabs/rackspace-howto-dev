---
node_id: 4271
title: RackConnect v3.0 - FAQ
type: article
created_date: '2014-09-26'
created_by: Juan Perez
last_modified_date: '2016-01-20'
last_modified_by: Stephanie Fillmon
product: RackConnect
body_format: full_html
---

**Applies to:** RackConnect v3.0. For questions on RackConnect v2.0, see
[RackConnect 2.0 -
FAQ](/how-to/rackconnect-20-faq).

#### Can I allocate multiple cloud networks to a single RackConnect v3.0 cloud server?

No. We currently support only one cloud network per cloud server.

#### Can I assign more than one cloud network IP address to my RackConnect v3.0 cloud servers?

No. For each cloud server, we currently only support:

-   One cloud network
-   One IP address per cloud network
-   One public IP address network address translation (NAT) per cloud
    server

#### Can I upgrade my RackConnect v2.0 environment to RackConnect v3.0?

Not yet, but we are working on a migration path. Initially, we plan to
offer you the ability to associate a *new* cloud account with your
existing RackConnect v2.0 configuration, which will enable you to
experience RackConnect v3.0 without deactivating your existing
RackConnect v2.0 environment. Note that only *next generation cloud
servers* will be compatible with the migration process to RackConnect
v3.0. We will provide more details about this process as they become
available.

#### Can I use a Brocade ADX 1000 as my RackConnect v3.0 edge device?

No. Because of access list limitations, we currently support the Brocade
ADX 1000 devices only in the connected device role. For a full list of
network devices that are compatible with RackConnect v3.0, see
[RackConnect Network Device
Comparison](/how-to/rackconnect-network-device-comparison).

#### Does RackConnect v3.0 support IPv6?

Not yet &mdash; but support for IPv6 is anticipated for early 2016.

#### Does RackConnect v3.0 support Managed Colocation environments?

Network devices in a Managed Colocation environment are supported only
if the network devices are managed by the Rackspace Network Security
team. Customer-managed network devices are not supported. For more
details about RackConnect v3.0 compatibility with other Rackspace
offerings, see [RackConnect v3.0 Compatibility
Matrix](/how-to/rackconnect-v30-compatibility).

#### How do I get RackConnect v3.0?

The answer varies based on whether you are an existing Rackspace
customer:

-   If you are new to Rackspace, contact a member of our Sales team
    for help. For details about how to contact our Sales teams, go to
    [Contact
    Rackspace](http://www.rackspace.com/information/contactus/).
-   If you are an existing Rackspace cloud-only customer, contact a
    member of our Sales team for help. For details about how to contact
    our Sales team, go to [Contact
    Rackspace](http://www.rackspace.com/information/contactus/).
-   If you are an existing Rackspace dedicated-only customer, contact
    your account manager for help in getting RackConnect v3.0 set up in
    your environment.

#### Is it possible to attach a RackConnect v3.0 cloud network to pre-existing cloud servers?

Yes, but with the following caveats:

Note that *pre-existing cloud servers* refers to cloud servers that were
built before RackConnect v3.0 was associated with the cloud account.

-   For the best possible experience, we recommend using a clean cloud
    account (meaning a cloud account with no pre-existing cloud servers)
    with RackConnect v3.0.
-   If the pre-existing cloud servers are using PublicNet, you must
    remove PublicNet before attempting to add a RackConnect v3.0 cloud
    network to the cloud server.
-   If you are a Managed Operations customer and need help detaching
    PublicNet, contact your Rackspace support team for assistance.
-   If the pre-existing cloud servers are using ServiceNet, the
    ServiceNet IP address will change because ServiceNet will
    be detached and then re-attached to apply the appropriate
    security policies. Note that ServiceNet in RackConnect v3.0 is
    highly restricted and cannot be used for communication between
    cloud servers.

#### What network subnet (CIDR) should I assign to my RackConnect v3.0 cloud network?

See the [Cloud
Networks](/how-to/rackconnect-v30-limitations)
section of [RackConnect v3.0
limitations](/how-to/rackconnect-v30-limitations).

#### What requirements must be met to implement RackConnect v3.0 in my environment?

For the full list of requirements, see [RackConnect v3.0
requirements](/how-to/rackconnect-v30-requirements).

#### Whom do I contact for help with RackConnect v3.0?

Because RackConnect spans both your cloud and dedicated environments,
you can contact your cloud or dedicated hosting support teams for help
with RackConnect. If you are certain that the issue you are experiencing
is directly related to your cloud servers, we recommend contacting your
cloud hosting team first. However, if you are certain that the issue is
related to your network device, we recommend contacting your dedicated
hosting team first. For details about how to contact your support teams,
visit the [Contact
Us](/how-to/support) page.

#### Why do I receive 403 Forbidden HTTP status code responses when I try to build RackConnect v3.0 cloud servers by using the Cloud Servers API or the nova client?

By default, when you use the Cloud Servers API or nova client to build
cloud servers, the servers are built with a PublicNet network. However,
RackConnect v3.0 does not support PublicNet and restricts you from
building cloud servers with PublicNet attached on RackConnect v3.0
linked cloud accounts. This restriction is likely the reason that you
are receiving `403 Forbidden` responses. Following are details for
resolving this error:

-   When building a cloud server using the nova client `boot` command,
    include the `--no-public` option to prevent the PublicNet network
    from being attached to the server. Note that you can also use the
    `--no-service-net` option with the nova client `boot` command to
    keep the ServiceNet network from being attached to a cloud server.
    However, consider that ServiceNet is required for cloud servers
    created in cloud accounts with a [Managed
    Operations](http://www.rackspace.com/managed-cloud/) service level.
-   With the Cloud Servers API, specify the cloud network that you want
    to attach to the cloud server. If you specify one or more networks,
    your server is attached to only those networks. See the [Create your
    first
    Server](https://developer.rackspace.com/docs/cloud-servers/v2/developer-guide/#document-getting-started/create-server-intro)
    section of the Cloud Servers v2 Developer Guide for
    more information.


