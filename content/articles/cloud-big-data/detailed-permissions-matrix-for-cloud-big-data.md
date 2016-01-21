---
node_id: 3680
title: Detailed Permissions Matrix for Cloud Big Data
type: article
created_date: '2013-09-12'
created_by: Renee Rendon
last_modified_date: '2016-01-15'
last_modified_by: Rose Contreras
product: Cloud Big Data
---

The following permissions matrix displays specific permissions for the
roles in Cloud Big Data v1. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.
\[\*\*API Documentation\*\*\](http://docs.rackspace.com/) \[\*\*Cloud
Big Data Terminology\*\*\](\#bigdata) \#\#\# As of February 4, 2014
Method | API Action | Role | Description :---: | :---: | :---:
\*\*PROFILES\*\* | | | Get User Profile | `GET /profile` | \*\*Observer
& Creator & Admin\*\* | Returns detailed profile information for the
current user. Create a User Profile | `POST /profile` | \*\*Creator &
Admin\*\* | Creates a profile or updates the information in an existing
profile. \*\*CLUSTERS\*\* | | | Create a Cluster | `POST /clusters` |
\*\*Creator & Admin\*\* | Creates a new cluster. Delete a Cluster |
`DELETE /clusters/{clusterId}` | \*\*Admin only\*\* | Deletes a
specified cluster. List Clusters | `GET /clusters` | \*\*Observer &
Creator & Admin\*\* | Lists all clusters for your account. Get Cluster
Details | `GET /clusters/{clusterId}` | \*\*Observer & Creator &
Admin\*\* | Returns details for a specified cluster. Perform an Action
on a Cluster | `POST /clusters/{clusterId}/action` | \*\*Creator &
Admin\*\* | Performs an actionon a specified cluster, such as resizing.
\*\*NODES\*\* | | | List Nodes in a cluster |
`GET /clusters/{clusterId}/nodes` | \*\*Observer & Creator & Admin\*\* |
Lists all nodes for a specified cluster. Get Node Details |
`GET /clusters/{clusterId}/nodes/{nodeId}` | \*\*Observer & Creator &
Admin\*\* | Returns details for a specified node in a specified cluster.
\*\*FLAVORS\*\* | | | List Available Flavors |`GET /flavors ` |
\*\*Observer & Creator & Admin\*\* | Lists all available flavors. Get
Flavor Details | `GET /flavors/{flavorId}` | \*\*Observer & Creator &
Admin\*\* | Lists the details for the specified flavor. List Supported
Cluster Types for a Flavor | `GET /flavors/{flavorid}/types` |
\*\*Observer & Creator & Admin\*\* | Lists the supported cluster types
for the specified flavor. \*\*TYPES\*\* | | | List Cluster Types |
`GET /types` | \*\*Observer & Creator & Admin\*\* | Returns a list of
cluster types. Get Cluster Type Details | `GET /types/{typeId}` |
\*\*Observer & Creator & Admin\*\* | Returns details for the specified
cluster type. List Supported Flavors for a Cluster Type |
`GET /types/{typeid}/flavors` | Lists the supported flavors for the
specified cluster type. \*\*RESOURCE LIMITS\*\* | | | List Resource
Limits for User | `GET /limits` | Displays the resource limits for the
user.  \#\# Cloud Big Data Terminology \#\#\# Cluster A group of
servers (nodes). In Cloud Big Data, the servers are virtual. \#\#\# Node
In a network, a node is a connection point, either a redistribution
point or an end point for data transmissions. In general, a node has
programmed or engineered capability to recognize and process or forward
transmissions to other nodes. &lt;\[\#\#\# Permissions Matrices for
RBAC\](http://www.rackspace.com/knowledge\_center/article/permissions-matrix-for-role-based-access-control-rbac)

