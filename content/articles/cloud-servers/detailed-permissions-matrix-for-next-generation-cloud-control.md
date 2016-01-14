---
node_id: 3386
title: Permissions Matrix for Next Generation Cloud Servers
type: article
created_date: '2013-04-10 15:53:07'
created_by: renee.rendon
last_modified_date: '2016-01-14 19:2351'
last_modified_by: rose.contreras
product: Cloud Servers
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Next Gen Cloud Servers. The matrix displays the method names,
their corresponding RESTful API commands, and the roles that are
supported.  

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Next Generation Cloud Servers
Terminology](#Next%20Generation%20Cloud%20Servers%20Terminology)**

### **As of April 21, 2014**

CAPABILITY

ROLE

DESCRIPTION 

Method Name

API Action

Observer

Creator

Admin

 

### Servers

List Servers

GET /servers

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists IDs, names, and links for all servers.

List All Details for All Servers

GET /servers/detail

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all details for all servers. 

Create Server

POST /servers

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a server.

Get Server Details

GET /servers/{id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists details for a specified server.

Update Server

PUT /servers/{id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates one or more editable attributes for a specified server.

Delete Server

\*Note: The user must also have a Cloud Block Storage Admin role. 

DELETE /servers/{id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a specified server.

### Server Key Pairs

Create or Upload a New Keypair

POST /os-keypairs

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Generates or uploads a keypair consisting of private key/public key.

List Keypairs

GET /os-keypairs

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists a keypair consisting of private key/public key.

Delete Server Keypair

DELETE /os-keypairs/{keypair name}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a keypair of a specified name.

### Server Addresses

List Addresses

GET /servers/{id}/ips

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all networks and server addresses associated with a specified
server.

List Addresses by Network

GET /servers/{id}/ips/{networkLabel}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists addresses associated with a specified server and network.

### Server Actions

Change Administrator password, Reboot Server, Rebuild Server, Resize
Server, Confirm Resized Server, Revert Resized Server, Enter Resuce
Mode, Exit Rescue Mode, or Create Image

POST /servers/{id}/action

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Performs the requested action.

### Volume Attachment Actions

Attach Volume to Server

\*Note: The user must also have a Cloud Block Storage Admin or Creator
role. 

POST /servers/{id}/os-volume\_attachments

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Attaches a volume to the specified server.

List Volume Attachments

GET /servers/{id}/os-volume\_attachments

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists the volume attachments for the specified server.

Get Volume Attachment Details

GET /servers/{id}/os-volume\_attachments/{attachment\_id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists volume details for the specified volume attachment ID.

Delete Volume Attachment

DELETE /servers/{id}/os-volume\_attachments/{attachment\_id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a specified volume attachment from a specified server instance.

### Flavors

List Flavors

GET /flavors

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists IDs, names, and links for all available flavors.

Get All Flavors Details

GET /flavors/detail

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all details for all available flavors.

Get Flavor Details

GET /flavors/{id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists details of the specified flavor.

### Images

Create Images

POST /servers/{id}/action

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates an image.

List Images

GET /images

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists IDs, names, and links for all available images.

Get All Image Details

GET /images/detail

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

List all details for all available images.

Get Image Details

GET /images/{id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists details of the specified image

Delete Image

DELETE /images/{id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes the specified image.

### Metadata

List Metadata Associated with a Server

GET /servers/{id}/metadata

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all metadata associated with a server.

List Metadata Associated with an Image

GET /images/{id}/metadata

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all metadata associated with an image.

Set Metadata for a Specified Server

PUT /servers/{id}/metadata

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Sets metadata for the specified server.

Set Metadata for a Specified Image

PUT /images/{id}/metadata

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Sets metadata for the specified image.

Update Metadata Items for a Specified Server

POST /servers/{id}/metadata

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates metadata items for the specified server.

Update Metadata Items for a Specified Image

POST /images/{id}/metadata

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates metadata items for the specified image.

Get a Metadata Item Associated with a Server

GET /servers/{id}/metadata/key

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Retrieves a single metadata item associated with a server.

Get a Metadata Item Associated with an Image

GET /images/{id}/metadata/key

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Retrieves a single metadata item associated with an image.

Set a Metadata Item for a Specified Server

PUT /servers/{id}/metadata/{key}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Sets a metadata item for a specified server.

Set a Metadata Item for a Specified Image

PUT /images/{id}/metadata/{key}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Sets a metadata item for a specified image.

Delete a Metadata Item for a Specified Server

DELETE /servers/{id}/metadata/{key}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a metadata item for the specified server.

Delete a Metadata Item for a Specified Image

DELETE /images/{id}/metadata/{key}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a metadata item for the specified image.

### RACKSPACE EXTENSIONS

**Used Limits Extension**

Used Limits Extension

GET v2/{tenant\_id}/limits

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Extends limits to include information about the absolute limits that are
currently used.

**Scheduled Images Extension**

Enable Scheduled Images

POST /servers/{serverId}/rax-si-image-schedule

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Enables scheduled images on a server, by creating an image\_schedule
resource.

Show Scheduled Images

GET /servers/{serverId}/rax-si-image-schedule

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows scheduled images setting.

Disable Scheduled Images

DELETE /servers/{serverId}/rax-si-image-schedule

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Disables scheduled images by deleting the image\_schedule resource that
indicates the scheduled image service should create snapshots of this
server.

### CLOUD NETWORKS

**Networks**

List Networks

GET /os-networksv2

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists the networks configured for a specified tenant ID.

Create Network

POST /os-networksv2

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a network for a specified tenant ID.

Provision Server and Attach Networks

POST /os-networksv2

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Provisions a new server with specified networks.

Shows Network

GET /os-networksv2/{id}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows information for a specified network ID.

Delete Network

DELETE /os-networksv2/{id}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a specified network.

**Virtual Interfaces**

List Virtual Interfaces 

GET /servers/{instance\_id}/os-virtual-interfacesv2

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists all virtual interfaces configured for a server instance.

Create Virtual Interface 

POST /servers/{instance\_id}/os-virtual-interfacesv2

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a virtual interface for a network and attaches the network to a
server instance.

Delete Virtual Interface

DELETE /servers/{instance\_id}/os-virtual-interfacesv2/interface\_id

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes a virtual interface from a server instance.

 
-

Next Generation Cloud Servers Terminology
-----------------------------------------

### Flavor

A resource configuration for a server. Each flavor is a unique
combination of disk, memory, vCPUs, and network bandwidth.

### Image

A collection of files for a specific operating system (OS) that you use
to create or rebuild a server. Rackspace provides pre-built images. You
can also create custom images from servers that you have launched.
Custom images can be used for data backups or as "gold" images for
additional servers.

### Key Pair

A cryptographic combination of public and private keys used for
asymmetric encryption.

### Server

A virtual machine (VM) instance in the Cloud Servers environment. To
create a server, you must specify a name, flavor reference, and image
reference.

 

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

