---
node_id: 3671
title: Setting Up Vyatta VPN with Policy NAT
type: article
created_date: '2013-09-03 17:12:36'
created_by: sameer.satyam
last_modified_date: '2013-09-17 17:3226'
last_modified_by: jered.heeschen
product: Cloud Servers
body_format: tinymce
---

undefined&rsquo; public interface for Internet access and the cloud networks
interface for VPN only traffic, your server admin will need to create a
static route on the cloud server for the remote VPN encryption domain
that points at the Vyatta's cloud network IP address.

Vyatta calls their static NAT a "bi-directional NAT". So when searching
Vyatta's documentation, please keep this in mind.

#### Topology

##### Local Vyatta Firewall

+--------------------------+--------------------------+--------------------------+
| **Interface**            | **IP Address**           | **Description**          |
+--------------------------+--------------------------+--------------------------+
| eth0                     | 166.78.184.111/24        | public                   |
+--------------------------+--------------------------+--------------------------+
| eth1                     | 172.26.26.1/24           | INSIDE-172.26.26.0/24    |
+--------------------------+--------------------------+--------------------------+

##### Remote Cisco ASA Firewall

+--------------------------+--------------------------+--------------------------+
| **Interface**            | **IP Address**           | **Description**          |
+--------------------------+--------------------------+--------------------------+
| eth 0/0                  | 192.0.2.10/28            | outside                  |
+--------------------------+--------------------------+--------------------------+
| eth 0/1                  | 192.168.10.1/24          | INSIDE-192.168.10.0/24   |
+--------------------------+--------------------------+--------------------------+
| eth 0/2                  | 192.168.19.1/24          | DMZ-192.168.19.0/24      |
+--------------------------+--------------------------+--------------------------+

#### VPN Details

##### Encryption Domains

+--------------------------------------+--------------------------------------+
| **Local VPN Encryption Domains**     | **Remote VPN Encryption Domains**    |
+--------------------------------------+--------------------------------------+
| INSIDE-172.26.26.0/24                | DMZ-192.168.19.0/24                  |
+--------------------------------------+--------------------------------------+

##### ISAKMP and IPSEC Settings

+--------------------------------------+--------------------------------------+
| **Phase 1 Settings**                 | **Phase 2 Settings**                 |
+--------------------------------------+--------------------------------------+
| AES-256                              | AES-256                              |
+--------------------------------------+--------------------------------------+
| SHA1                                 | SHA1                                 |
+--------------------------------------+--------------------------------------+
| Group 5                              | PFS Group 5                          |
+--------------------------------------+--------------------------------------+
| 86400 Seconds                        | 3600 Seconds                         |
+--------------------------------------+--------------------------------------+

#### VPN Configuration

##### Enable the VPN daemon on the outside interface

+--------------------------------------------------------------------------+
| \# Enable the VPN daemon on the eth0 Interface \                         |
|  set vpn ipsec ipsec-interfaces interface eth0                           |
+--------------------------------------------------------------------------+

##### Phase 1 Define the Policies

+--------------------------------------------------------------------------+
| \# Phase 1 Settings: AES-256, SHA1, Group 5, Lifetime 86400 \            |
|  set vpn ipsec ike-group **IKE-POLICY-10** lifetime 86400 \              |
|  set vpn ipsec ike-group **IKE-POLICY-10** proposal 1 dh-group 5 \       |
|  set vpn ipsec ike-group **IKE-POLICY-10** proposal 1 encryption aes256  |
| \                                                                        |
|  set vpn ipsec ike-group **IKE-POLICY-10** proposal 1 hash sha1          |
+--------------------------------------------------------------------------+

##### Phase 2 Define the ESP-GROUP (Like an ASA Transform Set)

