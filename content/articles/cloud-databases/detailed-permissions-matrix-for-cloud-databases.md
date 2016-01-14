---
node_id: 3391
title: Permissions matrix for Cloud Databases
type: article
created_date: '2013-04-10 16:06:40'
created_by: renee.rendon
last_modified_date: '2016-01-11 20:4513'
last_modified_by: stephanie.fillmon
product: Cloud Databases
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Databases. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](http://www.rackspace.com/knowledge_center/cloud-hosting)**

**[Cloud Databases Terminology](#Cloud%20Databases%20Terminology)**

### **Updated July 1, 2015**

CAPABILITY

ROLE

DESCRIPTION 

Method name

API action

Observer

Creator

Admin

 

### VERSIONS

List versions

GET /

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists information about all versions of the API.

List version details

GET /{version}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Returns detailed information about the specified version of the API.

### DATABASE INSTANCES

Create a database instance

POST /instances

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a new database instance.

List all database instances

GET /instances

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the status and information for all database instances.

Update a database instance

PUT /instances/{instanceId} 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Associates a specified database instance with the configuration group. 

List database instance status and details

GET /instances/{instanceId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists status and details for the specified database instance.

Delete a database instance

DELETE /instances/{instanceId}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes the specified database instance.

Get the default configuration

GET /instances/{instanceId}/configuration

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the default MySQL configuration settings from the template that
were applied to the specified instance.

Enable the root user

POST /instances/{instanceId}/root

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Enables the root user for the specified database instance and returns
the root password.

List root-enabled status

GET /instances/{instanceId}/root

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Returns true if the root user is enabled for the specified database
instance or false otherwise.

### DATABASE INSTANCE ACTIONS

Restart an instance

POST /instances/{instanceId}/action

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Restarts the database service on the specified instance.

Resize an instance

POST /instances/{instanceId}/action

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Resizes the memory of the specified instance.

Resize the instance volume

POST /instances/{instanceId}/action

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Resizes the volume attached to the instance.

### DATABASES

Create a database

POST /instances/{instanceId}/databases

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a new database within the specified instance.

List databases for an instance

GET /instances/{instanceId}/databases

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists databases for the specified instance.

Delete a database

DELETE /instances/{instanceId}/databases/{databaseName}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes the specified database.

### USERS

Create  a user

POST /instances/{instanceId}/users

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a user for the specified database instance.

List users a in database instance

GET /instances/{instanceId}/users

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the users in the specified database instance.

List a user

GET /instances/{instanceId}/users/{name}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the specified user's name and a list of databases that the user
can access.

List user access

GET /instances/{instanceId}/users/{name}/databases

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists user access for the specified database instance.

Grant user access

PUT /instances/{instanceId}/users/{name}/databases

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Grants access for the specified user to one or more databases for the
specified instance.

Delete user access

DELETE /instances/{instanceId}/users/{name}/databases/{database}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Removes access to the specified database for the specified user.

Delete a user

DELETE /instances/{instanceId}/users/{name}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes the specified user from the specified database instance.

Change user passwords

PUT /instances/{instanceId}/users

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Changes the user passwords for the specified database instance.

Modify user attributes

PUT /instances/{instanceId}/users/{name}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Modifies one or more of the following values for the specified user:
name, password, or the host from which the user is allowed to connect to
the database.

### FLAVORS

List flavors

GET /flavors

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists information for all available flavors.

List flavors by ID

GET /flavors/{flavorId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists information about the specified flavor.

List flavors for the datastore version

GET /datastores/{datastoreType}/versions/{versionId}/flavors

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists flavors for a datastore version.

### ON DEMAND BACKUPS

**Note**: Any user calling the on demand backup operations for Cloud
Databases must have access to Cloud Files.

Create a backup

POST /backups

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a new backup for a database instance.

Delete a backup

DELETE /backups/{backupId}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes the specified backup.

List backups

GET /backups

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all backups for all database instances.

List backup by ID

GET /backups/{backupId}

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists details about the specified backup.

List backups for instance

GET /instance/{instanceId}/backups

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all backups for the specified instance.

Restore a backup

POST /instances

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a new database instance from a backup.

### SCHEDULED BACKUPS

**Note**: Any user calling the scheduled backup operations for Cloud
Databases must have access to Cloud Files.

Create scheduled backup

POST /{version}/{accountId}/schedules

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a schedule for running a backup periodically.

List scheduled backups

GET /{version}/{accountId}/schedules

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all scheduled backups for all database instances for an account.

List the schedule for running a backup 

GET /{version}/{accountId}/schedules/{scheduleId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the specified schedule for running a backup.

Delete the schedule for running a backup

DELETE /{version}/{accountId}/schedules/{scheduleId}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes the specified schedule for running a backup.

### REPLICATION

Create a replica

**Note**: Because the process of creating a replica creates a
backup, the<br>
 user calling the Create replica operation must have access to Cloud
Files.

POST /instances

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a replica of the source instance.

List all replicas and replica source database instances

GET /instances

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the status and information for all replicas or replica sources.

List a replica source

GET /instances{instanceId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists status and details for the specified replica source instance.

List replica details

GET /instances{instanceId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists status and details for the specified replica.

Detach a replica

PATCH /instances{instanceId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Detaches the specified replica instance from its replication source
instance.

List replicas for a source instance

GET /{version}/{accountId}/instances/{instanceId}/replicas

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists replicas for the specified source instance.

### HIGH AVAILABILITY

Create an HA database instance

POST /{version}/{accountId}/ha

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a new HA instance.

List all HA database instances

GET /{version}/{accountId}/ha

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all the HA database instances.

List HA database instance details

GET /{version}/{accountId}/ha/{haId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists details for a specified HA instance.

Delete an HA database instance

DELETE /{version}/{accountId}/ha/{haId}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes an HA database instance.

Add HCLs to an HA database instance

POST /{version}/{accountId}/ha/{haId}/acls

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Adds access control lists (ACLs) to an HA instance.

List ACLs for an HA instance

GET /{version}/{accountId}/ha/{haId}/acls

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists ACLs for an HA instance.

Delete ACLs from an HA instance

DELETE /{version}/{accountId}/ha/{haId}/acls/{address}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes ACLs from an HA instance.

Add Replica to an HA instance

POST /{version}/{accountId}/ha/{haId}/action

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Adds a replica node to the HA group specified by {ha\_id}.

### CONFIGURATIONS

List configurations

GET /configurations

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all defined configuration groups for the tenant.

Create a configuration

POST /configurations

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Creates a new configuration group.

List configuration details

GET / configurations/{configId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists details for the specified configuration group*.*

Update some configuration parameters

PATCH / configurations/{configId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Updates some of the configuration parameters associated with the
specified configuration group.

Replace all configuration parameters

PUT /configurations/{configId}

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Replaces all the configuration parameters associated with the
specified configuration group.

Delete configuration group

*DELETE /*configurations/{configId}

 

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Deletes the specified configuration group.

List instances for a configuration

GET / configurations/{configId}/instances

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists instances that are associated with the specified configuration
group.

### CONFIGURATION PARAMETERS

List configuration parameters

GET /datastores/{datastoreId}/versions/{versionId}/parameters

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists configuration parameters that might be configured on the system.

List configuration parameter details 

GET
/datastores/{datastoreId}/versions/{versionId}/parameters/{parameterId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the details of a specified configuration parameter that might be
configured on the system.

List configuration parameters without datastore

GET /datastores/versions/{versionId}/parameters

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the configuration parameters that might be configured on the
system without specifying a datastore.

List configuration parameter details without datastore 

GET /datastores/versions/{versionId}/parameters/{parameterId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the details of a specified configuration parameter that might be
configured on the system without specifying a datastore.

List verbose default configuration parameters

GET /datastore/version/{versionId}/configuration/{flavorId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the default configuration parameters for a datastore version
flavor without specifying a datastore.

### DATASTORE TYPES AND VERSIONS

List all datastore types

GET /datastores

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all datastore types.

List all datastore types for a datastore

GET /datastores/{datastoreId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all datastore types for the specified datastore.

List all datastore versions for a datastore

GET /datastores/{datastoreId}/versions

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists all versions for the specified datastore.

List a version for a datastore.

GET /datastores/{datastoreId}/versions/{versionId}

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_3.png)

Lists the specified datastore version for the specified datastore.

 
-

Cloud Databases terminology
---------------------------

The following terms are used to describe Cloud Databases.

### Database

A MySQL database within a database instance.

### Database instance

An isolated MySQL instance in a single-tenant environment on a shared
host server. 

### Flavor

An available hardware configuration for a database instance. Each flavor
has a unique combination of memory capacity and priority for CPU time.

### Volume

User-specified storage that contains the MySQL data directory. Volumes
are automatically provisioned on shared Internet Small Computers System
Interface (iSCSI) storage area networks (SAN) that provide increased
performance, scalability, availability, and manageability. 

 

[\< Permission Matrixes for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

