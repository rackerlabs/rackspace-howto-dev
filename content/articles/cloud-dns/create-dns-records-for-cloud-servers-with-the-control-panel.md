---
node_id: 1456
title: Create DNS Records for cloud servers with the Control Panel
type: article
created_date: '2012-07-13'
created_by: Rackspace Support
last_modified_date: '2016-01-20'
last_modified_by: Kyle Laffoon
product: Cloud DNS
body_format: full_html
---

**Previous section:** [Getting Started with Cloud
Servers](/how-to/cloud-servers)

This article provides instructions for creating a DNS zone for your
domain and adding basic A, MX, and CNAME records by using the Cloud
Control Panel.

To learn more about A, MX, and CNAME records for Cloud Sites, see
[Getting started with Cloud Sites &ndash; Managing DNS
records](/how-to/getting-started-with-cloud-sites-managing-dns-records).

-   [DNS servers for cloud servers](#H)
-   [Create a DNS zone for your domain](#A)
-   [Add a domain](#B)
-   [Add an A record](#C)
-   [Add a CNAME record](#D)
-   [Add an MX record](#E)
-   [Delete a record](#F)
-   [Delete a domain](#G)



DNS servers for cloud servers
-----------------------------

Following are the DNS servers for your cloud servers:

-   dns1.stabletransit.com
-   dns2.stabletransit.com



Create a DNS zone for your domain
---------------------------------

1.  Log in to the [Cloud Control Panel](https://mycloud.rackspace.com).
2.  Select **Networking &gt; Cloud DNS**.

    <img src="/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-16%20at%201.12.55%20PM.png" width="470" height="174" />

3.  Continue with the following procedures to create the records for
    your domain's DNS zone.



### Add a domain

1.  Click **Create Domain**.
2.  In the popup dialog box, enter the following information:
    -   Name of your domain.
    -   Email address publicly associated as the admin and contact for
        the domain.
    -   Time to live (TTL) for the domain.

3.  Click **Create Domain**.



### Add an A record

An A record is an IPv4 address record that you use to point your domain
to an IP address. It is also known as an A name.

1.  On the Cloud DNS page, click the gear icon next to your domain and
    select **Add DNS Record**.
2.  In the popup dialog box, select **A/AAAA Record** for the
    record type.
3.  Enter the following information:
    -   The hostname for your domain (optional).
    -   Target (IP address of the server).
    -   Time to live (TTL). The TTL refers to the time it will take for
        your computer to refresh DNS information. It is referred to in
        seconds of time.

4.  Click **Add Record**.



### Add a CNAME record

A CNAME record, also known as a canonical name record, is a record type
in the DNS that you use to indicate that your domain name is an alias
for your domain's canonical name. Subdomains and IP addresses for your
domain are defined by the canonical domain.

Use the Common Name (CNAME) record to point to another record.

1.  Click the action gear next to your domain and click **Add DNS
    Record**.
2.  Select **CNAME Record** for the record type.
3.  Enter the following information:
    -   The hostname for your domain (optional).
    -   Target (for your domain)
    -   Time to live (TTL). The TTL refers to the time it will take for
        your computer to refresh DNS information. It is referred to in
        seconds of time.

4.  Click **Add Record**



### Add an MX record

Use the Mail Exchange (MX) is a DNS record that points to the server
that handles your domain-related email delivery. You create an MX record
for your domain that allows you to set up an email address. For example,
you can create an MX record to create the email address
**user@yourdomain.com**. You can send email without setting up the MX
record for your domain name, but you cannot receive emails without it.

1.  On the Cloud DNS page, click the gear icon next to your domain and
    select **Add DNS Record**.
2.  In the popup dialog box, select **MX Record** for the record type.
3.  Enter the following information:
    -   The hostname for your domain (optional).
    -   Domain of the mail server.
    -   Priority. The MX record priority is a setting you will use when
        your domain name uses more than one mail server. The priority
        that you set for your MX record affects the load sharing and the
        order in which multiple mail servers are used, and also allows
        the use of primary and backup mail servers.
    -   Time to live (TTL). TTL refers to the time it will take for your
        computer to refresh DNS information. It is referred to in
        seconds of time.

4.  Click **Add Record**.



### Delete a record from your domain

1.  On the Cloud DNS page, click the name of the domain.
2.  On the domain page, scroll down to the **Records** section, and
    choose one of the following methods to delete a record:
    -   Select the check box next to the record that you want to delete,
        click **Actions**, and select **Delete records**. You can use
        this method to delete multiple records at once.

        <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-16%20at%205.29.36%20PM.png" width="207" height="141" />

    -   Click the gear icon next to the record and select **Delete
        Record**.

        <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-16%20at%203.27.52%20PM_0.png" width="217" height="213" />



### Delete a domain

Use one of the following methods to delete a domain on the Cloud DNS
page.

-   Click the gear icon next to the domain, and select **Delete
    Domain**.

    <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-16%20at%205.13.13%20PM.png" width="208" height="133" />

-   Select the check box next to the domain and click **Delete** at the
    top of the domain list.

    <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-16%20at%205.12.52%20PM.png" width="189" height="95" />