+--------------------------------------------------------------------------+
| \# Phase 2 Settings: AES-256, SHA1, PFS Group 5, Lifetime 3600 \         |
|  set vpn ipsec esp-group **AES-256-SHA-PFS-GROUP-5-3600** lifetime 3600  |
| \                                                                        |
|  set vpn ipsec esp-group **AES-256-SHA-PFS-GROUP-5-3600** mode tunnel \  |
|  set vpn ipsec esp-group **AES-256-SHA-PFS-GROUP-5-3600** pfs enable \   |
|  set vpn ipsec esp-group **AES-256-SHA-PFS-GROUP-5-3600** proposal 1     |
| encryption aes256 \                                                      |
|  set vpn ipsec esp-group **AES-256-SHA-PFS-GROUP-5-3600** proposal 1     |
| hash sha1                                                                |
+--------------------------------------------------------------------------+

##### Phase 2 Define the Individual Peer Attributes

+--------------------------------------------------------------------------+
| set vpn ipsec site-to-site peer 192.0.2.10 description "VPN TO TANGO LAB |
| ASA-5510" \                                                              |
|  set vpn ipsec site-to-site peer 192.0.2.10 authentication mode          |
| pre-shared-secret \                                                      |
|  set vpn ipsec site-to-site peer 192.0.2.10 authentication               |
| pre-shared-secret netsecR@wks \                                          |
|  set vpn ipsec site-to-site peer 192.0.2.10 default-esp-group            |
| **AES-256-SHA-PFS-GROUP-5-3600** \                                       |
|  set vpn ipsec site-to-site peer 192.0.2.10 ike-group **IKE-POLICY-10**  |
| \                                                                        |
|  set vpn ipsec site-to-site peer 192.0.2.10 local-address 166.78.184.111 |
+--------------------------------------------------------------------------+

##### Phase 2 Define the Tunnel Attributes (Encryption Domains)

+--------------------------------------------------------------------------+
| \# Tunnel 1 Local Cloud Networks (Inside) to remote DMZ \                |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 1 allow-nat-networks  |
| disable \                                                                |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 1                     |
| allow-public-networks disable \                                          |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 1 esp-group           |
| AES-256-SHA-PFS-GROUP-5-3600 \                                           |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 1 local prefix        |
| 10.255.255.0/24 \                                                        |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 1 remote prefix       |
| 192.168.19.0/24                                                          |
|                                                                          |
| \# Tunnel 2 Local Cloud Networks (Inside) to remote INSIDE \             |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 2 allow-nat-networks  |
| disable \                                                                |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 2                     |
| allow-public-networks disable \                                          |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 2 esp-group           |
| AES-256-SHA-PFS-GROUP-5-3600 \                                           |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 2 local prefix        |
| 10.255.255.0/24 \                                                        |
|  set vpn ipsec site-to-site peer 192.0.2.10 tunnel 2 remote prefix       |
| 192.168.10.0/24                                                          |
+--------------------------------------------------------------------------+

#### Solution 1: Policy NAT Configuration With Individual Addresses

##### VPN NAT

