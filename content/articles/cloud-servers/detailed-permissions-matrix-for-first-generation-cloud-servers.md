---
node_id: 3532
title: Permissions Matrix for First Generation Cloud Servers
type: article
created_date: '2013-06-17 15:25:13'
created_by: renee.rendon
last_modified_date: '2016-01-11 20:4748'
last_modified_by: stephanie.fillmon
product: Cloud Servers
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in First Generation Cloud Servers. The matrix displays the method
names, their corresponding RESTful API commands, and the roles that are
supported.

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/)**

**[First Generation Servers terminology](#terminology)**

### **As of September 26, 2013**

CAPABILITY

ROLE

DESCRIPTION 

Method Name 

API Action

Observer

Admin

 

List All Servers

GET /servers

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all servers (IDs and names only).

List All Details for All Servers

GET /servers/detail

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all details for all servers.

 

Create a Server

POST /servers

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Creates a server.

 

List Details for a Specified Server

GET /servers/{id}

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists details for a specified server.

 

Update the Editable Attributes for a Specified Server (Server Name and
Password)

PUT /servers/{id}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png) 

Updates one or more editable attributes for a specified server. 

 

Delete a Specified Server

DELETE /servers/{id}

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

 

Deletes a specified server.

 

List All Server Addresses Associated with a Specified Server

GET /servers/{id}/ips

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all server addresses associated with a specified server.

 

List All Public Server Addresses

GET /servers/{id}/ips/public

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png) 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all public server addresses.

 

List All Private Server Addresses

GET /servers/{id}/ips/private

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all private server addresses.

 

Share Server Address

PUT /servers/{id}/ips/public/{address}

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Shares an IP address to the specified server.

 

Un-share Server Address

PUT /servers/{id}/ips/public/{address}

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Removes a shared IP address from the specified server.

 

Server Actions: Reboot Server (soft), Reboot Server (hard), Rebuild
Server, Resize Server, Confirm Resized Server, Revert Resized Server

POST /servers/{id}/action

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Performs the requested action.

 

List IDs, Names, and Links for All Available Flavors

GET /flavors

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists IDs, names, and links for all available flavors.

 

Lists All Details for All Available Flavors

GET /flavors/detail

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all details for all available flavors.

 

Lists Details of a Specified Flavor

GET /flavors/{id}

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists details of the specified flavor.

 

Lists IDs, Names, and Links for All Available Images

GET /images

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists IDs, names, and links for all available images.

 

List All Details for All Available Images

GET /images/detail

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

List all details for all available images.

 

List Details of a Specified Image

GET /images/{id}

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists details of the specified image.

 

Create a New Image

POST /images

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Creates a new image.

 

Delete a Specified Image

DELETE /images/{id}

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Delets a specified image.

 

List the Backup Schedule for a Specified Server

GET /servers/{id}/backup\_schedule

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists the backup schedule for a specified server.

 

Create/Update Backup Schedule for a Specified Server

POST /servers/{id}/backup\_schedule

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Creates or updates the backup schedule for a specified server.

 

Disable Backup Schedule

DELETE /servers/{id}/backup\_schedule

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Disables the backup schedule for a specified server.

 

List ID's and Names for Shared Address Groups

GET /shared\_ip\_groups

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists IDs and names for shared IP groups.

 

Lists All Details for Shared Address Groups

GET /shared\_ip\_groups/detail

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists all details for shared IP groups.

 

Create a Shared Address Group

POST /shared\_ip\_groups

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Creates a shared IP group.

 

Delete a Specified Shared Address Group

DELETE /shared\_ip\_groups/{id}

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists details for the specified shared IP group.

 

Get Current API Limits

GET /limits

 **![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Lists current API limits.

 

Get a URL for a Web Browser-mediated Console Session for a Specified
Server

GET /servers/{`id}`/console

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Gets a URL for a web browser-mediated console session for the specified
server.

 

Rescue/Unrescue a Server

POST /servers/{`id}`/rescue

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

 

Rescue or unrescue a server. 

Create a Next Generation Cloud Servers Image from a First Generation
Cloud Server that is Specified in the Request Body

POST /next\_gen\_image\_requests

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Creates a Next Generation Cloud Servers image from a First
Generation Cloud Server that is specified in the request body.

 

 
-

First Generation Cloud Servers terminology
------------------------------------------

### Flavor

A resource configuration for a server. Each flavor is a unique
combination of disk, memory, vCPUs, and network bandwidth.

### Image

A collection of files for a specific operating system (OS) that you use
to create or rebuild a server. Rackspace provides pre-built images. You
can also create custom images from servers that you have launched.
Custom images can be used for data backups or as "gold" images for
additional servers.

### Server

A virtual machine (VM) instance in the Cloud Servers environment. To
create a server, you must specify a name, flavor reference, and image
reference.

 

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

