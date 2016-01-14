---
node_id: 4216
title: RackConnect v3.0 limitations
type: article
created_date: '2014-08-29 13:16:51'
created_by: juan.perez
last_modified_date: '2014-11-17 17:3824'
last_modified_by: rose.contreras
product: RackConnect
body_format: tinymce
---

**Applies to:** RackConnect v3.0

The following table describes the limitations of RackConnect v3.0. 

 

Limitation

Details

**Cloud account**

-   A single cloud account cannot be associated with both a RackConnect
    v3.0 configuration and a RackConnect v2.0 configuration.

****Cloud Networks****

-   Cloud Networks limitations also apply to cloud networks that are
    associated with RackConnect v3.0. For example, Cloud Networks is
    currently limited to 10 isolated networks and up to 250 cloud
    servers per network; these limitations also apply to cloud networks
    that are associated with RackConnect v3.0. For a list of current
    Cloud Networks limitations, see the articles [Create an Isolated
    Cloud
    Network](http://www.rackspace.com/knowledge_center/article/create-an-isolated-cloud-network) and
    [Cloud Networks
    FAQ](http://www.rackspace.com/knowledge_center/article/cloud-networks-faq).

-   Currently, only cloud servers configured with a single cloud network
    are supported.

-   Avoid using network ranges for your cloud networks that overlap with
    the Rackspace public cloud ServiceNet IP address ranges of
    10.176.0.0/12 and 10.208.0.0/12. Also avoid using network ranges
    that are already in use on the dedicated-side of your network or
    that consist of public IP adresses. Other than the preceding caveats
    we recommend that you use network ranges from within the standard
    private IPv4 address spaces of 10.0.0.&ndash;10.255.255.255,
    172.16.0.&ndash;172.31.255.255, or 192.168.0.&ndash;192.168.255.255 for your
    cloud networks. We also recommend that you select a /24 CIDR subnet
    mask to simplify management, because a /24 CIDR is large enough to
    support 250 cloud servers (the cloud servers limit per network). If
    you are planning to build and delete a large number of cloud servers
    every hour, then you might want to use a subnet that allows for a
    larger number of cloud servers, such as a /23 CIDR, to avoid
    potential issues with cloud network IP address availability.

-   You cannot have a single network subnet that spans both your cloud
    and dedicated environments. To clarify, your dedicated-side's
    network subnets on your dedicated side must be on a different subnet
    than your cloud network's subnet.

-   RackConnect v3.0 cloud servers are automatically assigned their
    cloud network subnet's first IP address as the default gateway. The
    gateway IP address lives on the RackConnect v3.0 connected network
    device, and is manually configured by Rackspace during the
    RackConnect v3.0 implementation process.

**RackConnect v3.0**

-   Not all of the Rackspace public cloud products are compatible with
    RackConnect v3.0 cloud servers. To verify which offerings are
    supported, see the article, [RackConnect v3.0 Compatibility
    Matrix](http://www.rackspace.com/knowledge_center/article/rackconnect-v30-compatibility-matrix).
-   QoS: Traffic that traverses across your RackConnect v3.0 link
    between your cloud and dedicated environments is now bandwidth
    limited by Quality of Service (QoS) policies. By default, these QoS
    policies are set to limit bandwidth throughput to 100 Mbps (megabits
    per second), but with Rackspace approval, they may be increased. If
    you have need for more than 100 Mbps of bandwidth, please [contact
    us](http://www.rackspace.com/knowledge_center/support) for details
    on potential one-off solutions.
-   As with RackConnect v2.0, RackConnect v3.0 bandwidth might be
    limited by the capabilities of the Cloud Servers flavors that you
    are running, your network device's capabilities, and your dedicated
    server's capabilities.
-   The default setting for RackConnect v3.0 access between cloud and
    dedicated network segments is to restrict all communication. During
    the RackConnect v3.0 implementation process and afterwards, you can
    provide us with details on how you want the access between your
    network segments configured. Alternatively, you can also setup any
    necessary firewall rules on your own by using the Firewall Manager
    feature available in the [MyRackspace
    Portal](https://my.rackspace.com/).
-   Your devices must be deployed in a region supported by RackConnect
    v3.0. The regions supported, as of October 2014, are DFW, IAD, ORD,
    LON, HKG, and SYD.

**RackConnect v3.0 API**

-   Cloud Servers metadata options are no longer available with
    RackConnect v3.0. Metadata options for RackConnect v3.0 cloud
    servers have been superseded by the new RackConnect v3.0 API.
-   The RackConnect v3.0 API must be used to provision public IP
    addresses to your cloud servers and to add cloud servers to load
    balancer pools.
-   Currently, you can provision only one public IP address to a
    RackConnect v3.0 cloud server.

**RackConnect v3.0 Cloud Servers**

-   IPv6 is not currently supported.
-   First Generation Cloud Servers are not supported. Next Generation
    Standard Cloud Servers, [Performance 1 Cloud
    Servers](http://www.rackspace.com/knowledge_center/article/what-is-new-with-performance-cloud-servers),
    and [Performance 2 Cloud
    Servers](http://www.rackspace.com/knowledge_center/article/what-is-new-with-performance-cloud-servers)
    are supported.
-   Currently, PublicNet network interfaces are not supported.
    Optionally, a single *Network Address Translation* (NAT) from a
    dedicated public IP address to a cloud server's cloud network IP
    address may be configured. This is also known as provisioning a
    public IP address to a RackConnect v3.0 cloud server.
-   Currently, only cloud servers configured with a single cloud network
    are supported.
-   ServiceNet network interfaces are optional for [Managed
    Infrastructure](http://www.rackspace.com/managed-cloud/) service
    level customers, but are required for [Managed
    Operations](http://www.rackspace.com/managed-cloud/) service level
    customers.
-   Cloud Servers limitations also apply to RackConnect v3.0 cloud
    servers. For a list of current Cloud Servers limitations, see
    the [Cloud Servers:
    FAQ](http://www.rackspace.com/knowledge_center/product-faq/cloud-servers).
    Cloud Server bandwidth limitations are described in the [Rackspace
    Public Cloud
    Pricing](http://www.rackspace.com/cloud/public-pricing/#cloud-servers) article.
-   Currently, you cannot have multiple cloud network IP addresses on
    individual RackConnect v3.0 cloud servers.
-   Currently, you cannot move, change, add, or remove IP addresses from
    RackConnect v3.0 cloud servers.

If you have any questions, we are always here to help, reach out to
us.  Contact information is available on the [Contact
Us](http://www.rackspace.com/knowledge_center/support) page.

 

