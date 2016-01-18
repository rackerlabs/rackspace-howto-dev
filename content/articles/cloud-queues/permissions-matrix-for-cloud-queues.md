---
node_id: 3650
title: Permissions Matrix for Cloud Queues
type: article
created_date: '2013-08-19'
created_by: Renee Rendon
last_modified_date: '2016-01-05'
last_modified_by: Mike Asthalter
product: Cloud Queues
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Queues. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://developer.rackspace.com/docs/)**

**[Related Knowledge Center
Articles](/how-to/)**

**[Cloud Queues Terminology](#queues)**

**<span>As of October 4, 2013</span>**

CAPABILITY

ROLE

DESCRIPTION

Method Name

API Action

Observer

Creator

Admin



### HOME DOCUMENT

<span>Get Home Document</span>

<span>GET {version}</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Gets the home document.    </span>

### QUEUES

<span>List Queues</span>

<span>GET/ </span>*{*<span>version}/queues?marker</span>*=string&*<span>limit</span>*=integer&*<span>detailed</span>*=boolean*

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Lists queues.    </span> </span>

<span>Create Queue</span>

<span>PUT/ {version}/queues/{queue\_name}</span>



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Creates a queue.    </span>

<span>Delete Queue</span>

<span>DELETE/ {version}/queues/{queue\_name}</span>





<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Deletes the queue.    </span> </span>

<span>Check Queue Existence</span>

<span>GET/ </span>*{version}/queues/{queue\_name}*

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Verifies whether the specified queue exists.</span>

<span>Set Queue Metadata</span>

<span>PUT/ {version}/queues/{queue\_name}/metadata</span>



 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Sets queue metadata.    </span> </span>

<span>Show Queue Metadata</span>

<span>GET/ {version}/queues/{queue\_name}/metadata</span>

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Returns queue metadata.    </span> </span>

<span>Show Queue Stats</span>

<span>GET/ {version}/queues/{queue\_name}/stats</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Returns queue statistics.    </span> </span>

### MESSAGES

<span>Post Messages</span>

<span>POST/ {version}/queues/{queue\_name}/messages</span>



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Posts the message or messages for the specified queue.    </span>

<span>Get Messages</span>

<span>GET/
{version}/queues/{queue\_name}/messages?marker=</span>*string*<span>&limit=</span>*integer*
<span>&echo+</span>*=boolean*<span>&include\_claimed=</span>*boolean*

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Gets the message or messages in the specified queue.
 </span> </span>

<span>Get Messages by ID</span>

<span>GET/
{version}/queues/{queue\_name}/messages/{messageId}?claim\_id=</span>*string*

 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span><span>Gets the specified set of messages from the specified
queue.</span>  </span><span>   </span> </span>

<span>Bulk-delete Messages by ID</span>

<span>DELETE /{version}/queues/{queue\_name}/messages ?id</span><span
class="s1">s</span><span>=</span>*string*



 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Bulk-deletes for messages.</span>

<span>Show Message Details</span>

<span>GET/
{version}/queues/{queue\_name}/messages?ids=</span>*string*<span>&claim\_id=</span>*string*

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Shows details for the specified message from the specified
queue.</span>

<span>Delete Message</span>

<span>DELETE/
{version}/queues/{queue\_name}/messages?claim\_id=</span>*string*



 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Deletes the specified message from the specified queue.</span>

### CLAIMS

<span>Claim Messages</span>

<span>POST/ {version}/queues/{queue\_name}/claim?limit=</span>*integer*



<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Claims a set of messages from the specified queue.
 </span> </span>

<span>Query Claim</span>

<span>GET/ {version}/queues/{queue\_name}/claims/{claimId}</span>

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span>Queries the specified claim for the specified queue.    </span>

<span>Update Claim</span>

<span>PATCH/ {version}/queues/{queue\_name}/claims/{claimId}</span>



 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Updates the specified claim for the specified queue.
 </span> </span>

<span>Release Claim</span>

<span>DELETE/ {version}/queues/{queue\_name}/claims/{claimId}</span>



 <img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<img src="/knowledge_center/sites/default/files/field/image/green%20checkmark_1.png" alt="check" width="41" height="39" />

<span><span>Releases the specified claim for the specified queue.
 </span> </span>


-

<a href="" id="queues"></a>Cloud Queues Terminology
---------------------------------------------------

### Message

<span>A message is a task, a notification, or any meaningful data that
gets posted to the queue. A message exists until it is deleted by a
recipient or automatically by the system based on a TTL (time-to-live)
value.</span>

### <span>Queue</span>

<span>A queue holds messages. Ideally, a queue is created per work type.
For example, if you want to compress files, you would create a queue
dedicated to this job. Any application that reads from this queue would
only compress files.</span>

### <span> </span>

[&lt; Permission Matrices for RBAC](/how-to/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



