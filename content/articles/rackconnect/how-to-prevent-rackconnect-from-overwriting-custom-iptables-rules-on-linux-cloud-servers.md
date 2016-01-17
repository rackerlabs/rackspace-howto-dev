---
node_id: 3283
title: How to Prevent RackConnect from Overwriting Custom Iptables Rules on Linux Cloud Servers
type: article
created_date: '2013-01-26'
created_by: Russell Lambert
last_modified_date: '2014-11-11'
last_modified_by: Jered Heeschen
product: RackConnect
body_format: tinymce
---

By default, RackConnect Automation takes complete control of the
iptables software firewall on your Linux Cloud Servers, using it to
enforce your configured Network Policies for those network connections
that do not traverse your hardware firewall device.  For most users this
is exactly the functionality that they need.

For a few advanced users, however, the way that RackConnect Automation
replaces all existing iptables rules can be frustrating.  They have
specific needs that require the ability to create and maintain their own
custom iptables rules in addition to those used to enforce their Network
Policies.

This article describes a method by which an advanced user may modify the
default behavior of RackConnect Automation's software firewall
management on Linux Cloud Servers in order to allow them to create their
own iptables rules.

Who is the target audience for this article?
--------------------------------------------

This article is aimed at advanced Linux users who are familiar with the
iptables software firewall and who have a need to create custom iptables
rules to perform tasks that are beyond the scope of [Network
Policies](/howto/managing-rackconnect-v20-network-policies).

If you are unfamiliar with iptables syntax or how to write custom
iptables rules in Linux, or if you do not have a pressing need to create
and maintain your own iptables rules, it is highly recommended that you
do not modify the default behavior of RackConnect Automation.
[RackConnect Network
Policies](/howto/managing-rackconnect-v20-network-policies)
provide a friendlier and more scalable solution for software firewall
management than writing your own custom iptables rules on each
individual Cloud Server.

OK, I'm an advanced user and I have a need for custom rules.  What do I need to do?
-----------------------------------------------------------------------------------

Each time RackConnect Automation updates the iptables rules on a server
it checks for the existence of a file called
/etc/rackconnect-allow-custom-iptables.  If this file exists it uses a
slightly different method to update the iptables rules on the server -
instead of completely replacing the iptables filter rules, it rebuilds
only the RackConnect-created rules while preserving all other iptables
rules.  Because it merges RackConnect rules with custom rules, this new
method is often referred to as the "merge method" (as opposed to the
traditional "clobber method").  To tell RackConnect Automation to use
the "merge method" on a particular server, simply do the following:

1.  Create an empty file in /etc/
    named "rackconnect-allow-custom-iptables".

        touch /etc/rackconnect-allow-custom-iptables

2.  Force a software firewall update by creating a Network Policy in the
    MyRackspace Portal that affects the servers on which you created the
    /etc/rackconnect-allow-custom-iptables file.  The easiest way to do
    this is to create a temporary Dedicated to Cloud Server policy for a
    bogus IP to all Cloud Servers.  Once the policy has been pushed to
    all cloud servers (the indicator to the left of the policy changes
    from yellow to green) you should delete it (it is unlikely that
    someone with IP 1.1.1.1 will try to access your server, but better
    safe than sorry).

    ![Add Network Policy Screenshot; Name TempPolicy, Access Scenario
    Dedicated to Cloud Server, Source 1.1.1.1, Destination All,
    Destination Protocol
    All](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/framed-netpolicy_0.jpg){width="506"
    height="509"}



    ![Network Policy Indicator Screenshot; Yellow, still
    syncing](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/framed-netpolicy-syncing_0.jpg){width="749"
    height="63"}



    ![Network Policy Indicator Screenshot; Green, sync
    complete](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/framed-netpolicy-synced_0.jpg){width="750"
    height="58"}



    ![Network Policy Delete Screenshot; Check TempPolicy, Click Delete
    Policy](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/framed-netpolicy-delete_0.jpg){width="749"
    height="238"}




3.  You can verify that RackConnect Automation is using the "merge
    method" by looking at the last iptables rule in the
    RS-RackConnect-INBOUND chain on the server.  If it is a "RETURN"
    rule, the "merge method" is now being used for software firewall
    updates on this server.

        # iptables -vnL RS-RackConnect-INBOUND
        Chain RS-RackConnect-INBOUND (2 references)
         pkts bytes target     prot opt in     out     source               destination
          ###  #### ACCEPT     all  --  *      *       0.0.0.0/0            0.0.0.0/0            state RELATED,ESTABLISHED /* RackConnectChain-INBOUND-RE */
          ###  #### ACCEPT     all  --  lo     *       0.0.0.0/0            0.0.0.0/0            /* Local-Loopback */
          ...
          ###  #### ACCEPT     icmp --  *      *       0.0.0.0/0            0.0.0.0/0            /* RCAutoMP-NP_34908 */
          ###  #### RETURN     all  --  *      *       0.0.0.0/0            0.0.0.0/0

