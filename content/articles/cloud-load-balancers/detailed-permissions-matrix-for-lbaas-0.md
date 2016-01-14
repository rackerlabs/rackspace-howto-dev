---
node_id: 3390
title: Permissions Matrix for Cloud Load Balancers
type: article
created_date: '2013-04-10 16:05:06'
created_by: renee.rendon
last_modified_date: '2015-05-26 13:1148'
last_modified_by: kyle.laffoon
product: Cloud Load Balancers
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Load Balancers. The matrix displays the method names,
their corresponding RESTful API commands, and the roles that are
supported.

**[API Documentation](http://docs.rackspace.com/) **

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud Load Balancer
Terminology](#Cloud%20Load%20Balancer%20Terminology)**

**As of May 24, 2015**

CAPABILITY

ROLE

DESCRIPTION 

Method Name

API Action

Observer

Creator

Admin

 

### LOAD BALANCER

List Load Balancers

GET /loadbalancers

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Provide a list of all load balancers configured and associated with your
account.

List Load Balancer Details

GET /loadbalancers/{loadBalancerId}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Provide a list of all load balancers configured and associated with your
account. \*

Create Load Balancer

POST /loadbalancers

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Create a new load balancer with the configuration defined by the
request.

Update Load Balancer Attributes

PUT /loadbalancers/{loadBalancerId}

 

 ![check](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Asynchronously update the attributes of the specified load balancer.

Remove Load Balancer

DELETE /loadbalancers/{loadBalancerId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Remove the specified load balancer and its associated configuration from
the account.

Remove Load Balancer Batch Delete

DELETE /loadbalancers{?id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Bulk-delete load balancers.

### ERROR PAGES

List Error Page

GET /loadbalancers/{loadBalancerId}/errorpage

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List error page configured for the specified load balancer.

Update Error Page

PUT /loadbalancers/{loadBalancerId}/errorpage

 

 ![check](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Set custom error page for the specified load balancer.

Delete Error Page

DELETE /loadbalancers/{loadBalancerId}/errorpage

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete custom error page for the specified load balancer.

### LOAD BALANCER STATISTICS

List Load Balancer Stats

GET /loadbalancers/{loadBalancerId}/stats

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Provide detailed stats output for a specific load balancer.

### NODES

List Nodes

GET /loadbalancers/{loadBalancerId}/nodes

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List node(s) configured for the load balancer.

List Details of Specific Node

GET /loadbalancers/{loadBalancerId}/nodes/{nodeId}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List details of a specific node.

Add Nodes

POST /loadbalancers/{loadBalancerId}/nodes

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Add a new node to the load balancer.

Modify Nodes

PUT /loadbalancers/{loadBalancerId}/nodes/{nodeId}

 

 ![check](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Modify the configuration of a node on the load balancer.

Delete Nodes

DELETE /loadbalancers/{loadBalancerId}/nodes/{?nodeId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a node from a specified load balancer.

Delete Nodes Batch

DELETE /loadbalancers/{loadBalancerId}/nodes/{nodeId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Bulk-delete the specified nodes from a specified load balancer.

List Nodes

GET /loadbalancers/{loadBalancerId}/nodes

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List node(s) configured for the load balancer.

### VIRTUAL IPs

List Virtual IPs

GET /loadbalancers/loadBalancerId/virtualips

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List virtual IPs that are associated with a specified load balancer.

Add Virtual IPs

POST /loadbalancers/{loadBalancerId}/virtualips

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Add virtual IP version 6.

Bulk-delete Virtual IPs

DELETE /loadbalancers/{loadBalancerId}/virtualips/{?virtualIpId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Bulk-delete specified virtual IPs.

Delete Virtual IPs

GET /loadbalancers/{loadBalancerId}/virtualips/{virtualIpId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a specified virtual IP.

### ALLOWED DOMAINS

List Allowed Domains

GET /loadbalancers/alloweddomains

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

View a list of allowed domains. \*\*

### USAGE REPORTS

List Billable Load Balancers

GET /loadbalancers/billable{?startTime,endTime,offset, limit}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List billable load balancers for the given date range. The response is
paginated with a default limit of 500 and a maximum limit of 1000.

Show Account-level Usage

GET /loadbalancers/usage{?startTime,endTime}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show account-level usage.

Show Historical Usage

GET /loadbalancers/{loadBalancerId}/usage{?startTime,endTime}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show historical usage. \*\*\*

Show Current Usage

GET /loadbalancers/{loadBalancerId}/usage/current/{?startTime,endTime}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show current usage.

### ACCESS LISTS

Show Access List

GET /loadbalancers/{loadBalancerId}/accesslist

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show the access list.

Create or Update Access List

POST /loadbalancers/{loadBalancerId}/accesslist

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Create or append to an existing access list.

Delete Access List

DELETE /loadbalancers/{loadBalancerId}/accesslist

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete the entire access list.

Bulk-delete Specified Networks

DELETE /loadbalancers/{loadBalancerId}/accesslist/{?networkItemId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Bulk-delete the specified networks from an access list.

Delete Network Item from Access List

DELETE /loadbalancers/{loadBalancerId}/accesslist/ {networkItemId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a network item from a specified access list.

### MONITOR HEALTH

Show Health Monitor Configuration

GET /loadbalancers/{loadBalancerId}/healthmonitor

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show the health monitor configuration, if one exists.

Update Health Monitor

PUT /loadbalancers/loadBalancerId/healthmonitor

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Update the settings for a health monitor.

Delete Health Monitor

DELETE /loadbalancers/loadBalancerId/healthmonitor

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a health monitor.

### SESSION PERSISTENCE

Show Session Persistence Configuration

GET /loadbalancers/{loadBalancerId}/sessionpersistence

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List session persistence configuration.

Enable Session Persistence

PUT /loadbalancers/{loadBalancerId}/sessionpersistence

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Enable session persistence.

Disable Session Persistence

DELETE /loadbalancers/{loadBalancerId}/sessionpersistence

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Disable session persistence.

### LOG CONNECTIONS

Show Connection Logging Configuration

GET /loadbalancers/{loadBalancerId}/connectionlogging

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show connection logging configuration.

Enable or Disable Connection Logging

PUT /loadbalancers/{loadBalancerId}/connectionlogging

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Enable or disable connection logging.

Note: Enable connection logging requires that the user have access to
Cloud Files, which is used for storing the logs.

### THROTTLE CONNECTIONS

Show Connection Throttling Configuration

GET /loadbalancers/{loadBalancerId}/connectionthrottling

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show connection throttling configuration.

Create or Update Connection Throttling Configuration

PUT /loadbalancers/{loadBalancerId}/connectionthrottling

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Create or update throttling configuration.

Delete Connection Throttling Configuration

DELETE /loadbalancers/{loadBalancerId}/connectionthrottling

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete connection throttling configurations.

### CONTENT CACHING

Show Content Caching Configuration

GET /loadbalancers/{loadBalancerId}/contentcaching

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show current configuration of content caching.

Enable or Disable Content Caching

PUT /loadbalancers/{loadBalancerId}/contentcaching

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Enable or disable content caching.

### PROTOCOLS

List Load Balancer Protocols

GET /loadbalancers/protocol

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List supported load balancing protocols.

### ALGORITHMS

List Load Balancer Algorithms

GET /loadbalancers/algorithms

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List all supported load balancing algorithms.

### SSL TERMINATION / CERTIFICATE MAPPINGS

Show SSL Termination Configuration

GET /loadbalancers/{loadBalancerId}/ssltermination

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show the load balancer's SSL termination configuration.

Update SSL Termination

PUT /loadbalancers/{loadBalancerId}/ssltermination

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Update the SSL termination. \*\*\*\*\*

Delete SSL Termination

DELETE /loadbalancers/{loadBalancerId}/ssltermination

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete SSL termination.

List Certificate Mappings

GET /loadbalancers/{loadBalancerId}/ssltermination/certificatemappings

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

List certificate mappings that are configured for a specified load
balancer.

Add Certificate Mapping

POST /loadbalancers/{loadBalancerId}/ssltermination/certificatemappings

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Add a certificate mapping to a specified load balancer.

Show Certificate Mappings Details

GET
/loadbalancers/{loadBalancerId}/ssltermination/certificatemappings/{certificateMappingId}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show details for a specified certificate mapping.

Update Certificate Mapping

PUT
/loadbalancers/{loadBalancerId}/ssltermination/certificatemappings/{certificateMappingId}

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Update the configuration for a specified certificate mapping on a
specified load balancer.

Delete Certificate Mapping

DELETE
/loadbalancers/{loadBalancerId}/ssltermination/certificatemappings/{certificateMappingId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a certificate mapping from a specified load balancer.

### METADATA

Add Load Balancer Metadata 

POST /loadbalancers/{loadBalancerId}/metadata

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Add a new metadata item to the load balancer.

Show Load Balancer Metadata

GET /loadbalancers/{loadBalancerId}/metadata

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show all metadata associated with the specified load balancer.

Bulk-delete Load Balancer Metadata Items

DELETE /loadbalancers/{loadBalancerId}/metadata{?metaId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Bulk-delete the metadata items given specified id list.

Show Load Balancer Metadata Item

GET /loadbalancers/{loadBalancerId}/metadata/{metaId}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show details for a specified metadata item for a specified load
balancer.

Update Load Balancer Metadata Item

PUT /loadbalancers/{loadBalancerId}/metadata/{metaId}

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Update the configuration of a metadata item on the load balancer.

Delete Load Balancer Metadata Item

DELETE /loadbalancers/{loadBalancerId}/metadata/{metaId}

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a metadata item from the load balancer.

Show Load Balancer Node Metadata

GET loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata

 

 ![check](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show all metadata associated with a specified node and load balancer.

Add Load Balancer Node Metadata

POST loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata

 

 ![check](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Adds a metadata item to a specified node and load balancer.

Bulk-delete Load Balancer Node Metadata Items

DELETE loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadat{?metaId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Bulk-deletes the metadata items given specified id list.

Show Load Balancer Node Metadata Item

GET loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata/{metaId}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Show details for a specified metadata item for a specified node and load
balancer.

Update Load Balancer Node Metadata Item

PUT loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata/{metaId}

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Update the configuration of a metadata item on the node.

Delete Load Balancer Node Metadata Item 

loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata/{metaId}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

Delete a metadata item from the node.

### LIMITS

List Absolute Limits

 GET /loadbalancers/absolutelimits/

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

 Return the current absolute limits for the account.

List Limits

 GET /loadbalancers/limits

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_2.png)

 Return the current limits for the account.

\* This operation is not capable of returning details for a load
balancer which has been deleted.

\*\* Currently only Rackspace-based domain names are supported.

\*\*\* Historical usage data is available for up to 90 days of service
activity.

\*\*\*\*\* **Warning**: If SSL is enabled on a load balancer that is
configured with nodes that are NOT in the same datacenter, then
decrypted traffic will be sent in clear text over the public internet to
the external node(s) and will no longer be secure.

 

Cloud Load Balancer Terminology
-------------------------------

### Algorithm

A Process that defines how traffic should be directed between back-end
nodes.

### **Connection Logging**

A feature that allows logs to be delivered to a Cloud Files account
every hour. For HTTP-based protocol traffic, these are Apache-style
access logs. For all other traffic, this is connection and transfer
logging.

### [**Content Caching**](http://www.rackspace.com/knowledge_center/article/content-caching-for-cloud-load-balancers)

An operation that stores recently-accessed files on the load balancer
for easy retrieval by web clients. 

### **Error Page**

The HTML file that is shown to an end user who is attempting to access a
load balancer.

### **Health Monitor**

A configurable feature of each load balancer. It is used to determine
whether or not a back-end node is usable for processing a request. The
load balancing service currently supports active health monitoring.

### [**Load Balancer**](http://www.rackspace.com/knowledge_center/article/configuring-a-cloud-load-balancer-0#Virtual_IP_Type)

A logical device which belongs to a cloud account. It is used to
distribute workloads between multiple back-end systems or services,
based on the criteria defined as part of its configuration.

### Metadata

Metadata can be associated with each load balancer and each node for the
client's personal use. It is defined using key-value pairs where the key
and value consist of alphanumeric characters. A key is unique per load
balancer.

### **Node**

A back-end device providing a service on a specified IP and port.

### **Session Persistence**

A feature of the load balancing service that forces multiple requests
from clients to be directed to the same node.

### **Usage Reports**

A report that provides a view of all transfer activity, average number
of connections, and number of virtual IPs associated with the load
balancing service. 

### **Virtual IP**

An Internet Protocol (IP) configured on the load balancer for use by
clients connecting to a service that is load balanced. Incoming
connections are distributed to back-end nodes based on the configuration
of the load balancer.

 

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

