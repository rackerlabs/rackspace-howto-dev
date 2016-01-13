---
node_id: 1235
title: Rackspace Cloud DNS - Additional Resources
type: article
created_date: '2011-10-19 21:07:51'
created_by: RackKCAdmin
last_modified_date: '2016-01-11 22:1339'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

### Prior section

**[Rackspace Cloud DNS - API
Example](https://admin.rackspace.com/knowledge_center/cloud_dns_api_example)**

**Resources**

- For more information regarding the API, we encourage you to review the
***Rackspace Cloud DNS API documentation*** which is
located [here](http://docs.rackspace.com/api/%20). 

**Supported Record Types**

-   **A** - IPv4 address used to map hostnames to an IP address of the
    host.
-   **CNAME (Canonical Name Record)** - Points to another hostname that
    already has an A record associated with it. The CNAME record works
    like an alias. 
-   **MX** - Used to specify a mail server that is responsible for
    accepting email messages on behalf of a recipient domain.
-   **SOA** - Specifies authoritive information about a domain,
    including the primary name server(s), the email of the domain
    administrator, the domain serial number, and TTL's.
-   **AAAA** - IPv6 address used to map hostnames to an IP address of
    the host.
-   **NS (Name Server)** - NS records indicate where the domain's DNS
    hosting services are located. It effectively delegates a domain to
    use a set of name servers.
-   **TXT** - This is a text record and is used primarily for SPF and
    DKIM records.

- A SPF (Sender Policy Framework) record allows administrators to
specify which hosts are allowed to send e-mail from a given domain by
creating a specific SPF record in the public (DNS). Mail exchangers use
the DNS to check that mail from a given domain is being sent by a host
sanctioned by that domain's administrator.

- DomainKeys (DKIM) is a method for associating a domain name to an
e-mail, thereby allowing an organization to take responsibility for a
message in a way that can be validated by a recipient. 

-   **SRV** - Used to define the location (hostname and port) of servers
    used for a specific service. 

 

### Next steps

[**Rackspace Cloud DNS - Frequently Asked
Questions**](https://admin.rackspace.com/knowledge_center/cloud_dns_faq)

