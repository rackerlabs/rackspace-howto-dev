---
node_id: 3741
title: Detailed Permissions Matrix for Cloud Images
permalink: article/detailed-permissions-matrix-for-cloud-images
type: article
created_date: '2013-10-28 16:29:35'
created_by: renee.rendon
last_modified_date: '2014-02-19 17:4706'
last_modified_by: renee.rendon
products: Cloud Hosting
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Images. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.  

**[API Documentation](http://docs.rackspace.com/)**

[**Cloud Images Terminology**](#images)

### As of January 20, 2014  {style="line-height: 1.4em; color: #333333; font-family: arial; font-size: 12.727272033691406px; font-weight: normal;"}

CAPABILITY

ROLE

Description

Method Name

API Call

Observer

Creator

Admin

 

### Image Operations

List All Images

GET /v2/images

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists public virtual machine (VM) images.    

Get an Image

GET /v2/images/{image\_id}   

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Gets the details for the specified image.    

Update an Image

PATCH /v2/images/{image\_id}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Updates the specified image.    

 

Delete an Image

DELETE /v2/images/{image\_id}   

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Deletes the specified image.    

 

### Image Sharing Operations

Create Image Member

POST /v2/images/{image\_id}/members 

 

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Adds the specified tenant ID as an image member (user). 

 

List Image Members

GET /v2/images/{image\_id}/members

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns a collection of members (user) with whom the image has been
shared. 

 

Show Image Member

GET /v2/images/{image\_id}/members/{member\_id}

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 

Gets details for a specified image member.

 

Update Member Status

PUT /v2/images/{image\_id}/members/{member\_id}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Sets the specified status for the specified member (user) of the
specified image. 

 

Delete Image Member

 

DELETE /v2/images/{image\_id}/members/{member\_id}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 

Deletes the specified tenant ID from the member list of the specified
image. 

 

### Image Tag Operations

Add an Image Tag

PUT /v2/images/{image\_id}/tags/{tag}   

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Adds the specified tag to the specified image.    

 

Delete an Image Tag

DELETE /v2/images/{image\_id}/tags/{tag}   

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Deletes the specified tag from the specified image.    

 

### Image Schema Operations

Get Images Schema

GET /v2/schemas/images

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 

Gets a json-schema document that represents an images entity, which is a
container of image entities. 

 

Get Image Schema

GET /v2/schemas/image

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Gets a json-schema document that represents a single image entity. 

 

Get Image Members Schema 

GET /v2/schemas/members 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Gets a json-schema document that represents an image members entity. 

 

Get Task Schema

GET /v2/schemas/task

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Gets a json-schema document that represents a specified task entity. 

 

Get Tasks Schema

GET /v2/schemas/tasks

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Gets a json-schema document that represents a tasks entity. 

 

### Image Task Operations

List Tasks

GET /v2/tasks

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Returns a collection of tasks.

 

Create a Task

POST /v2/tasks

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Creates a task. 

 

Get a Task

GET /v2/tasks/{task\_id}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Gets the details for a specified task. 

 

 
-

Cloud Images Terminology
------------------------

### Image 

An image is represented by a JSON-encoded data structure (the image
scheme) and its raw binary data (the image file). 

### Image Member

A user who has been granted access to an image.

### Image Schema   

A json document representing metadata about an image.    

### Image Tag

An image tag is a string of characters used to identify a specific
image.

### JSON (Javascript Object Notation)

An open standard format that uses human-readable text to transmit data
objects consisting of key:value pairs. 

   

[\< Permissions Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac) {style="color: #514c4c; font-size: 18px; margin-top: 0px; margin-bottom: 0px; font-family: arial; line-height: normal;"}
-------------------------------------------------------------------------------------------------------------------------------------------

 

###  

** **

** **



