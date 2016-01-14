---
node_id: 3970
title: What is an SOA record?
type: frequently_asked_question
created_date: '2014-03-25 19:34:21'
created_by: nico4001
last_modified_date: '2014-03-31 14:5117'
last_modified_by: rose.contreras
product: Cloud Hosting
body_format: tinymce
---

A Start of Authority (SOA) resource record indicates which DNS name
server is the best source of information for the specified domain. Every
domain must have an SOA record.

When you add a domain to DNS, the email address that you indicate is
added to the SOA record for the domain. This publicly associates the
email with the domain.

![](http://5637f99e22e42b3a3b0a-e2386ae7b063b70b5535752a5fd32819.r21.cf5.rackcdn.com/NewDNSPopOver.png)

For example, the email address associated with the **rackspace.com**
domain is **hostmaster@rackspace.com**. You can see the SOA record for 
**rackspace.com** by running the following command:

    dig rackspace.com +nssearch

The following information is returned:

    SOA ns.rackspace.com. hostmaster.rackspace.com. 1392389079 300 300 1814400 300 from server 69.20.95.4 in 12 ms.

The SOA record includes the following details:

-   The primary name server for the domain, ns.rackspace.com
-   The e-mail for the domain, hostmaster@rackspace.com.
-   Revision number that changes whenever you update your domain.
-   Refresh time, the number of seconds before the zone should be
    refreshed.
-   Retry time, the number of seconds before a failed refresh should be
    retried.
-   Expiration time, the time, in seconds, before the data is considered
    unreliable.
-   Minimum TTL, this default applies to all resource records in the
    zone

 

