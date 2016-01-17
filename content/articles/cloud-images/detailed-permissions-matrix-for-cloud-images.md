---
node_id: 3741
title: Detailed Permissions Matrix for Cloud Images
type: article
created_date: '2013-10-28'
created_by: Renee Rendon
last_modified_date: '2016-01-11'
last_modified_by: Stephanie Fillmon
product: Cloud Images
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Images. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](https://developer.rackspace.com/docs/)**

[**Cloud Images Terminology**](#images)

### As of January 20, 2014

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

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Lists public virtual machine (VM) images.

Get an Image

GET /v2/images/{image\_id}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Gets the details for the specified image.

Update an Image

PATCH /v2/images/{image\_id}





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Updates the specified image.



Delete an Image

DELETE /v2/images/{image\_id}





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Deletes the specified image.



### Image Sharing Operations

Create Image Member

POST /v2/images/{image\_id}/members



 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Adds the specified tenant ID as an image member (user).



List Image Members

GET /v2/images/{image\_id}/members



 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Returns a collection of members (user) with whom the image has been
shared.



Show Image Member

GET /v2/images/{image\_id}/members/{member\_id}



 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}



Gets details for a specified image member.



Update Member Status

PUT /v2/images/{image\_id}/members/{member\_id}





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Sets the specified status for the specified member (user) of the
specified image.



Delete Image Member



DELETE /v2/images/{image\_id}/members/{member\_id}





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}



Deletes the specified tenant ID from the member list of the specified
image.



### Image Tag Operations

Add an Image Tag

PUT /v2/images/{image\_id}/tags/{tag}





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Adds the specified tag to the specified image.



Delete an Image Tag

DELETE /v2/images/{image\_id}/tags/{tag}





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Deletes the specified tag from the specified image.



### Image Schema Operations

Get Images Schema

GET /v2/schemas/images

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}



Gets a json-schema document that represents an images entity, which is a
container of image entities.



Get Image Schema

GET /v2/schemas/image

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Gets a json-schema document that represents a single image entity.



Get Image Members Schema

GET /v2/schemas/members

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Gets a json-schema document that represents an image members entity.



Get Task Schema

GET /v2/schemas/task

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Gets a json-schema document that represents a specified task entity.



Get Tasks Schema

GET /v2/schemas/tasks

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Gets a json-schema document that represents a tasks entity.



### Image Task Operations

List Tasks

GET /v2/tasks

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Returns a collection of tasks.



Create a Task

POST /v2/tasks





![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Creates a task.



Get a Task

GET /v2/tasks/{task\_id}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png){width="41"
height="39"}

Gets the details for a specified task.




-

[](){#images}Cloud Images Terminology
-------------------------------------

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



[&lt; Permissions Matrices for RBAC](/howto/permissions-matrix-for-role-based-access-control-rbac)
---------------------------------------------------------------------------------------------------------------------------------------------



###

** **

** **



