---
node_id: 1179
title: Requesting additional IPv4 addresses for Cloud Servers
permalink: article/requesting-additional-ipv4-addresses
type: article
created_date: '2011-08-08 17:28:23'
created_by: RackKCAdmin
last_modified_date: '2015-10-13 19:1158'
last_modified_by: kyle.laffoon
products: Cloud Servers
body_format: tinymce
---

Rackspace offers the ability to add IPv4 addresses to Cloud Servers for
a fee. If you wish to obtain an additional IPv4 address for your server
please open a ticket through the Support section of the Cloud Control
Panel to get policy information and approval.

### Conditions

Due to the global shortage of IPv4 address space, Rackspace currently
only offers additional IPv4 addresses for the following purposes:

1.  SSL on Cloud Servers
2.  NAT (Network Address Translation) on a [Brocade Vyatta
    vRouter](http://www.rackspace.com/cloud/servers/vrouter/)

### Pricing

The rates for additional IP addresses vary by region. Discuss rates for
your region with the Support team during your set up.

### Requesting additional IP addresses

Once approved for an additional IP address you'll be asked to supply the
following information:

#### Cloud Servers

For an additional IPv4 address on a Cloud server you will need to
provide:

-   The name of the server for which you would like to add the IP
    address.
-   The SSL certificate. The certificate must have been signed by a
    valid Certificate Authority; self-signed certificates are not
    accepted.

#### Brocade Vyatta vRouters

For an additional IPv4 address on a Brocade Vyatta vRouter you will need
to confirm that you intend to use the Additional IPv4 address for the
purpose of NAT.

Please note that we cannot allocate more than 4 additional IPv4
addresses to a single Cloud Server or to a Brocade Vyatta vRouter. This
gives each Cloud Server or the Brocade Vyatta vRouter a maximum capacity
of five (5) IPv4 addresses including the originally assigned public IP
address.

