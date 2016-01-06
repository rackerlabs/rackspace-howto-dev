---
node_id: 3675
title: Permissions Matrix for Auto Scale
permalink: article/permissions-matrix-for-autoscale
type: article
created_date: '2013-09-04 16:58:35'
created_by: renee.rendon
last_modified_date: '2014-08-23 19:5105'
last_modified_by: rose.contreras
products: Auto Scale
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Auto Scale. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](/knowledge_center/article/rackspace-auto-scale-overview)**

**Auto Scale Terminology**

### **As of November 11, 2013** {style="margin-bottom: 0in; text-align: left;"}

CAPABILITY

ROLE

DESCRIPTION 

Method Name 

API Action

Observer

Admin

 

Create Group

POST/groups/

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Creates an autoscaling group.

List Groups

GET/groups/

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Lists the autoscaling groups available to the specified tenant.

 

List Group Details 

GET /groups/{groupId}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Lists detailed autoscaling group configuration. 

 

Delete Group

DELETE /groups/{groupId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Deletes autoscaling group.

 

Get Group State

GET /groups/{groupId}/state

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Reports autoscaling group state.  

 

Get Group Configuration

GET /groups/{groupId}/config

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 

Lists autoscaling group configuration.

 

Replace Group Configuration

PUT /groups/{groupId}/config

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Updates autoscaling group configuration.

 

Get Launch Configuration 

GET /groups/{groupId}/launch 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Lists launch configuration. 

 

Replace Launch Configuration 

PUT /groups/{groupId}/launch 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Update launch group configuration.  

 

Pause Group Policy Execution 

POST /groups/{groupId}/pause 

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Pauses policy execution.

 

Resume Group Policy Execution

POST /groups/{groupId}/resume

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Resumes policy execution. 

 

Get a List of Policies

GET /groups/{groupId}/policies/ 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Lists scaling policies in the autoscaling group.

 

Get Details of a Policy 

GET /groups/{groupId}/policies/{policyId} 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Describes one policy. 

 

Create a New Policy 

 POST /groups/{groupId}/policies/

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Creates autoscaling policy.

 

Delete a Policy

DELETE /groups/{groupId}/policies/{policyId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Deletes a policy. 

 

Replace a Policy

PUT /groups/{groupId}/policies/{policyId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Updates policy. 

 

Execute a Policy

POST /groups/{groupId}/policies/{policyId}/execute

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Executes a policy. 

 

Get a List of Webhooks

GET /groups/{groupId}/policies/{policyId}/webhook

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Lists webhooks in the autoscaling group. 

 

 Create a Webhook

POST /groups/{groupId}/policies/{policyId}/webhook

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Creates a webhook. 

 

Replace a Webhook

PUT /groups/{groupId}/policies/{policyId}/webhook/{webhookId} 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Updates a webhook. 

 

Delete a Webhook

DELETE /groups/{groupId}/policies/{policyId}/webhook/{webhookId} 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Deletes a webhook.

 

View Webhook Info

GET /groups/{groupId}/policies/{policyId}/webhook/{webhookId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Describes one webhook.

 

 
-

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

