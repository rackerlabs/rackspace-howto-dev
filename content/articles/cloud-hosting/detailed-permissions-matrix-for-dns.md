---
node_id: 3393
title: Detailed Permissions Matrix for DNS
type: article
created_date: '2013-04-10 16:16:15'
created_by: renee.rendon
last_modified_date: '2014-10-30 20:3417'
last_modified_by: David Hendler
products: Cloud Hosting
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud DNS. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.  

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud DNS Terminology](#Cloud%20DNS%20Terminology)**

**As of July 16, 2014**

CAPABILITY

ROLE

DESCRIPTION 

Method Name

API Action

Observer

Creator

Admin

 

### LIMITS

List All Limits

GET /limits

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all applicable limits.

List Limit Types

GET /limits/types

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists the types of limits.

List Specific Limit

GET /limits/*type* (/limits/*domain\_limit*, /limits/*rate\_limit*,
/limits/*domain\_record\_limit*)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

List assigned limits of the specified type. 

### DOMAINS

List Domains

GET /domains

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all account domains. 

List Domains by Name

GET /domains?name=*domainName*

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Filters domains by domain name: lists all domains manageable by the
account specified that exactly match the the value of the name
parameter.

List Domain Details

GET /domains/*domainId*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists details for a specific domain. By default this call displays
information for records but not subdomains. 

List Domain Changes

GET /domains/*domainId*/changes?*since*=[date/time]

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows all changes to the specified domain `since` the
specified `date/time`{.code style="font-size: 12px;"}.

Export Domain

GET /domains/*domainId*/export

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Exports details of the specified domain. 

Search Domains

GET /domains/search{?name}

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Searches domains by domain name: lists all names manageable by the
specified account that have the value of the name parameter as part of
their name.

Create Domain(s) 

POST /domains

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a new domain.

Clone Domain

POST /domains/*domainId*/clone?cloneName=*new-domain-name*

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates specified domain by cloning domain with id*domainId*. 

Import Domain

POST /domains/import

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Imports a new domain with the configuration specified by the request.

Modify Single Domain

PUT /domains/*domainId*

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Modifies the configuration of a domain. 

Modify Multiple Domains

PUT /domains

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Modifies multiple domains. 

Remove Single Domain

DELETE /domains/*domainId*

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes a domain. 

Remove Single Domain + Subdomains

DELETE /domains/*domainId*?deleteSubdomains=true

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes a domain and all its subdomains. 

Remove Multiple Domains

DELETE /domains?id=*domainId1*&id=*domainId2*

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes multiple domains.

Remove Multiple Domains + Subdomains

DELETE /domains?id=*domainId1*&id=*domainId2*&deleteSubdomains=true

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes multiple domains and their subdomains. 

### SUBDOMAINS

List Subdomains

GET /domains/*domainId*/subdomains

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists domains that are subdomains of the specified domain.

### RECORDS

List Records

GET /domains/*domainId*/records

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all records configured for the domain.  

Search Records

GET
/domains/*domainId*/records?type=record\_type &name=record\_name &data=record\_data

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all records for the specified domain of the specified type that
match the specified *`name`* and/or *`data`*. 

List Record Details

GET /domains/*domainId*/records/*recordId*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists details for a specific record. 

Add Records

POST /domains/*domainId*/records

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Adds new record(s) to the domain. 

Modify Single Record

PUT /domains/*domainId*/records/*recordId*

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Modifies the configuration of a record in the domain.

Modify Multiple Records

PUT /domains/*domainId*/records

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Modifies the configuration of records in the domain.

Delete Single Record

DELETE /domains/*domainId*/records/*recordId*

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes a record from the domain. 

Delete Multiple Records

DELETE /domains/*domainId*/records?id=*recordId1*&id=*recordId2*

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes multiple records from the domain. 

### REVERSE DNS

**Note:** For Reverse DNS, in order to create a PTR record for a Cloud
Load Balancer, First Generation Cloud Server, or Next Generation Cloud
Server, you will additionally need at least the Observer role for the
service you are associating the PTR record with.

List PTR Records

GET /rdns/*service\_name*?href=*device-resource-uri*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all PTR records configured for a Rackspace Cloud device. 

List PTR Record Details

GET /rdns/*service\_name*/*recordId*?href=*device-resource-uri*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists details for a specific PTR record associated with a Rackspace
Cloud device. 

Add PTR Records

POST /rdns

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Adds new PTR record(s) for a Rackspace Cloud device. 

Modify PTR Records

PUT /rdns

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Modifies one or more PTR records associated with a Rackspace Cloud
device. 

Remove PTR Records

DELETE
/rdns/*service-name*?href=*device-resource-uri*&ip=*optional-ip-address*

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Removes one or all PTR records associated with a Rackspace Cloud
device. 

### JOB STATUS

View Jobs Status

GET */status/*`jobId`*?*`showDetails=[true|false]`**

GET
/status?*showDetails*=true|false&*showErrors*=true|false&*showRunning*=
true|false&*showCompleted*=true|false&*limit*=int1&*offset*=int2

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png) 

Lists status of all asynchronous job requests for an account and filters
the information requested by using the optional boolean request
parameters. 

 
-

Cloud DNS Terminology
---------------------

**DNS**

The Domain Name System (DNS) is a system by which internet domain
name-to-address and address-to-name resolutions are determined. All
domains and their components, such as mail servers, utilize DNS to
resolve to the appropriate locations. DNS servers are usually set up in
a master-slave relationship such that failure of the master invokes the
slave. DNS servers may also be clustered or replicated such that changes
made to one DNS server are automatically propagated to other active
servers.

**Domain**

A domain is an entity/container of all DNS-related information
containing one or more records.

**Record**

A DNS record belongs to a particular domain and is used to specify
information about the domain. There are several types of DNS records.
Each record type contains particular information used to describe that
record's purpose. Examples include mail exchange (MX) records, which
specify the mail server for a particular domain, and name server (NS)
records, which specify the authoritative name servers for a domain.

**Subdomain**

Subdomains are domains within a parent domain, and subdomains cannot be
registered. Subdomains allow you to delegate domains. Subdomains can
themselves have subdomains, so third-level, fourth-level, fifth-level,
and deeper levels of nesting are possible.

###  

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

