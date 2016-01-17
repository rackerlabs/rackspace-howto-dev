---
node_id: 3532
title: Permissions Matrix for First Generation Cloud Servers
type: article
created_date: '2013-06-17'
created_by: Renee Rendon
last_modified_date: '2016-01-11'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
body_format: tinymce
---

<span>The following permissions matrix displays specific permissions for
the roles in First Generation Cloud Servers. The matrix displays the
method names, their corresponding RESTful API commands, and the roles
that are supported.</span>

**<span>[API Documentation](http://docs.rackspace.com/)</span>**

**<span>[Related Knowledge Center
Articles](/howto/)</span>**

**<span>[First Generation Servers terminology](#terminology)</span>**

### <span>**As of September 26, 2013**</span>

CAPABILITY

ROLE

DESCRIPTION

Method Name

API Action

Observer

Admin



<span>List All Servers</span>

<span>GET /servers</span>

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all servers (IDs and names only).</span>

<span>List All Details for All Servers</span>

<span>GET /servers/detail</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all details for all servers.</span>



<div>

<span>Create a Server</span>

</div>

<span>POST /servers</span>



**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Creates a server.</span>



<span>List Details for a Specified Server</span>

<span>GET /servers/{id}</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists details for a specified server.</span>



<span>Update the Editable Attributes for a Specified Server
(</span><span>Server Name and Password)</span>

<span>PUT /servers/{id}</span>

<div>



</div>

<div>

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}

</div>

<span>Updates one or more editable attributes for a specified
server.</span>



<span>Delete a Specified Server</span>

<span>DELETE /servers/{id}</span>



<div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

<div>



</div>

<span>Deletes a specified server.</span>



<span>List All Server Addresses Associated with a Specified
Server</span>

<span>GET /servers/{id}/ips</span>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all server addresses associated with a specified
server.</span>



<span>List All Public Server Addresses</span>

<span>GET /servers/{id}/ips/public</span>

<div>

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all public server addresses.</span>



<span>List All Private Server Addresses</span>

<span>GET /servers/{id}/ips/private</span>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all private server addresses.</span>



<span>Share Server Address</span>

<span>PUT /servers/{id}/ips/public/{address}</span>



**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Shares an IP address to the specified server.</span>



<span>Un-share Server Address</span>

<span>PUT /servers/{id}/ips/public/{address}</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Removes a shared IP address from the specified server.</span>



<span>Server Actions: Reboot Server (soft), Reboot Server (hard),
Rebuild Server, Resize Server, Confirm Resized Server, Revert Resized
Server</span>

<span>POST /servers/{id}/action</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Performs the requested action.</span>



<span>List IDs, Names, and Links for All Available Flavors</span>

<span>GET /flavors</span>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists IDs, names, and links for all available flavors.</span>



<span>Lists All Details for All Available Flavors</span>

<span>GET /flavors/detail</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all details for all available flavors.</span>



<span>Lists Details of a Specified Flavor</span>

<span>GET /flavors/{id}</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists details of the specified flavor.</span>



<span>Lists IDs, Names, and Links for All Available Images</span>

<span>GET /images</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists IDs, names, and links for all available images.</span>



<span>List All Details for All Available Images</span>

<span>GET /images/detail</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>List all details for all available images.</span>



<span>List Details of a Specified Image</span>

<span>GET /images/{id}</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists details of the specified image.</span>



<span>Create a New Image</span>

<span>POST /images</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

Creates a new image.



<span>Delete a Specified Image</span>

<span>DELETE /images/{id}</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

Delets a specified image.



<span>List the Backup Schedule for a Specified Server</span>

<span>GET /servers/{id}/backup\_schedule</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

Lists the backup schedule for a specified server.



<span>Create/Update Backup Schedule for a Specified Server</span>

<span>POST /servers/{id}/backup\_schedule</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

Creates or updates the backup schedule for a specified server.



<span>Disable Backup Schedule</span>

<span>DELETE /servers/{id}/backup\_schedule</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Disables the backup schedule for a specified server.</span>



<span>List ID's and Names for Shared Address Groups</span>

<span>GET /shared\_ip\_groups</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists IDs and names for shared IP groups.</span>



<span>Lists All Details for Shared Address Groups</span>

<span>GET /shared\_ip\_groups/detail</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists all details for shared IP groups.</span>



<span>Create a Shared Address Group</span>

<span>POST /shared\_ip\_groups</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Creates a shared IP group.</span>



<span>Delete a Specified Shared Address Group</span>

<span>DELETE /shared\_ip\_groups/{id}</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Lists details for the specified shared IP group.</span>



<span>Get Current API Limits</span>

<span>GET /limits</span>

<div>

 **<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

Lists current API limits.



<span>Get a URL for a Web Browser-mediated Console Session for a
Specified Server</span>

<span>GET </span><span>/servers/{</span>`id}`<span>/console</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Gets a URL for a web browser-mediated console session for the
specified server.</span>



<span>Rescue/Unrescue a Server</span>

<span>POST </span><span>/servers/{</span>`id}`<span>/rescue</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**



Rescue or unrescue a server.

<span>Create a Next Generation Cloud Servers Image from a First
Generation Cloud Server that is Specified in the Request Body</span>

<span>POST </span><span>/next\_gen\_image\_requests</span>

<div>



</div>

**<span>![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png){width="41"
height="39"}</span>**

<span>Creates a Next Generation Cloud Servers image from a First
Generation Cloud Server that is specified in the request body.</span>




-

[](){#terminology}First Generation Cloud Servers terminology
------------------------------------------------------------

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



[&lt; Permission Matrices for RBAC](/howto/article/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



