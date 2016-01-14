---
node_id: 1268
title: Split Domain Routing
type: article
created_date: '2011-12-30 21:02:52'
created_by: RackKCAdmin
last_modified_date: '2016-01-12 16:1118'
last_modified_by: stephanie.fillmon
product: Cloud Office
body_format: tinymce
---

### **What is Split Domain Routing?**

Split Domain Routing (SDR) allows you to have a single domain's
mailboxes distributed between our system and an external system, working
together as if they were in one environment. This is primarily used when
migrating a large number of mailboxes over to our system from another
server over an extended period of time.

Mailboxes can be moved in batches to make the move more manageable for
administrators and to make the transition almost seamless for the users.
Though it is not common, SDR can also be used when you need to maintain
some mailboxes on an existing system for an extended period of time or
permanently.  

If SDR will be a permanent feature of your set up they can point to
either your external mail server or us. You may want to point your MX
records to Rackspace because then all your messages get the benefit of
our spam/anti-virus filtering instead of just the Rackspace-hosted
mailboxes.

### **Setting up Split Domain Routing:**

There are two parts to setting up SDR and they relate to enabling our
system and the external system to have two-way communication. If you are
using SDR as part of a migration, you will want to keep your MX records
for the domain pointing to your existing server (described as your
external mail server in this documentation). Once the migration is
complete you can switch them to the Rackspace MX records listed here:
[Set up DNS records for Cloud Office email and Skype for
Business](http://www.rackspace.com/knowledge_center/article/set-up-dns-records-for-cloud-office-email-and-skype-for-business)

![](http://c973967.r67.cf2.rackcdn.com/(E%26A)SplitDomainRouting.png)  

### **Enabling Split Domain Routing through the Cloud Office control panel:** 

When SDR is enabled, our environment will forward to your external
server any messages addressed to recipients on your domain that do not
exist in our system. To enable it requires the hostname of your external
mail server (usually one of the MX Records that point to your external
system) and a valid email address within the designated domain hosted on
that external mail server. We will use this address only to validate the
server. You must also open port 25 on the external mail server so that
our system can connect to it. 

![](http://c973967.r67.cf2.rackcdn.com/(E%26A)SplitDomainRouting2.png)  

###  

### **To enable Split Domain Routing perform the following steps:** 

1. First log in to the control panel
([cp.rackspace.com](http://cp.rackspace.com)) & mouse over the **Go To
Section** drop-down menu and select **Domains**.

![](/knowledge_center/sites/default/files/field/image/a.png)

2. In the **Tools** section, select the **Split Domain** link & select
the domain you want to set up Split Domain Routing for.

![](/knowledge_center/sites/default/files/field/image/b.png)

3. Check the **Enable Split Domain Routing** box & in the **External
Mail Server** box, enter the name of your external mail server. In
the **Verification Address box**, enter in a valid email address that is
hosted on your external mail server and then select the **Save** button.

### ![](/knowledge_center/sites/default/files/field/image/c.png)

 

### **Configuring Split Domain Routing from your own external server to Rackspace: **

This type of functionality is known by several names including
non-authoritative mail delivery or message routing for a shared address
space. The idea is to set up the external server so that if it is not
able to deliver a message locally, the server forwards to another system
(Rackspace). Different mail systems will have their own procedures for
configuring this. 

The following Microsoft articles show how to accomplish this: 

**Exchange Server 2007**:  [http://bit.ly/rE6YBR](http://bit.ly/rE6YBR)

**Exchange Server 2010**:  [http://bit.ly/CQy7](http://bit.ly/CQy7) 

###  

### **Sub-Domain Message Routing: **

This is a suggested way to route messages from your external server back
to Rackspace.  Sub-domain routing uses contacts (or forwards) set up on
your external system to route the messages to a sub-domain e-mail
address.  This same sub-domain should be added as a domain alias on our
system in order for this to work.

The following should be in place:

-   a sub-domain created with your DNS host pointing to Rackspace MX
    records, e.g. rackspace.example.com with its own set of MX records
    pointing to **mx1.emailsrvr.com**

-   contacts (aliases) must be created on the external system for each
    mailbox hosted by Rackspace - the contact must forward the
    yourdomain.com address to the rackspace.example.com address.  For
    example, user@example.com (on your external server) will have a
    forward set to user@rackspace.example.com.  Your server will see the
    @rackspace.example.com address and query DNS - which will then
    resolve back to **mx1.emailsrvr.com** and deliver to the user in
    Rackspace's environment.

-   Please ensure you have requested your rackspace.example.com
    subdomain as a **domain alias**. In order to do this, please contact
    Support (chat, phone call, or open a ticket).

![](http://c973967.r67.cf2.rackcdn.com/(E%26A)SplitDomainRouting6.png)

If Rackspace is your DNS host, enter this sub-domain name in the Mail
Records (MX) section of the DNS Settings page in the Control Panel. To
learn more, please see the help topic, [Manage DNS
Records](http://www.rackspace.com/knowledge_center/article/managing-cloud-sites-email-dns-records).

*Note:* *For a migration, when changing the MX Records, ensure that you
are changing them for the new sub-domain, e.g. rackspace.example.com,
and not the primary domain. After all mailboxes are on our system, you
will change the MX Records for the primary domain.* 

