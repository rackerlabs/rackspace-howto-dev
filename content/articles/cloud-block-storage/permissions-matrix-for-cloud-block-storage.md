---
node_id: 3394
title: Permissions Matrix for Cloud Block Storage
type: article
created_date: '2013-04-10'
created_by: Renee Rendon
last_modified_date: '2016-01-15'
last_modified_by: Rose Contreras
product: Cloud Block Storage
product_url: cloud-block-storage
---

The following permissions matrix displays specific permissions for the
roles in Cloud Block Storage. The matrix displays the method names,
their corresponding RESTful API commands, and the roles that are
supported. \[\*\*API Documentation\*\*\](http://docs.rackspace.com/)
\[\*\*Related Knowledge Center
Articles\*\*\](http://www.rackspace.com/knowledge\_center/cloud-hosting)
\[\*\*Cloud Block Storage Terminology\*\*\](\#blockstorage) \#\#\# As of
February 7, 2013 Method | API Action | Role | Description :---: | :---:
| :---: | :---: \*\*VOLUMES\*\* | Create Volume | `POST /volumes` |
\*\*Creator & Admin\*\* | Creates the volume. List Volumes |
`GET /volumes` | \*\*Observer & Creator & Admin\*\* | Lists summary
information for all block storage volumes that the tenant who submits
the request can access. List Volumes (Detailed) | `GET /volumes/detail`
| \*\*Observer & Creator & Admin\*\* | Lists detailed information for
all Block Storage volumes that the tenant who submits the request can
access. Show Volume | `GET /volumes/{volume_id}` | \*\*Observer &
Creator & Admin\*\* | View all information about a single volume. Rename
Volume | `PUT /volumes/{volume_id}` | \*\*Observer & Creator & Admin\*\*
| Updates a volume's display name and display description. Delete Volume
| `DELETE /volumes/{volume_id}` | \*\*Admin only\*\* | Deletes a single
volume. \*\*VOLUME TYPES\*\* | List Volume Types | `GET /types` |
\*\*Observer & Creator & Admin\*\* | Requests a list of volume types.
Describe Volume Type | `GET /types/{volume_type_id}` | \*\*Creator &
Admin\*\* | Requests a single volume type. \*\*SNAPSHOTS\*\* | Create
Snapshot
| `POST /snapshots` | \*\*Creator & Admin\*\* | Creates a snapshot. List
Snapshots | `GET /snapshots` | \*\*Observer & Creator & Admin\*\* |
Lists summary information for all Block Storage snapshots that the
tenant who submits the request can access. List Snapshots (Detailed) |
`GET /snapshots/detail` | \*\*Observer & Creator & Admin\*\* | Lists
detailed information for all Block Storage snapshots that the tenant who
submits the request can access. Show Snapshot |
`GET /snapshots/{snapshot_id}` | View all information about a single
snapshot. Delete Snapshot | `DELETE /snapshots/{snapshot_id}` |
\*\*Admin only\*\* | Deletes a single snapshot.  \#\# Cloud Block
Storage Terminology \#\#\# Snapshot A point-in-time copy of the data
contained in a volume. \#\#\# Volume A detachable block storage device.
You can think of it as a USB hard drive. It can onlt be attached to one
instance at a time. \#\#\# Volume Type The type of a block storage
volume. There are two types: SATA for standard performance and SSD for
high performance. \*\*&lt;\*\* \[\*\*Permissions Matrices for
RBAC\*\*\](http://www.rackspace.com/knowledge\_center/article/permissions-matrix-for-role-based-access-control-rbac)

