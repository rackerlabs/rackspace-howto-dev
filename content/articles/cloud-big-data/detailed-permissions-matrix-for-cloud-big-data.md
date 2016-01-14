---
node_id: 3680
title: Detailed Permissions Matrix for Cloud Big Data
type: article
created_date: '2013-09-12 18:53:10'
created_by: renee.rendon
last_modified_date: '2016-01-11 20:4256'
last_modified_by: stephanie.fillmon
product: Cloud Big Data
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Big Data v1. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.  

**[API Documentation](http://docs.rackspace.com/)**

**[Cloud Big Data Terminology](#bigdata)**

### As of February 4, 2014    

CAPABILITY

ROLE

Description

Method Name

API Call

Observer

Creator

Admin

 

### PROFILES

Get User Profile

GET /profile

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns detailed profile information for the current user. 

 

Create a User Profile

POST /profile

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Creates a profile or updates the information in an existing profile. 

 

### CLUSTERS

Create a Cluster

POST /clusters

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Creates a new cluster.

 

Delete a Cluster

DELETE /clusters/{clusterId}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Deletes a specified cluster.  

 

List Clusters

GET /clusters

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists all clusters for your account.  

 

Get Cluster Details

GET /clusters/{clusterId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns details for a specified cluster.  

 

Perform an Action on a Cluster

POST /clusters/{clusterId}/action

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 Performs an actionon a specified cluster, such as resizing.

 

### NODES

List Nodes in a cluster

GET /clusters/{clusterId}/nodes

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists all nodes for a specified cluster. 

 

Get Node Details

GET /clusters/{clusterId}/nodes/{nodeId}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns details for a specified node in a specified cluster.  

 

### FLAVORS

List Available Flavors 

GET /flavors 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists all available flavors. 

 

Get Flavor Details 

GET /flavors/{flavorId} 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists the details for the specified flavor. 

 

List Supported Cluster Types for a Flavor

GET /flavors/{flavorid}/types

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists the supported cluster types for the specified flavor. 

 

### TYPES

List Cluster Types

GET /types

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns a list of cluster types. 

 

Get Cluster Type Details 

GET /types/{typeId}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns details for the specified cluster type. 

 

List Supported Flavors for a Cluster Type

GET /types/{typeid}/flavors

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists the supported flavors for the specified cluster type.

 

### RESOURCE LIMITS

List Resource Limits for User

GET /limits

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Displays the resource limits for the user. 

 

 
-

Cloud Big Data Terminology
--------------------------

### Cluster

A group of servers (nodes). In Cloud Big Data, the servers are virtual.

### Node

In a network, a node is a connection point, either a redistribution
point or an end point for data transmissions. In general, a node has
programmed or engineered capability to recognize and process or forward
transmissions to other nodes.

[ **\< Permissions Matrices for RBAC**](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------------

###  

** **

** **

 

