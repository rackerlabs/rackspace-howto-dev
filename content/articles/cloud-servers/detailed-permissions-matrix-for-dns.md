---
node_id: 3393
title: Detailed Permissions Matrix for DNS
type: article
created_date: '2013-04-10'
created_by: Renee Rendon
last_modified_date: '2016-01-15'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud DNS. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](/howto/)**

**[Cloud DNS Terminology](#Cloud%20DNS%20Terminology)**

<span>**As of July 16, 2014**</span>

CAPABILITY

ROLE

DESCRIPTION

Method Name

API Action

Observer

Creator

Admin



### LIMITS

<span>List All Limits</span>

<span>GET /limits</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="39"
height="37"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="39"
height="37"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists all applicable limits.</span>

<span>List Limit Types</span>

<span>GET /limits/types</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists the types of limits.</span>

<span>List Specific Limit</span>

<span>GET
/limits/</span>*type*<span> (/limits/</span><span>*domain\_limit*,
/limits/*rate\_limit*,
/limits/*domain\_record\_limit*</span><span>)</span>

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>List assigned limits of the specified type.</span> </span>

### DOMAINS

<span>List Domains</span>

<span>GET /domains</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists all account domains. </span>

<span>List Domains by Name</span>

<span>GET /domains?name=</span>*<span>domainName</span>*

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Filters domains by domain name: lists all domains manageable by
the account specified that exactly match the the value of the name
parameter.</span>

<span>List Domain Details</span>

<span>GET /domains/</span>*<span class="s1">domainId</span>*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Lists details for a specific domain. By default this call
displays information for records but not subdomains.</span> </span>

<span>List Domain Changes</span>

<span class="s1">GET /domains/</span>*<span>domainId</span>*<span
class="s1">/changes?</span>*<span>since</span>*<span
class="s1">=</span><span>\[date/time\]</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Shows all changes to the specified domain </span>`since`<span> the
specified </span>`date/time`{.code}<span>.</span>

<span>Export Domain</span>

<span>GET /domains/</span>*<span
class="s1">domainId</span>*<span>/export</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Exports details of the specified domain.</span> </span>

<span>Search Domains</span>

<span>GET /domains/search{?name}</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

Searches domains by domain name: lists all names manageable by the
specified account that have the value of the name parameter as part of
their name.

<span>Create Domain(s) </span>

<span>POST /domains</span>



![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Creates a new domain.</span>

<span>Clone Domain</span>

<span>POST /domains/*domainId*/clone?cloneName=</span>*new-domain-name*



![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Creates specified domain</span><span> by cloning domain with
id</span><span>*domainId*</span><span>. </span>

<span>Import Domain</span>

<span>POST /domains/import</span>



 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Imports a new domain with the configuration specified by the
request.</span>

<span>Modify Single Domain</span>

<span>PUT /domains/</span>*<span>domainId</span>*



![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Modifies the configuration of a domain.</span> </span>

<span>Modify Multiple Domains</span>

<span>PUT /domains</span>



![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Modifies multiple domains.</span>

<span>Remove Single Domain</span>

<span>DELETE /domains/</span>*<span class="s1">domainId</span>*





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Removes a domain.</span> </span>

<span>Remove Single Domain + Subdomains</span>

<span>DELETE /domains/</span>*<span
class="s1">domainId</span>*<span>?deleteSubdomains=true</span>





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Removes a domain and all its subdomains.</span> </span>

<span>Remove Multiple Domains</span>

<span>DELETE /domains?id=*domainId1*&id=*domainId2*</span>





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Removes multiple domains.</span>

<span>Remove Multiple Domains + Subdomains</span>

<span>DELETE /domains?id=</span>*<span
class="s1">domainId1</span>*<span>&id=</span>*<span
class="s1">domainId2</span>*<span>&deleteSubdomains=true</span>





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Removes multiple domains and their
subdomains.</span> </span>

### SUBDOMAINS

<span>List Subdomains</span>

<span>GET /domains/</span>*<span
class="s1">domainId</span>*<span>/subdomains</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists domains that are subdomains of the specified domain.</span>

### RECORDS

<span>List Records</span>

<span>GET /domains/</span>*<span
class="s1">domainId</span>*<span>/records</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists all records configured for the domain.  </span>

<span>Search Records</span>

<span class="s1">GET /domains/</span>*<span>domainId</span>*<span
class="s1">/records?type=</span><span>record\_type</span><span
class="s1"> &name=</span><span>record\_name</span><span
class="s1"> &data=</span><span>record\_data</span>

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists all records for the specified domain of the specified type
that match the specified *`name`* and/or *`data`*. </span>

<span>List Record Details</span>

<span>GET /domains/</span>*<span
class="s1">domainId</span>*<span>/records/</span>*<span
class="s1">recordId</span>*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Lists details for a specific record.</span> </span>

<span>Add Records</span>

<span>POST /domains/</span>*<span
class="s1">domainId</span>*<span>/records</span>



 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Adds new record(s) to the domain.</span> </span>

<span>Modify Single Record</span>

<span>PUT /domains/</span>*<span
class="s1">domainId</span>*<span>/records/</span>*<span
class="s1">recordId</span>*



 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Modifies the configuration of a record in the domain.</span>

<span>Modify Multiple Records</span>

<span>PUT /domains/</span>*<span
class="s1">domainId</span>*<span>/records</span>



 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Modifies the configuration of records in the domain.</span>

<span>Delete Single Record</span>

<span>DELETE /domains/</span>*<span
class="s1">domainId</span>*<span>/records/</span>*<span
class="s1">recordId</span>*





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Removes a record from the domain.</span> </span>

<span>Delete Multiple Records</span>

<span>DELETE /domains/</span>*<span
class="s1">domainId</span>*<span>/records?id=</span>*<span
class="s1">recordId1</span>*<span>&id=</span>*<span
class="s1">recordId2</span>*





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Removes multiple records from the domain.</span> </span>

### REVERSE DNS

**Note:** For Reverse DNS, in order to create a PTR record for a Cloud
Load Balancer, First Generation Cloud Server, or Next Generation Cloud
Server, you will additionally need at least the Observer role for the
service you are associating the PTR record with.

<span>List PTR Records</span>

<span class="s1">GET /rdns/</span>*<span>service\_name</span>*<span
class="s1">?href=</span>*<span>device-resource-uri</span>*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Lists all PTR records configured for a Rackspace Cloud
device.</span> </span>

<span>List PTR Record Details</span>

<span class="s1">GET /rdns/</span>*<span>service\_name</span>*<span
class="s1">/</span>*<span>recordId</span>*<span
class="s1">?href=</span>*<span>device-resource-uri</span>*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Lists details for a specific PTR record associated with a
Rackspace Cloud device.</span> </span>

<span>Add PTR Records</span>

<span>POST /rdns</span>



 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Adds new PTR record(s) for a Rackspace Cloud
device.</span> </span>

<span>Modify PTR Records</span>

<span>PUT /rdns</span>



 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span><span>Modifies one or more PTR records associated with a Rackspace
Cloud device.</span> </span>

<span>Remove PTR Records</span>

<span class="s1">DELETE /rdns/</span>*<span>service-name</span>*<span
class="s1">?href=</span>*<span>device-resource-uri</span>*<span
class="s1">&ip=</span>*<span>optional-ip-address</span>*





![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Removes one or all PTR records associated with a Rackspace Cloud
device. </span>

### JOB STATUS

<span>View Jobs Status</span>

<span>GET</span><span> </span>*/<span
class="highlight">status</span>/*`jobId`*?*`showDetails=[true|false]`**

GET
/status?*showDetails*=true|false&*showErrors*=true|false&*showRunning*=
true|false&*showCompleted*=true|false&*limit*=int1&*offset*=int2

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png){width="41"
height="39"}

<span>Lists status of all asynchronous job requests for an account and
filters the information requested by using the optional boolean request
parameters. </span>


-

[]()Cloud DNS Terminology
-------------------------

**DNS**

<span>The Domain Name System (DNS) is a system by which internet domain
name-to-address and address-to-name resolutions are determined. All
domains and their components, such as mail servers, utilize DNS to
resolve to the appropriate locations. DNS servers are usually set up in
a master-slave relationship such that failure of the master invokes the
slave. DNS servers may also be clustered or replicated such that changes
made to one DNS server are automatically propagated to other active
servers.</span>

**<span>Domain</span>**

<span>A domain is an entity/container of all DNS-related information
containing one or more records.</span>

**<span>Record</span>**

<span>A DNS record belongs to a particular domain and is used to specify
information about the domain. There are several types of DNS records.
Each record type contains particular information used to describe that
record's purpose. Examples include mail exchange (MX) records, which
specify the mail server for a particular domain, and name server (NS)
records, which specify the authoritative name servers for a
domain.</span>

**<span>Subdomain</span>**

<span>Subdomains are domains within a parent domain, and subdomains
cannot be registered. Subdomains allow you to delegate domains.
Subdomains can themselves have subdomains, so third-level, fourth-level,
fifth-level, and deeper levels of nesting are possible.</span>

### <span> </span>

[&lt; Permission Matrices for RBAC](/howto/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



