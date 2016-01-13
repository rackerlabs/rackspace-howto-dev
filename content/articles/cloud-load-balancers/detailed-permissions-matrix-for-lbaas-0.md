---
node_id: 3390
title: Permissions Matrix for Cloud Load Balancers
type: article
created_date: '2013-04-10 16:05:06'
created_by: renee.rendon
last_modified_date: '2015-05-26 13:1148'
last_modified_by: kyle.laffoon
products: Cloud Load Balancers
body_format: tinymce
---

undefined{?metaId}

 

 

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

 

