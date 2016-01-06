---
node_id: 3781
title: Brocade Vyatta vRouter FAQ
permalink: article/brocade-vyatta-vrouter-faq
type: article
created_date: '2013-11-18 18:51:25'
created_by: sameer.satyam
last_modified_date: '2015-05-21 01:1745'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

What is the network throughput on the Brocade Vyatta vRouter?
-------------------------------------------------------------

Since the Brocade Vyatta vRouter is a network appliance deployed on a
Cloud Server, the network throughput is dictated by the size of the
Cloud Server. Please refer to the
table [here](http://www.rackspace.com/cloud/servers/pricing/) for the
network throughput for different flavors of Cloud Servers.

What is the minimum amount of RAM needed to run a Vyatta?
---------------------------------------------------------

The minimum RAM size needed to run a vRouter is 1 GB.

Can you assign more than one IP address to the Vyatta's public interface?
-------------------------------------------------------------------------

Each Vyatta appliance comes with one public IPv4 address assigned. Up to
four additional public IPv4 addresses can be allocated (for a total of
5) . Please see this article for more details: [Requesting Additional
IPv4 Addresses for First Generation and Next Generation Cloud
Servers](/knowledge_center/article/requesting-additional-ipv4-addresses-for-first-and-next-generation-cloud-servers)

Can Vyatta be used along with RackConnect?
------------------------------------------

No. RackConnect users may not use the vRouter at this time.

Is Vyatta available for Managed Operations service level accounts?
------------------------------------------------------------------

Yes. The vRouter is available for the Managed Operations service level.

Can the Vyatta be configured in a redundant mode (active/backup Highly available configuration)?
------------------------------------------------------------------------------------------------

The Vyatta appliance supports VRRP for High-availability. However,
Rackspace cannot support High Availability of Vyatta over the Public Net
interface because &ldquo;Shared IP address&rdquo; is not available over PublicNet at
this time. You can, however, setup Vyatta to be Highly Available on the
Cloud Networks interface since Shared IP addresses are supported on
Cloud Networks.

Can I add or remove interfaces from a live Vyatta device ?
----------------------------------------------------------

No. Do not add/disconnect networks . This will cause serious issues with
networking on the Vyatta and the only recourse will be to rebuild the
Vyatta.

I cannot log into the Vyatta using username &lsquo;root&rsquo; and the password that was set when the Vyatta was created. What is wrong?
----------------------------------------------------------------------------------------------------------------------------

Please log in with username &lsquo;vyatta&rsquo; to login to the appliance.

What actions are supported on Vyatta through the control panel?
---------------------------------------------------------------

Control panel actions and limitations are described at the following
link:[Vyatta Network Appliance: Supported Actions Through Control
Panel](/knowledge_center/article/vyatta-network-appliance-supported-actions-through-control-panel)

