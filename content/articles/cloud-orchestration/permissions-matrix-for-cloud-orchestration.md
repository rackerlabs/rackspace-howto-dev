---
node_id: 3888
title: Permissions Matrix for Cloud Orchestration
type: article
created_date: '2014-02-05 18:21:44'
created_by: renee.rendon
last_modified_date: '2016-01-11 22:2247'
last_modified_by: rose.contreras
product: Cloud Orchestration
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Orchestration. The matrix displays the method names,
their corresponding RESTful API commands, and the roles that are
supported.  

[Cloud Orchestration API v1.0 Developer
Guide](https://developer.rackspace.com/docs/cloud-orchestration/v1/developer-guide/)

[Cloud Orchestration
FAQs](https://www.rackspace.com/knowledge_center/product-faq/cloud-orchestration)

[Cloud Orchestration Terminology](#orchestration)

[Permission Matrices for
RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)

### **As of May, 2015     **

CAPABILITY

ROLE

DESCRIPTION

Method Name

API Action

Observer

Creator

Admin

 

### STACK OPERATIONS

Note: Orchestration users will need access to any products used in their
templates.

Create Stack

POST /stacks

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Creates a stack.

List Stack Data 

GET /stacks

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Lists active stacks.

Find Stack 

GET /stacks/{stack\_name}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Finds the canonical URL for a specified stack.

Get Stack Data

GET /stacks/{stack\_name}/{stack\_id}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Gets data about a specified stack.

Update Stack 

PUT /stacks/{stack\_name}/{stack\_id}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Updates a specified stack.

Delete Stack 

DELETE /stacks/{stack\_name}/{stack\_id}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Deletes a specified stack.

Abandon Stack

DELETE /stacks/{stack\_name}/{stack\_id}/abandon  

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Deletes a given stack (from orchestration system database) but leaves
the stack resources intact.

Adopt Stack

POST /stacks 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

This operation is similar to the Create Stack operation. Along with
stack create parameters, an additional body parameter
'adopt\_stack\_data' must be provided (adopt\_stack\_data type is
String). Data returned by Abandon Stack could be provided as
adopt\_stack\_data.

Preview Stack

POST /stacks/preview

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Previews a stack.

### STACK RESOURCES

Find Stack Resources 

GET /stacks/{stack\_name}/resources

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Finds the canonical URL for the resource list of a specified stack.

List Resources 

GET /stacks/{stack\_name}/{stack\_id}/resources 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Lists resources in a stack.

Get Resource Data

GET /stacks/{stack\_name}/{stack\_id}/resources/{resource\_name}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Gets data for a specified resource.

List Resource Types

GET /resource\_types

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Lists the supported template resource types.

Get Resource Schema

GET /resource\_types/{type\_name}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Gets the interface schema for a specified resource type.

Get Resource Template 

GET /resource\_types/{type\_name}/template

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Gets a template representation for a specified resource type.

### STACK EVENTS

Find Stack Events 

GET /stacks/{stack\_name}/events

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Finds the canonical URL for the event list of a specified stack.

List Stack Events 

GET /stacks/{stack\_name}/{stack\_id}/events

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Lists events for a specified stack.

List Resource Events 

GET /stacks/{stack\_name}/{stack\_id}/resources/{resource\_name}/events

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Lists events for a specified stack resource.

Show Event 

GET /stacks/{stack\_name}/{stack\_id}/resources/events/{event\_id}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Gets data about a specified event.

### TEMPLATES

Get Stack Template 

GET /stacks/{stack\_name}/{stack\_id}/template 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

Gets a template for a specified stack.

### BUILD INFORMATION {.p1}

Get Build Info

GET /build\_info

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_9.png)

 

Gets information about the current heat build.

 
-

Cloud Orchestration Terminology
-------------------------------

**Template**

A Cloud Orchestration template is a portable file, written in a
user-readable language, that describes how a set of resources should be
assembled and what software should be installed in order to produce a
working deployment. The template specifies what resources should be
used, what attributes can be set, and other parameters that are critical
to the successful, repeatable automation of a specific application
deployment.

**Resource**

A resource is a template artifact that represents some component of your
desired architecture (a Nova server, a group of scaled servers, a Cinder
volume, some configuration management system, and so forth).

**Stack**

A stack is a group of resources (servers, load balancers, databases, and
so forth) combined to fulfill a useful purpose. Based on a template,
Heat orchestration engine creates an instantiated set of resources (a
stack) to run the application framework or component specified (in the
template). A stack is a running instance of a template. The result of
creating a stack is a deployment of the application framework or
component.

