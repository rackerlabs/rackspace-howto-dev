---
node_id: 3653
title: Permissions Matrix for Cloud Networks
permalink: article/permissions-matrix-for-cloud-networks
type: article
created_date: '2013-08-20 20:40:08'
created_by: renee.rendon
last_modified_date: '2016-01-05 21:1210'
last_modified_by: Mike Asthalter
products: Cloud Hosting
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Networks. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.  

**[API Documentation](http://developer.rackspace.com/docs/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud Networks Terminology](#Cloud%20Networks%20Terminology)**

**As of October 30, 2014**

The following permissions matrix displays specific permissions for roles
using the Neutron API. 

CAPABILITY

ROLE

DESCRIPTION 

Method Name

API Action

Observer

Creator

Admin

 

### **NETWORKS**

List Networks

GET /networks

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists networks to which the specified tenant has access.

List Details for a Network

GET /networks/{network-id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows information for a specified network ID.

Create a Network

POST /networks

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a network.

Update a Specified Network

PUT /networks/{network-id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates editable attributes for a specified network.

Delete a Specified Network

DELETE /networks/{network-id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes the specified network and its associated resources.

### **SUBNETS**

List Subnets

GET /subnets

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists subnets to which the specified tenant has access.

List Details for a Subnet

GET /subnets/{subnet-id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows information for a specified subnet.

Create a Subnet

POST /subnets

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a subnet on a specified network.

Update a Specified Subnet

PUT /subnets/{subnet-id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates editable attributes for a specified subnet.

Delete a Subnet

DELETES /subnets/{subnet-id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a specified subnet.

### **PORTS**

List Ports

GET /ports

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists ports to which the tenant has access.

List Details for a Port

GET /ports/{port-id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows information for a specified port.

Create a Port

POST /ports

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a port on a specified network.

Update Editable Attribute of a Port

PUT /ports/{port-id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates a editable attributes for a specified port.

Delete Specified Port

DELETE /ports/{port-id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a specified port.

 

The following permissions matrix displays specific permissions for the
roles using the nova-network API. 

CAPABILITY

ROLE

DESCRIPTION 

Method Name

API Action

Observer

Creator

Admin

 

**Networks**

 

 

 

 

 

List Networks 

GET/os-networksv2

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists the networks configured for a specified tenant ID.

Create Network 

POST/os-networksv2

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a network for the specified tenant ID.

Provision Server and Attach Networks

POST/servers

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Provisions a new server and attaches networks.

Show Network

GET/os-networkv2/id

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows information for a specified network ID. 

Delete Network 

DELETE/GET/os-networkv2/id

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 Deletes the specified network.

**Virtual Interfaces**

 

 

 

 

 

List Virtual Interfaces

GET/servers/instance\_id/os-virtual-interfacesv2

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists the virtual interfaces configured for a server instance.

Create Virtual Interface

POST/servers/instance\_id/os-virtual-interfacesv2

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a virtual interface for a network and attaches the network to a
server instances.

Delete Virtual Interface

DELETE/servers/instances\_id/os-virtual-interfacesv2/interface\_id

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 Deletes a virtual interface from a server instance.

 
-

Cloud Networks Terminology
--------------------------

**Network**

A sequence of connection points that communicate with each other.

**Server**

A virtual machine (VM) instance in the Cloud Servers environment. To
create a server, you must specify a name, flavor reference, and image
reference.

**Virtual Interface**

An extension to the networking API that is specifically used for
attaching and detaching networks.

###  

[\< Permissions Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
-------------------------------------------------------------------------------------------------------------------------------------------

 

