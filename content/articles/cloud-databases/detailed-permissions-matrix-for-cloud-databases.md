---
node_id: 3391
title: Permissions matrix for Cloud Databases
type: article
created_date: '2013-04-10'
created_by: Renee Rendon
last_modified_date: '2016-01-11'
last_modified_by: Stephanie Fillmon
product: Cloud Databases
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Databases. The matrix displays the method names, their
corresponding RESTful API commands, and the roles that are supported.

**[API Documentation](http://docs.rackspace.com/)**

**[Related Knowledge Center
Articles](/howto/)**

**[Cloud Databases Terminology](#Cloud%20Databases%20Terminology)**

### <span>**Updated July 1, 2015**</span>

CAPABILITY

ROLE

DESCRIPTION

Method name

API action

Observer

Creator

Admin



### VERSIONS

<span>List versions</span>

GET /

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists information about all versions of the API.</span>

<span>List version details</span>

GET /{version}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Returns detailed information about the specified version of the
API.</span>

### DATABASE INSTANCES

<span>Create a database instance</span>

<span>POST /instances</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a new database instance.</span>

<span>List all database instances</span>

<span>GET /instances</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the status and information for all database
instances.</span>

<span>Update a database instance</span>

PUT /instances/{instanceId}



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Associates a specified database instance with the configuration group.

<span>List database instance status and details</span>

<span>GET /instances/{instanceId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists status and details for the specified database
instance.</span>

<span>Delete a database instance</span>

<span>DELETE /instances/{instanceId}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes the specified database instance.</span>

<span>Get the default configuration</span>

<span>GET /instances/{instanceId}/configuration</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists the default MySQL configuration settings from the template that
were applied to the specified instance.

<span>Enable the root user</span>

<span>POST /instances/{instanceId}/root</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Enables the root user for the specified database instance and
returns the root password.</span>

<span>List root-enabled status</span>

<span>GET /instances/{instanceId}/root</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Returns true if the root user is enabled for the specified
database instance or false otherwise.</span>

### DATABASE INSTANCE ACTIONS

<span>Restart an instance</span>

<span>POST /instances/{instanceId}/action</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Restarts the database service on the specified instance.</span>

<span>Resize an instance</span>

<span>POST /instances/{instanceId}/action</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Resizes the memory of the specified instance.</span>

<span>Resize the instance volume</span>

<span>POST /instances/{instanceId}/action</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Resizes the volume attached to the instance.</span>

### DATABASES

<span>Create a database</span>

<span>POST /instances/{instanceId}/databases</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Creates a new database <span>within the specified instance.</span>

<span>List databases for an instance</span>

<span>GET /instances/{instanceId}/databases</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists databases for the specified instance.</span>

<span>Delete a database</span>

<span>DELETE /instances/{instanceId}/databases/{databaseName}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes the specified database.</span>

### USERS

<span>Create  a user</span>

<span>POST /instances/{instanceId}/users</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a user for the specified database instance.</span>

<span>List users a in database instance</span>

<span>GET /instances/{instanceId}/users</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the users in the specified database instance.</span>

<span>List a user</span>

<span>GET /instances/{instanceId}/users/{name}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the specified user's name and a list of databases that the
user can access.</span>

List user access

<span>GET /instances/{instanceId}/users/{name}/databases</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists user access for the specified database instance.

Grant user access

<span>PUT /instances/{instanceId}/users/{name}/databases</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Grants access for the specified user to one or more databases for
the specified instance.</span>

Delete user access

<span>DELETE
/instances/{instanceId}/users/{name}/databases/{database}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Removes access to the specified database for the specified
user.</span>

Delete a user

<span>DELETE /instances/{instanceId}/users/{name}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes the specified user from the specified database
instance.</span>

Change user passwords

<span>PUT /instances/{instanceId}/users</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Changes the user passwords for the specified database
instance.</span>

Modify user attributes

<span>PUT /instances/{instanceId}/users/{name}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Modifies one or more of the following values for the specified
user: name, password, or the host from which the user is allowed to
connect to the database.</span>

### FLAVORS

List flavors

<span>GET /flavors</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists information for all available flavors.</span>

List flavors by ID

<span>GET /flavors/{flavorId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists information about the specified flavor.</span>

List flavors for the datastore version

<span>GET
/datastores/{datastoreType}/versions/{versionId}/flavors</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists flavors for a datastore version.</span>

### ON DEMAND BACKUPS

**Note**: Any user calling the on demand backup operations for Cloud
Databases must have access to Cloud Files.

<span>Create a backup</span>

<span>POST /backups</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a new backup for a database instance.</span>

<span>Delete a backup</span>

<span>DELETE </span><span>/backups/{backupId}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes the specified backup.</span>

<span>List backups</span>

<span>GET </span><span>/backups</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all backups for all database instances.</span>

<span>List backup by ID</span>

<span>GET </span><span>/backups/{backupId}</span>

 ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

 ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists details about the specified backup.

<span>List backups for instance</span>

<span>GET /instance/{instanceId}/backups</span>

 ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

 ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all backups for the specified instance.</span>

<span>Restore a backup</span>

<span>POST /instances</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a new database instance from a backup.</span>

### SCHEDULED BACKUPS

**Note**: Any user calling the scheduled backup operations for Cloud
Databases must have access to Cloud Files.

Create scheduled backup

POST <span>/{version}/{accountId}/schedules</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a schedule for running a backup periodically.</span>

List <span>scheduled backups</span>

GET <span>/{version}/{accountId}/schedules</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all scheduled backups for all database instances for an
account.</span>

List the <span>schedule for running a backup </span>

GET <span>/{version}/{accountId}/schedules/{scheduleId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the specified schedule for running a backup.</span>

Delete the <span>schedule for running a backup</span>

DELETE <span>/{version}/{accountId}/schedules/{scheduleId}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes the specified schedule for running a backup.</span>

### REPLICATION

Create a replica

**Note**: Because the process of creating a replica creates a
backup, the
user calling the Create replica operation must have access to Cloud
Files.

POST /instances



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Creates a replica of the source instance.

List all replicas and replica source database instances

<span>GET /</span><span>instances</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists the status and information for all replicas or replica sources.

List a replica source

<span>GET /</span><span>instances{instanceId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists status and details for the specified replica source instance.

List replica details

<span>GET /</span><span>instances{instanceId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists status and details for the specified replica.

Detach a replica

<span>PATCH /</span><span>instances{instanceId}</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Detaches the specified replica instance from its replication source
instance.

List replicas for a source instance

<span>GET
/</span><span>{version}/{accountId}/instances/{instanceId}/replicas</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

Lists replicas for the specified source instance.

### HIGH AVAILABILITY

Create an HA database instance

POST <span>/{version}/{accountId}/ha</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a new HA instance.</span>

List all HA database instances

GET <span>/{version}/{accountId}/ha</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all the HA database instances.</span>

List HA database instance details

GET <span>/{version}/{accountId}/ha/{haId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists details for a specified HA instance.</span>

Delete an HA database instance

DELETE <span>/{version}/{accountId}/ha/{haId}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes an HA database instance.</span>

Add HCLs to an HA database instance

POST <span>/{version}/{accountId}/ha/{haId}/acls</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Adds access control lists (ACLs) to an HA instance.</span>

List ACLs for an HA instance

GET <span>/{version}/{accountId}/ha/{haId}/acls</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists ACLs for an HA instance.</span>

Delete ACLs from an HA instance

DELETE <span>/{version}/{accountId}/ha/{haId}/acls/{address}</span>





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes ACLs from an HA instance.</span>

Add Replica to an HA instance

POST <span>/{version}/{accountId}/ha/{haId}/action</span>



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Adds a replica node to the HA group specified by {ha\_id}.</span>

### CONFIGURATIONS

List configurations

<span>GET /configurations</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all defined configuration groups for the tenant.</span>

Create a configuration

<span>POST /co</span>nfigurations



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Creates a new configuration group.</span>

List configuration details

GET / <span>co</span>nfigurations/{configId}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists details for the specified </span>configuration group*.*

Update some configuration parameters

PATCH / <span>co</span>nfigurations/{configId}



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Updates some of the configuration parameters associated with the
specified </span>configuration group.

Replace all configuration parameters

PUT /<span>co</span>nfigurations/{configId}



![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Replaces all the configuration parameters associated with the
specified </span>configuration group.

Delete configuration group

*DELETE /*<span>co</span>nfigurations/{configId}





![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Deletes the specified </span>configuration group.

List instances for a configuration

GET / <span>co</span>nfigurations/{configId}/instances

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists instances that are associated with the
specified </span>configuration group.

### CONFIGURATION PARAMETERS

List configuration parameters

<span>GET
/datastores/{datastoreId}/versions/{versionId}/parameters</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists configuration parameters that might be configured on the
system.</span>

List configuration parameter details

<span>GET
/datastores/{datastoreId}/versions/{versionId}/parameters/{parameterId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the details of a specified configuration parameter that
might be configured on the system.</span>

List configuration parameters without datastore

<span>GET /datastores/versions/{versionId}/parameters</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the configuration parameters that might be configured on the
system without specifying a datastore.</span>

List configuration parameter details without datastore

<span>GET
/datastores/versions/{versionId}/parameters/</span><span>{parameterId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the details of a specified configuration parameter that
might be configured on the system </span><span>without specifying a
datastore.</span>

List verbose default configuration parameters

<span>GET /datastore/version/{versionId}/configuration/{flavorId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the default configuration parameters for a datastore version
flavor </span><span>without specifying a datastore.</span>

### DATASTORE TYPES AND VERSIONS

<span>List all datastore types</span>

<span>GET /datastores</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all datastore types.</span>

<span>List all datastore types for a datastore</span>

<span>GET /datastores/{datastoreId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all datastore types for the specified datastore.</span>

<span>List all datastore versions for a datastore</span>

<span>GET /datastores/{datastoreId}/versions</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists all versions for the specified datastore.</span>

<span>List a version for a datastore.</span>

<span>GET /datastores/{datastoreId}/versions/{versionId}</span>

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_3.png){width="41"
height="39"}

<span>Lists the specified datastore version for the specified
datastore.</span>


-

[]()Cloud Databases terminology
-------------------------------

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



[&lt; Permission Matrixes for RBAC](/howto/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



