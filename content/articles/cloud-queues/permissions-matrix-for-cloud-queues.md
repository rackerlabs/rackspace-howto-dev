---
node_id: 3650
title: Permissions Matrix for Cloud Queues
type: article
created_date: '2013-08-19 20:46:52'
created_by: renee.rendon
last_modified_date: '2016-01-05 21:1907'
last_modified_by: Mike Asthalter
product: Cloud Queues
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Queues. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.  

**[API Documentation](http://developer.rackspace.com/docs/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud Queues Terminology](#queues)**

**As of October 4, 2013**

CAPABILITY

ROLE

DESCRIPTION 

Method Name

API Action

Observer

Creator

Admin

 

### HOME DOCUMENT

Get Home Document

GET {version}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Gets the home document.    

### QUEUES

List Queues

GET/ *{*version}/queues?marker*=string&*limit*=integer&*detailed*=boolean*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Lists queues.     

Create Queue

PUT/ {version}/queues/{queue\_name}

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Creates a queue.     

Delete Queue

DELETE/ {version}/queues/{queue\_name}

 

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes the queue.     

Check Queue Existence

GET/ *{version}/queues/{queue\_name}*

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Verifies whether the specified queue exists.

Set Queue Metadata

PUT/ {version}/queues/{queue\_name}/metadata

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Sets queue metadata.     

Show Queue Metadata

GET/ {version}/queues/{queue\_name}/metadata

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Returns queue metadata.     

Show Queue Stats

GET/ {version}/queues/{queue\_name}/stats

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Returns queue statistics.     

### MESSAGES

Post Messages

POST/ {version}/queues/{queue\_name}/messages

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Posts the message or messages for the specified queue.    

Get Messages

GET/
{version}/queues/{queue\_name}/messages?marker=*string*&limit=*integer*<br>
 &echo+*=boolean*&include\_claimed=*boolean*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Gets the message or messages in the specified queue.     

Get Messages by ID

GET/
{version}/queues/{queue\_name}/messages/{messageId}?claim\_id=*string*

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Gets the specified set of messages from the specified queue.      

Bulk-delete Messages by ID

DELETE /{version}/queues/{queue\_name}/messages ?ids=*string*

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Bulk-deletes for messages.

Show Message Details

GET/
{version}/queues/{queue\_name}/messages?ids=*string*&claim\_id=*string*

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Shows details for the specified message from the specified queue.

Delete Message

DELETE/ {version}/queues/{queue\_name}/messages?claim\_id=*string*

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Deletes the specified message from the specified queue.

### CLAIMS

Claim Messages

POST/ {version}/queues/{queue\_name}/claim?limit=*integer*

 

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Claims a set of messages from the specified queue.     

Query Claim

GET/ {version}/queues/{queue\_name}/claims/{claimId}

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Queries the specified claim for the specified queue.     

Update Claim

PATCH/ {version}/queues/{queue\_name}/claims/{claimId}

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Updates the specified claim for the specified queue.     

Release Claim

DELETE/ {version}/queues/{queue\_name}/claims/{claimId}

 

 ![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

![check](/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png)

Releases the specified claim for the specified queue.     

 
-

Cloud Queues Terminology
------------------------

### Message

A message is a task, a notification, or any meaningful data that gets
posted to the queue. A message exists until it is deleted by a recipient
or automatically by the system based on a TTL (time-to-live) value.

### Queue

A queue holds messages. Ideally, a queue is created per work type. For
example, if you want to compress files, you would create a queue
dedicated to this job. Any application that reads from this queue would
only compress files.

###  

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

