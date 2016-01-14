---
node_id: 1233
title: Rackspace Cloud DNS - Technical Details
type: article
created_date: '2011-10-19 21:06:42'
created_by: RackKCAdmin
last_modified_date: '2016-01-11 22:1142'
last_modified_by: rose.contreras
product: Cloud Servers
body_format: tinymce
---

### Previous section

**[Rackspace Cloud DNS - Available
Features](https://admin.rackspace.com/knowledge_center/cloud_dns_available_features)**

### Technical Details

Implementation of Rackspace Cloud DNS is available through our API. To
use our API, you should have a general understanding of DNS management
and be familiar with: 

-   RESTful Web Services
-   JSON and/or XML Data Serialization Formats

The list of currently available operations are shown below on this
chart:

Domains

Records

**- List Domains**

-   List all domains and subdomains manageable by the account specified.
    Displays ID's and names only.
-   Filter domains by domain name: list all domains and subdomains
    manageable by the account specified that match the *domainName*.
    Display ID's and names only.

**- List Records**

-   List all records configured for the domain or list the details for a
    specific record. SOA cannot be modified.

**- List Domain Details**

-   List details of the specified domain. Display all details, including
    records. This operation provides the detailed output for a specific
    domain configured and associated with an account. This operation is
    not capable of returning details for a domain that has been deleted.

**- List Record Details**

- **Create Domain(s)**

-   This operation provisions one or more new DNS domains under the
    account specified, based on the configuration defined in the request
    object. If the corresponding request cannot be fulfilled due to
    insufficient or invalid data, an HTTP 400 (Bad Request) error
    response will be returned with information regarding the nature of
    the failure in the body of the response. Failures in the validation
    process are non-recoverable and require the caller to correct the
    cause of the failure and POST the request again.

**- Add Records**

-   Add new record(s) to the domain.

**- Modify Domain(s)**

-   This operation modifies DNS domain(s) attributes only. Records
    cannot be added, modified or removed. Only the TTL and e-mail
    address attributes of a domain can be modified.

**- Modify Records**

-   Modify the configuration of a record or records in a domain.

**- Delete Domain(s)**

-   This operation removes one or more specified domains from the
    account; when a domain is deleted, its immediate resource records
    are also deleted from the account. By default, if a deleted domain
    had subdomains, each subdomain becomes a root domain and is not
    deleted. This can be overridden by the optional *deleteSubdomains*
    parameter.
-   When a domain is deleted, any and all configuration data is
    immediately purged and is not recoverable via the API. In a request
    to remove multiple domains, a failure on a single part of the
    request will cause the entire request to fail. Utilizing the
    optional *deleteSubdomains* parameter on domains without subdomains
    does not result in a failure.

**- Remove Records**

-   Remove a record or multiple records from a domain.

**- Search (Filter Domains)**

 

**- Import Domain**

-   This operation provisions a new DNS domain under the account
    specified by the bind9 - formatted file configuration contents
    defined in the request object. If the corresponding request cannot
    be fulfilled due to insufficient or invalid data, an HTTP 400 (Bad
    Request) error response will be returned with information regarding
    the nature of the failure in the body of the response. Failures in
    the validation process are non-recoverable and require the caller to
    correct the cause of the failure and POST the request again.

 

**- Export Domain**

-   This operation provides the bind9-formatted contents of the
    requested domain. This operation is for a single domain only, and as
    such, does not traverse up or down the domain hierarchy for details
    (that is, no subdomain information is provided). 

 

Prior to this API we supported only a few DNS record types. With the new
API we have added support for NS, TXT and SRV records. Let's dive into
the details of these new record types: 

-   NS (Name Server) records indicate where the domain's DNS hosting
    services are located. It effectively delegates a domain to use a set
    of name servers.
-   TXT records are used primarily for SPF and DKIM records. An SPF
    (Sender Policy Framework) record allows administrators to specify
    which hosts are allowed to send e-mail from a domain by creating a
    specific SPF record in the public (DNS). Mail exchangers then use
    the DNS to check that mail from a given domain is being sent by a
    host sanctioned by that domain's administrators. DomainKeys
    Identified Mail (DKIM) is a method for associating a domain name to
    an email, thereby allowing an organization to take responsibility
    for a message in a way that can be validated by a recipient.
-   SRV records are used to define the location of a (hostname and port)
    of servers used for a specific service.

For a full list of record types and their definitions, please click
[here](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-dns-additional-resources).

### Next steps

**[Rackspace Cloud DNS - API
Example](https://admin.rackspace.com/knowledge_center/cloud_dns_api_example)**

