---
node_id: 3392
title: Permissions Matrix for Cloud Files
permalink: article/detailed-permissions-matrix-for-cloud-files
type: article
created_date: '2013-04-10 16:10:21'
created_by: renee.rendon
last_modified_date: '2013-09-26 19:4336'
last_modified_by: kyle.laffoon
products: Cloud Files
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Files. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud Files Terminology](#Cloud%20Files%20Terminology)**

### **As of September 26, 2013** {style="margin-bottom: 0in; text-align: left;"}

CAPABILITY

ROLE

DESCRIPTION 

Method Name 

API Action

Observer

Admin

 

Read Account Metadata

HEAD /account

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

View quick metadata on an account.

Write Account Metadata

POST /account

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Write metadata on an account.

 

List Containers

GET /account

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

View a list of containers in an account.

 

Create Container

PUT /account/container

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Create containers, or storage compartments, for your
data.[ ](http://www.rackspace.com/knowledge_center/product-page/cloud-files)

 

Delete Container

DELETE /account/container

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png) 

Permanently remove a container. (The container must be empty before it
can be removed.) 

 

Read Container Metadata

HEAD /account/container

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

 

View quick metadata on a container.

 

Write Container metadata

POST /account/container

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

 Write metadata on a container.

 

List Objects

GET /account/container

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png) 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

View names and details of objects within a container.

 

Read Object

GET /account/container/object

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

 Retrieve the object's data.

 

Create/Update Object

PUT /account/container/object

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Write or overwrite an object's content and metadata. 

 

Copy Object

PUT /account/container/destobject

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Copy an existing object to another object in Cloud Files. (The
destination container must exist before attempting the copy.)

 

Delete Object

DELETE /account/container/object

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Permanently remove an object from the storage system (data and
metadata).

 

Retrieve Object Metadata

HEAD /account/container/object

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Retrieve object metadata and other standard HTTP headers.

 

Update Object Metadata

POST /account/container/object

 

**![](/knowledge_center/sites/default/files/field/image/green%20checkmark_0.png)**

Set your own custom object metadata.

 

 
-

Cloud Files Terminology
-----------------------

### [**Container**](http://www.rackspace.com/knowledge_center/frequently-asked-question/what-is-a-container-in-cloud-files)

A storage compartment for your data that provides a way for you to
organize that data.

### [**Object**](http://www.rackspace.com/knowledge_center/frequently-asked-question/what-is-an-object-in-cloud-files)

The basic storage entity that represents the files that you store in
your Cloud Files account.

 

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

