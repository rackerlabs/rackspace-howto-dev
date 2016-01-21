---
node_id: 3183
title: RackConnect Network Device Comparison
type: article
created_date: '2012-11-07'
created_by: Juan Perez
last_modified_date: '2015-07-14'
last_modified_by: Kelly Holcomb
product: RackConnect
---

**APPLIES TO**: RackConnect v3.0, RackConnect v2.0

The following charts provide a detailed comparison of the network
devices available for use with your RackConnect configuration.
RackConnect and RC are used interchangeably.

** RackConnect Network Device Comparison**
------------------------------------------

**Features**

**ASA 5505 Sec+**

**ASA 5510 Sec+**

**ASA 5520**

**ASA 5540**

**ASA 5550**

**ASA 5515-X**

**ASA 5525-X**

**ASA 5545-X**

**ASA 5555-X**

**Brocade ADX 1000**

**F5 1600**

**F5 3600**

Load Balancer Pools

No

No

No

No

No

No

No

No

No

Yes

Yes

Yes

Maximum Concurrent Connections

25,000

130,000

280,000

400,000

650,000

250,000

500,000

750,000

1 Million

 4&ndash;8 Million

1 Million

8 Million

Maximum SSL TPS \*

   &mdash;

   &mdash;

 &mdash;

 &mdash;

 &mdash;

 &mdash;

 &mdash;

 &mdash;

 &mdash;

 7,250&ndash;14,500

5,000

10,000

Maximum Concurrent SSL Connections

&mdash;

&mdash;

&mdash;

&mdash;

&mdash;

&mdash;

&mdash;

&mdash;

&mdash;

 64,000

1 Million

1 Million

Stateful Firewall \*\*

Yes

Yes

Yes

Yes

Yes

Yes

Yes

Yes

Yes

 Yes (but not supported as a firewall)

No

No

VPN Tunneling

Yes

Yes

Yes

Yes

Yes

Yes

Yes

Yes

Yes

 No

No

No

High Availability Option

Yes

Yes

Yes

Yes

Yes

Yes

Yes

Yes

Yes

 Yes

Yes

Yes



**RackConnect Specific Overview**
---------------------------------

**Features**

**Maximum RC Cloud Servers\*\*\***

**RC Net Device Config. Options**

**RackConnect v2.0 Compatible**

**RackConnect v3.0**

****Compatible****

**Maximum Throughput\*\*\*\*
(Cloud&lt;-&gt;Dedicated)
(Cloud&lt;-&gt;Internet)**

**ASA 5505 Sec+**

5

Edge or Edge+Connected

Yes

Yes

150 Mbps

**ASA 5510 Sec+**

25

Edge or Edge+Connected

Yes

Yes

300 Mbps

**ASA 5520**

50

Edge or Edge+Connected

Yes

Yes

450 Mbps

**ASA 5540**

80

Edge or Edge+Connected

Yes

Yes

650 Mbps

**ASA 5550**

100+

Edge or Edge+Connected

Yes

Yes

1 Gbps

**ASA 5515-X**

50

Edge or Edge+Connected

Yes

Yes

1.2 Gbps

**ASA 5525-X**

100+

Edge or Edge+Connected

Yes

Yes

2 Gbps

**ASA 5545-X**

100+

Edge or Edge+Connected

Yes

Yes

3 Gbps

**ASA 5555-X**

100+

Edge or Edge+Connected

Yes

Yes

4 Gbps

**Brocade ADX 1000**

 100+

Connected Only

No (not in RackConnect edge or connected device roles)

Yes

 2&ndash;9 Gbps

**F5 1600**

100+

Connected or Edge+Connected

Yes

Yes

In: 500 Mbps
Out: 500 Mbps

**F5 3600**

100+

Connected or Edge+Connected

Yes

Yes

In: 1 Gbps
Out: 1 Gbps

**\* License upgrade may be required to reach Maximum SSL TPS**
**\*\* We recommend utilizing a Cisco ASA as the RackConnect Edge Device
Type**
**\*\*\* Maximum Cloud Servers&rsquo; Guidelines based on internal testing.
Actual results may vary by production load and Edge Device Type.**
**\*\*\*\*  RackConnect Throughput limited by RackConnect Switching
Infrastructure connectivity: Maximum of 1 Gbps Theoretical**



