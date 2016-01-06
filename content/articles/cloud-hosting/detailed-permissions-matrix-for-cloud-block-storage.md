---
node_id: 3394
title: Permissions Matrix for Cloud Block Storage
permalink: article/detailed-permissions-matrix-for-cloud-block-storage
type: article
created_date: '2013-04-10 16:20:08'
created_by: renee.rendon
last_modified_date: '2014-02-07 15:4237'
last_modified_by: renee.rendon
products: Cloud Hosting
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Block Storage. The matrix displays the method names,
their corresponding RESTful API commands, and the roles that are
supported.  

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud Block Storage Terminology](#blockstorage)**

### As of February 7, 2013 {style="line-height: 1.4em; color: #333333; font-family: arial; font-size: 12.727272033691406px; font-weight: normal;"}

CAPABILITY

ROLE

Description

Method Name

API Call

Observer

Creator

Admin

 

### VOLUMES

Create Volume

POST /volumes

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Creates the volume. 

 

List Volumes

GET /volumes

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists summary information for all block storage volumes that the tenant
who submits the request can access.

 

List Volumes (Detailed)

GET /volumes/detail

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists detailed information for all Block Storage volumes that the tenant
who submits the request can access.

 

Show Volume

GET /volumes/{volume\_id}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

View all information about a single volume.

 

Rename Volume

PUT /volumes/{volume\_id}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Updates a volume's display name and display description.

 

Delete Volume

DELETE /volumes/{volume\_id}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Deletes a single volume. 

 

### VOLUME TYPES

List Volume Types

GET /types

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Requests a list of volume types. 

 

Describe Volume Type

GET /types/{volume\_type\_id}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Requests a single volume type. 

 

### SNAPSHOTS

Create Snapshot

POST /snapshots

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Creates a snapshot. 

 

List Snapshots

GET /snapshots

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists summary information for all Block Storage snapshots that the
tenant who submits the request can access.

 

List Snapshots (Detailed)

GET /snapshots/detail

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Lists detailed information for all Block Storage snapshots that the
tenant who submits the request can access.

 

Show Snapshot

GET /snapshots/{snapshot\_id}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

View all information about a single snapshot.

 

Delete Snapshot

DELETE /snapshots/{snapshot\_id}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_7.png)

Deletes a single snapshot. 

 

 
-

Cloud Block Storage Terminology
-------------------------------

### Snapshot

A point-in-time copy of the data contained in a volume.

### Volume

A detachable block storage device. You can think of it as a USB hard
drive. It can onlt be attached to one instance at a time.

### Volume Type

The type of a block storage volume. There are two types: SATA for
standard performance and SSD for high performance.

[\< Permissions Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
-------------------------------------------------------------------------------------------------------------------------------------------

** **

** **