+--------------------------------------------------------------------------+
| **NAT traffic bidirectionally mapping 172.26.26.2 \<--\> 10.255.255.202  |
| and 172.26.26.3 \<--\> 10.255.255.203**                                  |
+--------------------------------------------------------------------------+
| \# Rule 10 - **NAT 172.26.26.2 \<--\> 10.255.255.2 when traffic is       |
| destined for the remote VPN encryption domain** \                        |
|  set nat **destination** rule 10 description "172.26.26.2 -              |
| 10.255.255.202 Policy Nat" \                                             |
|  set nat **destination** rule 10 source address 192.168.19.0/24 \        |
|  set nat **destination** rule 10 destination address 10.255.255.202 \    |
|  set nat **destination** rule 10 inbound-interface eth0 \                |
|  set nat **destination** rule 10 translation address 172.26.26.2 \       |
|  set nat **source** rule 10 description "172.26.26.2 - 10.255.255.202    |
| Policy Nat" \                                                            |
|  set nat **source** rule 10 outbound-interface eth0 \                    |
|  set nat **source** rule 10 source address 172.26.26.2 \                 |
|  set nat **source** rule 10 destination address 192.168.19.0/24 \        |
|  set nat **source** rule 10 translation address 10.255.255.202           |
|                                                                          |
| \# Rule 20 - **NAT 172.26.26.3 \<--\> 10.255.255.3 when traffic is       |
| destined for the remote VPN encryption domain** \                        |
|  set nat **destination** rule 20 description "172.26.26.3 -              |
| 10.255.255.203 Policy Nat" \                                             |
|  set nat **destination** rule 20 source address 192.168.19.0/24 \        |
|  set nat **destination** rule 20 destination address 10.255.255.203 \    |
|  set nat **destination** rule 20 inbound-interface eth0 \                |
|  set nat **destination** rule 20 translation address 172.26.26.3 \       |
|  set nat **source** rule 20 description "172.26.26.3 - 10.255.255.203    |
| Policy Nat" \                                                            |
|  set nat **source** rule 20 outbound-interface eth0 \                    |
|  set nat **source** rule 20 source address 172.26.26.3 \                 |
|  set nat **source** rule 20 destination address 192.168.19.0/24 \        |
|  set nat **source** rule 20 translation address 10.255.255.203           |
|                                                                          |
| \# Rule 50 - **PAT all other traffic from 172.26.26.0/24 as the outside  |
| interface's IP Address** (Outside PAT Overload) \                        |
|  \# Note that this traffic would not be destined for the VPN but for     |
| unencrypted Internet traffic \                                           |
|  set nat source rule 50 description "POLICY PAT INSIDE TO Internet" \    |
|  set nat source rule 50 outbound-interface eth0 \                        |
|  set nat source rule 50 source address 172.26.26.0/24 \                  |
|  set nat source rule 50 translation address masquerade                   |
+--------------------------------------------------------------------------+

#### Solution 2: Policy NAT Subnet to Subnet

##### VPN NAT

+--------------------------------------------------------------------------+
| **NAT traffic bidirectionally mapping the entire subnets 172.26.26.0/24  |
| \<--\> 10.255.255.0/24 \                                                 |
|  eg: 172.26.26.2 \<--\> 10.255.255.2 and 172.26.26.3 \<--\>              |
| 10.255.255.3**                                                           |
+--------------------------------------------------------------------------+
| \# Rule 10 - **NAT 172.26.26.0/24 \<--\> 10.255.255./24 when traffic is  |
| destined for the remote VPN encryption domain** \                        |
|  set nat **destination** rule 10 description "172.26.26.0/24 -           |
| 10.255.255.0/24 Policy Nat" \                                            |
|  set nat **destination** rule 10 source address 192.168.19.0/24 \        |
|  set nat **destination** rule 10 destination address 10.255.255.0/24 \   |
|  set nat **destination** rule 10 inbound-interface eth0 \                |
|  set nat **destination** rule 10 translation address 172.26.26.0/24 \    |
|  set nat **source** rule 10 description "172.26.26.0/24 -                |
| 10.255.255.0/24 Policy Nat" \                                            |
|  set nat **source** rule 10 outbound-interface eth0 \                    |
|  set nat **source** rule 10 source address 172.26.26.0/24 \              |
|  set nat **source** rule 10 destination address 192.168.19.0/24 \        |
|  set nat **source** rule 10 translation address 10.255.255.0/24          |
|                                                                          |
| \# Rule 50 - **PAT all other traffic from 172.26.26.0/24 as the outside  |
| interface's IP Address** (Outside PAT Overload) \                        |
|  \# Note that this traffic would not be destined for the VPN but for     |
| unencrypted Internet traffic \                                           |
|  set nat source rule 50 description "POLICY PAT INSIDE TO Internet" \    |
|  set nat source rule 50 outbound-interface eth0 \                        |
|  set nat source rule 50 source address 172.26.26.0/24 \                  |
|  set nat source rule 50 translation address masquerade                   |
+--------------------------------------------------------------------------+



