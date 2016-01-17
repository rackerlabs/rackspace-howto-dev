---
node_id: 4452
title: RackConnect RegionLink FAQ
type: article
created_date: '2014-12-04'
created_by: Sameer Satyam
last_modified_date: '2014-12-12'
last_modified_by: Kyle Laffoon
product: RackConnect
body_format: tinymce
---

Get quick answers to common questions about RackConnect RegionLink.

-   [What is RackConnect RegionLink?](#Q1)
-   [Why do you need it?](#Q2)
-   [What are some common use cases for this service?](#Q3)
-   [What are the benefits of the interregional solution?](#Q4)
-   [Which Rackspace customers can use this service?](#Q5)
-   [In which data centers is this service available?](#Q6)
-   [Is a dedicated aggregation (customer edge) device needed to use
    this service?](#Q8)
-   [Is the traffic encrypted?](#Q9)
-   [What kind of speeds are supported?](#Q10)
-   [Is redundancy built in to the solution?](#Q11)
-   [What is the SLA for this service?](#Q12)
-   [For an MPLS L3 VPN connection, how many VPN prefixes can be
    exchanged between the sites?](#Q13)
-   [Is IPv6 traffic supported?](#Q14)
-   [How do I order the service, and what is the pricing?](#Q15)

#### [](){#Q1}What is RackConnect RegionLink? {#Inter-regionconnectivityFAQ-WhatistheInter-regionconnectivityservice?}

RackConnect RegionLink is a Limited Availability service that enables
Dedicated Hosting customers to connect infrastructure that they have
deployed across two or more Rackspace data centers. The service uses
multiprotocol label switching (MPLS) virtual private network (VPN)
across Rackspace Backbone and enables connectivity between resources at
Layer 2 or Layer 3.

#### [](){#Q2}Why do you need it? {#Inter-regionconnectivityFAQ-Whydocustomersneedit?}

Some Dedicated Hosting customers cannot tolerate the risk of unexpected
downtime. To mitigate the risk of an outage caused by a problem with a
single Rackspace region, customers might want to distribute their
compute resources across multiple Rackspace regions. Interregional
connectivity is a way to transfer data between Rackspace regions at
lower latency and with better throughput than over the Internet.

#### [](){#Q3}What are some common use cases for this service? {#Inter-regionconnectivityFAQ-Whataretheusecases?}

Customers might want to establish a backup or high availability
duplicate of an existing configuration (for example, database
replication) or geographically distribute applications closer to their
customers to minimize latency and improve network performance.

#### [](){#Q4}What are the benefits of the interregional solution? {#Inter-regionconnectivityFAQ-WhatarethebenefitsoftheInter-regionsolution?}

-   Bypasses multiple layers of network devices, which improves latency
-   Better option than using upgraded firewalls just for VPN throughput
-   Built-in redundancy
-   Fully managed and supported by Rackspace

#### [](){#Q5}Which Rackspace customers can use this service? {#Inter-regionconnectivityFAQ-Whatkindofcustomersisitfor?}

The RackConnect RegionLink service is available only for Dedicated
Hosting customers at this time.

#### [](){#Q6}In which data centers is this service available? {#Inter-regionconnectivityFAQ-WhichDatacentersisthisserviceavailablein?}

#### The service is curently available in all three US data centers (IAD, DFW, and ORD).

#### [](){#Q8}Is a dedicated aggregation (customer edge) device needed to use this service? {#Inter-regionconnectivityFAQ-IsaDedicatedAggregationdeviceneededtousethisservice?}

Yes, a dedicated aggregation, or customer edge (CE) device is needed at
this time.
We recommend one of the following devices:

-   Cisco 4948E
-   Arista 7050
-   Cisco Nexus 3064

#### [](){#Q9}Is the traffic encrypted? {#Inter-regionconnectivityFAQ-Isthetrafficsecure?}

The service does not provide any encryption. It is purely an MPLS VPN
connection (L2/L3). The traffic rides across the Rackspace backbone all
the way through without hitting the Internet.

#### [](){#Q10}What kind of speeds are supported? {#Inter-regionconnectivityFAQ-Whatkindofspeedsaresupported?}

At launch, the service supports connectivity speeds of 100 Mbps, 500
Mbps, and 1 Gbps. Faster speeds will be supported on a case-by-case
basis.

#### [](){#Q11}Is redundancy built in to the solution? {#Inter-regionconnectivityFAQ-Isthereredundancybuiltintothesolution?}

Yes, there are two connectivity options into the backbone from the
dedicated aggregation (customer edge) device. Both options use
two uplinks to the data center provider edge (PE) device.

#### [](){#Q12}What is the SLA for this service? {#Inter-regionconnectivityFAQ-WhatistheSLAforthisservice?}

The SLA varies based on which of the above redundancy option the
customer chooses. If the customer wants only one Dedicated Aggr. device,
the SLA will be limited to a 1 hour hardware replacement time for the
Aggr. device. If the customer uses two CE devices we have an SLA of 99.9
% connection availability between data center edge devices. See
[Rackspace RackConnect RegionLink Service Level
Guaranty](http://www.rackspace.com/information/legal/rackconnect_regionlink)
for the SLA.

#### [](){#Q13}For an MPLS L3 VPN connection, how many VPN prefixes can be exchanged between the sites? {#Inter-regionconnectivityFAQ-ForanMPLSL3VPNconnection,howmanyVPNprefixescanbeexchangedbetweenthesites?}

Up to 100 prefixes can be exchanged.

#### [](){#Q14}Is IPv6 traffic supported? {#Inter-regionconnectivityFAQ-IsIPv6trafficsupported?}

No. Only IPv4 is supported at this time.

#### [](){#Q15}How do I order the service, and what is the pricing? {#Inter-regionconnectivityFAQ-Iwanttoseeasummaryofwhatwearelaunching}

Contact your Rackspace account representative for ordering and pricing
information.
