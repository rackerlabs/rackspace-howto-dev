---
node_id: 1239
title: Rackspace Cloud DNS - FAQ
type: article
created_date: '2011-10-25 16:30:48'
created_by: RackKCAdmin
last_modified_date: '2016-01-11 22:1210'
last_modified_by: rose.contreras
product: Cloud Servers
body_format: tinymce
---

### Prior section

[**Rackspace Cloud DNS - Additional
Resources**](https://admin.rackspace.com/knowledge_center/cloud_dns_additional_resources)

#### **Table of Contents**

#### General

[What is a domain name system (DNS)?](#whatisdns)\
 [What types of customers/accounts have access to Cloud
DNS?](#whattypesofaccounts)\
 [Where can I find the Cloud DNS API documentation?](#wherecanifindapi)

####  

#### Billing and Usage

[How much does this service cost?](#howmuch)

####  

#### Existing Product Compatibility

[Can this service be used for Dedicated
Servers?](#canbeusedfordedicated)\
 [Does Cloud DNS work with Cloud Sites?](#doesthisworkforcloudsites)\
 [How does this work for Hybrid customers?](#howdoesthisworkforhybrid)

####  

#### Accessing Cloud DNS

[When authenticating, do I use the same API user & key that I use when
connect to other Cloud APIs?](#howdoiauthenticate)\
 [What account number do I use to access the
service?](#whataccountnumber)\
 [What is the difference between US and UK Cloud
DNS?](#whatisthedifference)

####  

#### Features and Functionality

[What DNS management operations does the Cloud DNS API
support?](#whatdnsmanagement)\
 [What record types does Cloud DNS support?](#whatrecordtypes)\
 [Can I import and export domains?](#caniimportandexport)\
 [What are the Rackspace DNS servers?](#dnsservers)\
 [What type of DNS network does Rackspace use?](#whattypeofdnsnetwork)\
 [What are the limitations of the search
functionality?](#whatarethelimitations)\
 [Do my TTL settings expire?](#domyttlsettingsexpire)

####  

#### Performance

[What are the default TTL&rsquo;s for domains and
records?](#whataredefaultttl)\
 [How long does it take for DNS changes to be propagated
globally?](#howlongpropagate)\
 [Are there API rate limits?](#arethereapiratelimits)

####  

#### Support

[How many Cloud DNS domains and records can I
have?](#howcaniraiseapilimit)\
 [How can I create a Cloud DNS ticket?](#howcanicreateticket)

 

#### What is a domain name system (DNS)?

The Domain Name System (DNS) is a system by which internet domain
name-to-address and address-to-name resolutions are determined. All
domains and their components, such as mail servers, utilize DNS to
resolve to the appropriate locations. For example, DNS is used to turn
'www.rackspace.com' into the computer addressable IP address
'207.97.209.147'.

DNS servers are usually set up in a master-slave relationship such that
failure of the master invokes the slave. DNS servers may also be
clustered or replicated such that changes made to one DNS server are
automatically propagated to other active servers.

#### What types of customers/accounts can access Cloud DNS?

Anyone who has a Rackspace Cloud account can access the Cloud DNS
service.  Existing Cloud customers will have access to the Rackspace
Cloud DNS by default.

#### Where can I find the Cloud DNS API documentation?

[http://docs.rackspace.com](http://docs.rackspace.com/)

#### How much does this service cost?

Cloud DNS is currently available at no additional cost, and is intended
for use with Cloud accounts that have provisioned and active resources.

#### Can this service be used for Dedicated Servers?

No. The Cloud DNS service is only available for Cloud account resources.
Managed / Dedicated customers with Rack Connect (i.e. those customers
who also have a Cloud account) have access, but can only use the service
to manage DNS for their Rackspace Cloud resources.

#### Does Cloud DNS work with Cloud Sites?

Absolutely; in addition to managing DNS in the Cloud Sites Control
Panel, you can view, edit and delete Cloud Sites domains can be viewed,
edited and deleted via Cloud DNS API. Domain registration is not
supported by the Cloud DNS API, but you can still register domains
through the existing Cloud Sites Control Panel.

**How does this work for Hybrid customers?**

A Hybrid customer will be able to continue to utilize MyRackspace.com to
manage domains for their dedicated resources, and will be able to
utilize Cloud DNS to manage domains for their Cloud resources.

\*\*Duplicate domains may not exist between Managed Hosting and Cloud
Hosting resources.\*\*

#### How do I authenticate with the Cloud DNS API?

The process for authenticating with the Cloud DNS API is the same when
authenticating with all other Rackspace Cloud APIs.

To authenticate, you must supply your username and API access key in
x-headers.

-   Use your Rackspace Cloud username as the username for the API. Place
    it in the XAuth-\
     User x-header.
-   [Obtain your API access
    key](http://www.rackspace.com/knowledge_center/article/view-and-reset-your-api-key)
    from the Rackspace Cloud Control Panel in the Your Account API
    Access section. Place it in the X-Auth-Key x-header.

For full authentication details, see the [Cloud DNS Developers
Guide](http://docs.rackspace.com/api).

#### What account number do I use to access the service?

Customers should use their existing Cloud account number.

#### What is the difference between US and UK Cloud DNS?

The functionality is the same.  The only difference is US and UK each
have their own separate API endpoint:

US = `https://dns.api.rackspacecloud.com/v1.0/1234/`\
 UK = `https://lon.dns.api.rackspacecloud.com/v1.0/1234/`

#### What DNS management operations does the Cloud DNS API support?

Customers can create, modify, remove and list domains, subdomains and
records.

Additionally, users can search domains by filtering. We do not support
filtering records.

For a full list of supported API operations, see the [Cloud DNS
Developers Guide](http://docs.rackspace.com/api).

#### What record types does Cloud DNS support?

The Cloud DNS API currently supports the following record types:

-   A
-   CNAME
-   MX
-   AAAA
-   NS
-   TXT
-   SRV
-   PTR ([Reverse
    DNS](http://docs.rackspace.com/cdns/api/v1.0/cdns-devguide/content/ReverseDNS-123456999.html))
-   SOA - you will not be able to create SOA records (as this is handled
    by the system) but you may modify TTL and email address

The service supports DKIM and SPF records through formatting TXT records
with custom attributes indicating the record type. We do not currently
support the SPF RR type as defined in [RFC
4408](http://tools.ietf.org/html/rfc4408).

#### Can I import and export domains?

Yes, via API. You can import a domain from external providers using a
valid bind9-formatted zone file. Similarly, you can export their domain
to a bind9-formatted file. Currently, you will not be able to export
zone files from MyRackspace to Cloud DNS and should contact Support to
request a domain transfer from dedicated resources to Cloud resources.

#### What are the Rackspace DNS servers?

Our default DNS servers are:

-   dns1.stabletransit.com

-   dns2.stabletransit.com

#### What type of DNS network does Rackspace use?

Rackspace leverages a globally distributed anycast Anycast network.
Currently we have DNS servers located in Texas, Virginia, Chicago, and
London. Using Anycast, we broadcast the IP addresses for
ns.rackspace.com and ns2.rackspace.com from each location. All DNS
queries will generally go to the geographically closest name servers,
giving you faster results no matter where your queries originate.
Additionally, all of our DNS servers are monitored 24/7 and if an entire
datacenter were to fail, or even if all of the DNS servers within a
specific datacenter were to fail, the DNS queries will automatically
start going to the next best location.

#### What are the limitations of the search functionality?

You will be able to search for domains within your own account.  The
functionality does not allow you to search for records.

#### Do my TTL settings expire?

No. 

#### What are the default TTL&rsquo;s for domains and records?

When a domain and/or record is created, and no TTL (Time To Live) is
specified, a default value of 3600 seconds is used. When the domain
and/or record TTL is supplied by the user via a create or update
operation, the specified TTL values must be 300 seconds or more.

#### How long does it take for DNS changes to be propagated globally?

Typical DNS propagation to Rackspace nameservers (globally) may take up
to one minute. This refers to the amount of time it takes after a change
(add/delete/update) is made to a customer's records via API, DNS
Manager, MyRackspace Customer Portal, Cloud Control, etc. before the
change is live on our nameservers. Large amount of changes made
simultaneously may take 2-3 minutes.

If a new domain is added or an existing domain is deleted, this may take
up to a few minutes to propagate to our Rackspace nameservers.

When changing nameservers for a domain, complete propagation will take
about 2 days for most domains. This is enforced by the registries.

#### Are there API rate limits?

All accounts, by default, have a preconfigured set of thresholds (or
limits) to manage capacity and prevent abuse of the system. The system
recognizes two kinds of limits: rate limits and absolute limits. Rate
limits are thresholds that are reset after a certain amount of time
passes. Absolute limits are fixed. See the [developers
guide](http://docs.rackspace.com/) for more information on rate limits.

#### How many Cloud DNS domains and records can I have?

By default, Cloud DNS users may have up to 500 domains (including
sub-domains) and 500 records per domain per Cloud account. When a user
submits a request to create new domains, records, and/or sub-domains,
the system will only accept the request if the total number of existing
plus requested domains, sub-domains and/or records is within the account
limits. If the total exceeds the account limit, the entire request will
be rejected and a '413 Request Entity Too Large' message will be
returned. See the [Cloud DNS Developer's
Guide](http://docs.rackspace.com/cdns/api/v1.0/cdns-devguide/content/overview.html)
for more information on absolute limits.

#### How can I create a Cloud DNS ticket?

You may submit Cloud DNS requests using the standard Support
ticket interface in the Control Panel.