That's it?  Create one file and everything magically works?  What's the catch?
------------------------------------------------------------------------------

For the most part, yes; touching the file and forcing automation to
update iptables is all that is required.  There are a few important
things to note, however:

1.  #### **RackConnect rules always run before custom rules**

    All RackConnect-related ACCEPT/DENY rules are kept in filter chains
    named "RS-RackConnect-&lt;something&gt;" (such as
    RS-RackConnect-INBOUND).  The first rule of a primary iptables
    filter chain (such as INPUT) will always be an unconditional jump to
    the relevant RS-RackConnect-\* chain.  **This jump rule needs to
    remain the first rule in the basic chains, otherwise your custom
    rules may prevent RackConnect Automation from being able to log in
    to your server.**

    If you try to add iptables rules above this jump rule, RackConnect
    Automation will automatically move it back to the top of the list
    the next time Network Policies affecting that server are updated.
    Because the "merge method" adds an unconditional RETURN statement to
    the end of each of the RS-RackConnect-\* chains, iptables will
    automatically continue processing rules underneath the jump rule if
    none of the rules in the RS-RackConnect-\* chain match.

2.  #### **No changes may be made to the RS-RackConnect-\* chains except through Network Policies**

    All of the RS-RackConnect-\* chains are rebuilt whenever Network
    Policies affecting a server are updated.  As a result, any manual
    changes to a RS-RackConnect chain will be overwritten on
    next update.

3.  #### **RackConnect Automation saves iptables rules so they are restored on reboot**

    Every time RackConnect Automation runs it saves the current rules to
    the default system location for the Linux distribution running on
    that server, ensuring that they will be restored on reboot.
    Normally, this is desired behavior - after all, you don't want your
    server to be unprotected if it reboots.  Occasionally, advanced
    users will exploit the fact that iptables rules are held in memory
    until manually committed to disk in order to experiment with new
    rules, knowing that they can simply restart the iptables "service"
    to restore the old ruleset.  If you are one of these users be aware
    that updates to your Network Policies (by yourself or by another
    user in your organization with access to your account in the
    MyRackspace Portal) may cause RackConnect Automation to save the
    running ruleset to disk in the background while you
    are experimenting.

4.  #### **RS-RackConnect-\* rules are only updated when Network Policies change**

    If you use the *iptables-save* command to back up your iptables
    rules, take note of when your backup files are created.  By default,
    the *iptables-save* utility saves all chains in all tables.  If you
    restore from such a backup using *iptables-restore* you may be
    restoring an older version of the RS-RackConnect-\* chains than you
    should currently have.  If you have any doubt or suspicion that
    RackConnect Automation may have updated the iptables rules for a
    server since the backup you're restoring was taken, restore the
    backup and then use the "create a temporary Network Policy" method
    listed earlier in this article to force RackConnect Automation to
    update the RS-RackConnect-\* chains to the latest version.

Troubleshooting
---------------

-   **I created /etc/rackconnect-allow-custom-iptables, but it doesn't
    appear that my rules are being processed!**

    There are two possible causes:

    1.  *RackConnect Automation has not updated iptables on the server
        since /etc/rackconnect-allow-custom-iptables was created*

        RackConnect Automation only creates a RETURN rule at the end of
        the RS-RackConnect-\* chains when operating in "merge mode".  If
        you have created the /etc/rackconnect-allow-custom-iptables file
        but RackConnect Automation has not yet updated iptables on your
        server, there will not be a RETURN rule and iptables will stop
        processing rules as soon as it reaches the end of the relevant
        RS-RackConnect-\* chain.  You can remedy the situation by
        forcing a software firewall refresh using the "create a
        temporary Network Policy" method detailed in setup Step 2
        above.  As long as /etc/rackconnect-allow-custom-iptables
        exists, RackConnect Automation will not remove the custom rules
        you have created - it will simply add the RETURN rule necessary
        for iptables to process them.

    2.  *A RackConnect rule is already handling the packet*

        Iptables rules are handled on a "first match" basis.  If a rule
        in the relevant RS-RackConnect-\* chain matches a packet,
        iptables will do as that rule says (ACCEPT or DROP it) and will
        stop processing further rules.  If the matching
        RS-RackConnect-\* rule is insufficient for your needs you may
        need to adjust your Network Policies to remove the matching rule
        in order to allow iptables to continue down the rule list to
        your custom rule.

<!-- -->

-   **Who can I contact if I have any questions?**

    Should you have any questions about RackConnect, Managed Cloud
    Service Level, or this change, please don't hesitate to [contact
    your Rackspace Support team](http://www.rackspace.com/support/).



