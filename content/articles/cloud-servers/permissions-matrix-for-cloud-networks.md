---
node_id: 3653
title: Permissions Matrix for Cloud Networks
type: article
created_date: '2013-08-20'
created_by: Renee Rendon
last_modified_date: '2016-01-11'
last_modified_by: Rose Contreras
product: Cloud Servers
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Networks. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://developer.rackspace.com/docs/)**

**[Related Knowledge Center
Articles](/how-to/)**

**[Cloud Networks Terminology](#Cloud%20Networks%20Terminology)**

<span>**As of October 30, 2014**</span>

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

<span>List Networks</span>

<div>

<span>GET /networks</span>

</div>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Lists networks to which the specified tenant has access.</span>

<span>List Details for a Network</span>

<span>GET /networks/{network-id}</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Shows information for a specified network ID.</span>

<span>Create a Network</span>

<span>POST /networks</span>



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

Creates a network.

<span>Update a Specified Network</span>

<span>PUT /networks/{network-id}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Updates editable attributes for a specified network.</span>

<span>Delete a Specified Network</span>

<span>DELETE /networks/{network-id}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

Deletes the specified network and its associated resources.

### **SUBNETS**

<span>List Subnets</span>

<span>GET /subnets</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Lists subnets to which the specified tenant has access.</span>

<span>List Details for a Subnet</span>

<span>GET /subnets/{subnet-id}</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Shows information for a specified subnet.</span>

Create a Subnet

<span>POST /subnets</span>



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Creates a subnet on a specified network.</span>

<span>Update a Specified Subnet</span>

<span>PUT /</span><span>subnets/{subnet-id}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Updates editable attributes for a specified subnet.</span>

Delete a Subnet

<span>DELETES /subnets/{subnet-id}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

Deletes a specified subnet.

### **PORTS**

List Ports

<span>GET /ports</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Lists ports to which the tenant has access.</span>

List Details for a Port

<span>GET /ports/{port-id}</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Shows information for a specified port.</span>

Create a Port

<span>POST /ports</span>



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Creates a port on a specified network.</span>

<span>Update Editable Attribute of a Port</span>

<span>PUT /ports/{port-id}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Updates a editable attributes for a specified port.</span>

<span>Delete Specified Port</span>

<span>DELETE /ports/{port-id}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Deletes a specified port.</span>



<span>The following permissions matrix displays specific permissions for
the roles using the nova-network</span><span> API. </span>

CAPABILITY

ROLE

DESCRIPTION

Method Name

API Action

Observer

Creator

Admin



**<span>Networks</span>**









<span> </span>

List Networks

<span>GET/os-networksv2</span>

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

Lists the networks configured for a specified tenant ID.

Create Network

POST/os-networksv2



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Creates a network for the specified tenant ID.</span>

Provision Server and Attach Networks

POST/servers



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Provisions a new server and attaches networks.</span>

Show Network

GET/os-networkv2/id

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Shows information for a specified network ID. </span>

Delete Network

<span>DELETE/</span>GET/os-networkv2/id





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span> Deletes the specified network.</span>

**<span>Virtual Interfaces</span>**









<span> </span>

List Virtual Interfaces

<span>GET/servers/instance\_id/os-virtual-interfacesv2</span>

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Lists the virtual interfaces configured for a server
instance.</span>

Create Virtual Interface

POST/servers/instance\_id/os-virtual-interfacesv2



 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Creates a virtual interface for a network and attaches the network
to a server instances.</span>

Delete Virtual Interface

<span>DELETE/servers/instances\_id/os-virtual-interfacesv2/interface\_id</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span> Deletes a virtual interface from a server instance.</span>


-

[]()Cloud Networks Terminology
------------------------------

**<span>Network</span>**

<span><span>A sequence of connection points that communicate with each
other.</span></span>

**<span>Server</span>**

<span>A virtual machine (VM) instance in the Cloud Servers environment.
To create a server, you must specify a name, flavor reference, and image
reference.</span>

**<span>Virtual Interface</span>**

<span><span>An extension to the networking API that is specifically used
for a</span></span><span><span>ttaching and detaching
networks.</span></span>

### <span> </span>

[&lt; Permissions Matrices for RBAC](/how-to/permissions-matrix-for-role-based-access-control-rbac)
---------------------------------------------------------------------------------------------------------------------------------------------



