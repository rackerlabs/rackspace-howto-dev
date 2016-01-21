---
node_id: 4165
title: Brocade Vyatta vRouter configuration guide
type: article
created_date: '2014-07-30'
created_by: Sameer Satyam
last_modified_date: '2016-01-15'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
product_url: cloud-servers
---

The Brocade Vyatta vRouter is a network appliance that you can spin up
in the Rackspace public cloud. It acts as a firewall, VPN gateway,
router, and NAT device. You read more about the Brocade Vyatta vRouter
at the \[Rackspace virtual cloud
servers\](http://www.rackspace.com/cloud/servers/vrouter). The following
articles provide detailed configurations for the Brocade Vyatta vrouter:
\[Brocade Vyatta vRouter configuration
guide\](https://www.rackspace.com/knowledge\_center/node/4165/revisions/20104/view)
\[Configuring a policy-based IPsec site-to-site VPN on a Vyatta
vRouter\](https://www.rackspace.com/knowledge\_center/article/configuring-a-policy-based-ipsec-site-to-site-vpn-on-a-vyatta-vrouter)
\[Configure a Site-to-site VPN using the Vyatta Network
Appliance\](https://www.rackspace.com/knowledge\_center/article/configure-a-site-to-site-vpn-using-the-vyatta-network-appliance)
\[Creating NAT rules for Vyatta
vRouter\](https://www.rackspace.com/knowledge\_center/article/creating-nat-rules-for-vyatta-vrouter)
\[Vyatta vRouter: Allow an IP address to access the vRouter via
SSH\](https://www.rackspace.com/knowledge\_center/article/vyatta-vrouter-allow-an-ip-address-to-access-the-vrouter-via-ssh)
\[Vyatta vRouter: Adding a local administrative
user\](https://www.rackspace.com/knowledge\_center/article/vyatta-vrouter-adding-a-local-administrative-user)
\[Vyatta vRouter: Configure an interface
firewall\](https://www.rackspace.com/knowledge\_center/article/vyatta-vrouter-configure-an-interface-firewall)
The following table shows the list of Rackspace supported features on
the Brocade Vyatta vRouter

Feature

Support Status on Vyatta vRouter

Routing

Static routing

**Supported**

Static routing with IP SLA tracking

Not supported

Dynamic routing protocols OSPF, EIGRP

Not supported

Dynamic routing protocols - all other

Not supported

IPv6

Static routing

Not supported

Static routing with IP SLA tracking

Not supported

Dynamic routing protocols

Not supported

NAT

Static (one-to-one)

**Supported**

PAT (NAT overloading)

**Supported**

Policy NAT/PAT

**Supported**

DNS Doctoring

N/A

Connection limits via static NAT

N/A

Packet filtering

Layer 3/4 filtering ingress/egress

**Supported**

FQDN based filtering

N/A

VPN

IPsec - IKEv2

Not supported

IPsec LAN-to-LAN Layer 3/4 filtering

Not supported

IPsec LAN-to-LAN Pre-shared keys authentication

**Supported**

IPsec LAN-to-LAN Hub and spoke configuration

**Supported**

IPsec LAN-to-LAN Cert-based authentication

Not supported

IPsec DMVPN

N/A

IPsec remote access with Cisco Client

N/A

IPsec remote access with Apple OS X native IPsec client

N/A

IPsec remote access with Shrew Soft client

N/A

IPsec remote access with group authentication

N/A

IPsec remote access with group and user authentication

N/A

IPsec remote access with two-factor authentication

N/A

IPsec remote access - Multiple VPN groups

N/A

IPsec remote access with layer 3/4 filtering

N/A

IPsec remote access - Split-tunneling

N/A

IPsec remote access - all traffic through VPN (tunnel all)

N/A

IPsec remote access - DNS server assignment

N/A

IPsec remote access - Client certificate-based authentication

N/A

IPsec remote access on Windows 8

N/A

SSL VPN - AnyConnect

**N/A (Supported via Open VPN SSL client)**

SSL VPN - Certificate authentication

Not supported

SSL VPN - Two-factor authentication

Not supported

SSL VPN - Clientless SSL VPN

Not supported

SSL VPN - Secure desktop

N/A

SSL VPN - Mobile client

N/A

Management

Buffered Logging

**Supported**

Log shipping to log correlation device within customer's account

**Supported**

Custom logging, logging lists

Not supported

Log retention by Rackspace

Not supported

Log analysis, outside of troubleshooting an issue

Not supported

Direct customer access if firewall is on TACACS

N/A

SNMP read-only for customer

**Supported**

High Availability (HA)

Active/Standby (stateful and non-stateful)

N/A

Active/Active (stateful and non-stateful)

N/A

Clustering of more than two units

N/A

Modes and modules

Mode - Multi-Context Routed

N/A

Mode - Routed

**Supported**

Mode - Transparent

N/A

Modules/Configs - Threat-detection

N/A

Modules/Configs - IPS Module

N/A

Modules/Configs - Cisco Unified Communications Proxy

N/A

RackConnect

RackConnect VLANs termination

N/A



