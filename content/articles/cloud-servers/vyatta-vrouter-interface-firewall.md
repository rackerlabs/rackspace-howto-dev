---
node_id: 4234
title: 'Vyatta vRouter: Configure an interface firewall'
type: article
created_date: '2014-09-11 16:20:49'
created_by: sameer.satyam
last_modified_date: '2015-02-18 20:5323'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

undefined&rdquo; policy, which means that you
must add the most specific rules at the top of the list. The number of
the rule dictates its position in the rule base.

By default, apply your rules inbound, into the interface. There is a
limit of 10k lines per firewall rule base. Rules cannot be reordered, so
allow space between added rules; space new rules by 10. Lastly, firewall
rules are processed POST-DNAT. See the NAT page for more information.

To configure the interface firewall rule base
---------------------------------------------

The following are configuration examples to guide in configuring the
interface firewall rule base.

    set firewall name PUBLIC-IN rule 1000 description "Allow 7's to DMZ, 80/443"
    set firewall name PUBLIC-IN rule 1000 source address 7.7.7.0/24
    set firewall name PUBLIC-IN rule 1000 destination address 192.168.100.0/24
    set firewall name PUBLIC-IN rule 1000 destination port http, https
    set firewall name PUBLIC-IN rule 1000 protocol tcp
    set firewall name PUBLIC-IN rule 1000 action accept

    set firewall name DMZ-IN rule 1000 description "Allow mail to APP segment"
    set firewall name DMZ-IN rule 1000 destination port smtp
    set firewall name DMZ-IN rule 1000 protocol tcp
    set firewall name DMZ-IN rule 1000 action accept`
    set firewall name DMZ-IN rule 1000 description "BLOCK to INSIDE"
    set firewall name DMZ-IN rule 1000 destination address 10.0.0.0/24
    set firewall name DMZ-IN rule 1000 action drop
    set firewall name DMZ-IN rule 1000 description "BLOCK to APP"
    set firewall name DMZ-IN rule 1000 destination address 172.16.10.0/24
    set firewall name DMZ-IN rule 1000 action drop
    set firewall name DMZ-IN rule 9999 description "ALLOW OUT"
    set firewall name DMZ-IN rule 9999 action accept
    . . .

**NOTE:** If a field in the rule base is left empty, vRouter interprets
that field as nonspecific and allows all possible matches. In the case
of source and destination addresses, the vRouter assumes 0.0.0.0/0. In
the case of source and destination ports, vRouter assumes all ports. If
a port is specified, a protocol must also be specified. If no port is
specified, and the protocol field is left empty, vRouter assumes all
protocols.

Specify the actions.

### To apply the rule base to the interfaces

The following configuration examples will help you apply the rule base
to the interfaces.

    set interfaces ethernet eth0 firewall in name PUBLIC-IN
    set interfaces ethernet eth1 firewall in name INSIDE-IN
    set interfaces ethernet eth2 firewall in name APP-IN
    set interfaces ethernet eth3 firewall in name DMZ-IN

Configure the local firewall
----------------------------

vRouter has a specific firewall that you can configure to handle traffic
destined for vRouter itself. Each interface can share a single local
firewall rule base, or each interface can have a specific rule base
configured. As with traditional interface firewall rule bases, create
your specific rules first. The naming convention is also similar,
-LOCAL. You can then apply that rule base to the interface, as a local
firewall.

### To apply the local firewall to the interface

The following configuration examples will guide you in configuring the
local firewall to the interface.

    set interfaces ethernet eth0 firewall local name PUBLIC-LOCAL
    set interfaces ethernet eth1 firewall local name INTERNAL-LOCAL
    set interfaces ethernet eth2 firewall local name INTERNAL-LOCAL
    set interfaces ethernet eth3 firewall local name INTERNAL-LOCAL

### Verify the firewall configuration

The following configuration examples will guide you in verifying the
firewall configuration.

    show firewall name 
    show firewall name  statistics
    show firewall name  counters

Log firewall rules
------------------

You can enable logging for specific firewall rules within the command
hierarchy. Enable logging only when needed and disable it after you are
done so that vRouter is not flooded with unneeded log messages.

### To enable logging on a specific rule (configuration mode)

    set firewall name <'rulebase_name'> rule 10 log enable commit

### To view (operational mode) active log messages

    monitor firewall

### To disable logging on a specific rule (configuration mode)

    delete firewall name <*rulebase_name'> rule 10 log commit

