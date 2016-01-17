---
node_id: 3722
title: Detailed permissions matrix for Cloud Backup
type: article
created_date: '2013-10-07'
created_by: Renee Rendon
last_modified_date: '2016-01-11'
last_modified_by: Rose Coste
product: Cloud Backup
body_format: tinymce
---

The following permissions tables display specific permissions for the
roles in Cloud Backup. The tables display the method names, their
corresponding RESTful API commands, and the roles that are supported. To
read more about the API commands, see the [Cloud Backup API Developer's
Guide](https://developer.rackspace.com/docs/cloud-backup/v1/developer-guide/).

-   [Role permissions for Cloud Backup v1](#v1)
-   [Role permissions for Cloud Backup v2](#v2)



[](){#v1}Role permissions for Cloud Backup v1
---------------------------------------------

Capability

Role

Description

Method

API command

Observer

Creator

Admin



Agents

Get agent details

GET /agent/{machineAgentId}

 x

 x

 x

<span>Gets details about the specified server and its agent.</span>

Enable or disable agent

POST /agent/enable



 x

x

<span>Enables or disables an agent. Disabling an agent only stops it
from making backups. The agent is not deleted and its data remains.
Disabled agents can later be re-enabled.</span>

Enable volume encryption

POST /agent/encrypt



 x

x

<span>Enables volume encryption.</span>

Delete agent

POST /agent/delete





 x

Permanently and immediately deletes an agent and its backup data.

Migrate a vault

PUT /agent/migratevault





 x

<span>Migrates a backup vault from one agent to another. These two
agents should be under the same user and their backups should not be
encrypted.</span>

Update agent backup behavior

POST agent/{machineAgentId}



 x

x

<span>Updates the backup data center or enables or disables ServiceNet
for the Cloud Backup agent. If ServiceNet is enabled, the Cloud Backup
agent connects with Cloud Files over ServiceNet and does not incur any
bandwidth charges.</span>

Get agent details by host server ID

GET /agent/server/{hostServerId}

 x

 x

 x

<span>Gets details about the server and its agent by using the specified
host server ID.</span>

User

Method

API command

Observer

Creator

Admin



Get all agents for this user

GET /user/agents

x

x

x

<span>Retrieves information for all of the agents for the current
user.</span>

Wake up agents

GET /user/wakeupagents

x

x

x

<span>Activates the agent before any tasks are performed.</span>

Backup configurations

Method

API command

Observer

Creator

Admin



Create backup configuration

POST /backup-configuration



 x

x

Creates a backup configuration for the authenticated user. and returns
the details of the configuration.

Update backup configuration

PUT /backup-configuration/{backupConfigurationId}



 x

 x

Updates a backup configuration that already exists.

Get backup configuration details

GET /backup-configuration/<span>{backupConfigurationId}</span>

 x

 x

 x

<span>Gets detailed information for the specified backup
configuration.</span>

Get all backup configurations for user

GET /backup-configuration

 x

 x

x

Gets a list of all the backup configurations for the current user.

Get all backup configurations for agent

GET /backup-configuration/system/{machineAgentId}

 x

 x

 x

Gets a list of backup configurations for the specified agent.

Enable or disable a backup configuration

POST /backup-configuration/enable/{backupConfigurationId}



 x

 x

Enables or disables a backup configuration. Disabling a backup
configuration does not delete it nor its data. Disabled backup
configurations can later be re-enabled.

Delete backup configuration

DELETE /backup-configuration/{backupConfigurationId}





 x

Deletes the specified backup configuration.

Backups

Method

API command

Observer

Creator

Admin



Start or stop a backup manually

POST /backup/action-requested



 x

 x

Starts or stops a backup. and returns the  identifier of the instance of
the backup.

Get backup details

GET /backup/{backupId}

 x

x

 x

Gets details about the specified backup.

Get completed backups

GET /backup/completed/{backupConfigurationId}

 x

 x

 x

Gets details for backups that can still be restored. Backups are
returned only for the specified backup configuration.

Get a backup report

GET/backup/report/{backupId}

 x

x

x

Gets details about the specified  completed backup.

Restore configuration operations

Method

API command

Observer

Creator

Admin



Creates a restore configuration

PUT /restore



x

x

Creates a new restore configuration.

Update a restore configuration

POST /restore



x

x

Updates an existing restore configuration.

Include or exclude a file to a restore configuration

PUT /restore/files



x

x

Creates a restore file associated with a restore configuration.

List included or excluded restore configuration files

GET /restore/files/{restoreId}

 x

x

x

Lists the files that are included or excluded in a restore
configuration.

Delete a restore configuration file

DELETE /restore/files/{restoreFileID}



x

x

Deletes a restore configuration file.

Restore

Method

API command

Observer

Creator

Admin



List available backups for restore

GET /backup/availableforrestore

 x

 x

x

Lists the backups that are eligible for restore. An eligible backup is
one that has completed at least once, has not been deleted, and is not
expired.

Start or stop a restore manually

POST /restore/action-requested



 x

 x

Manually starts or stops a restore.

Get detailed information about a restore

GET /restore/{restoreId}

 x

x

x

Gets details about the specified restore.

Get a restore report

GET /restore/report/{restoreId}

 x

 x

 x

Gets a report for the specified completed restore.

Activity operations

Method

API command

Observer

Creator

Admin



Get an activity feed for an agent

GET /system/activity/{agentId}

x

 x

x

Lists all in-progress and completed activity for an agent. Activity
types are Backup, Cleanup, and Restore.

Get activity feed for the user

GET /activity

 x

 x

x

Gets a listing of all activity completed or in progress for the user.



[](){#v2}Role permissions for Cloud Backup v2
---------------------------------------------

Capability

Role

Method

API command

Observer

Creator

Administrator

Agents

Register an agent

POST /v2/agents



x

x

List agents for project

GET /v2/agents{?host\_machine\_id}

x

x

x

Get agent details

GET /v2/agents/{agent\_id}

x

x

x

Update agent

PATCH /v2/agents/{agent\_id}



x

x

Delete agent

DELETE /v2/agents/{agent\_id}





x

Get activity feed for an agent

GET /v2/agents/{id}activites {?marker, limit, sort\_dir, type, state,
agent\_ids, configuration\_ids}

x

x

x

Request to browse an agent's files

POST /v2/agents/{agent\_id}/browse-requests



x

x

View results of agent browse request

GET /v2/agents/{agent\_id}/browse-requests/{request\_id}



x

x

Retrieve an agent's configuration

GET /v2/agents/{agent\_id}/configuration

x

x

x

List configurations for an agent

GET /v2/agents/{agent\_id}/configurations

x

x

x

Process agent events

POST /v2/agents/{agent\_id}/events

x

x

x

List events for an agent

GET /v2/agents/{agent\_id}/events{?marker}

x

x

x

Request to download agent's log files

POST /v2/agents/{agent\_id}/logfiles





x

List log files for agent

GET /v2/agents/{agent\_id}logfiles





x

Get details about a log file

GET /v2/agents/{agent\_id}/logfiles/{logfile\_id}





x

Update a log file

PATCH /v2/agents/{agent\_id}/logfiles/{logfile\_id}



x

x

Delete a log file

DELETE /v2/agents/{agent\_id}/logfiles/{logfile\_id}





x

Get agent status

GET /v2/agents/{agent\_id}/status

x

x

x

Migrate a vault

POST /v2/agents/{agent\_id}/vault





x

Enable valut encryption

POST /v2/agents/{agent\_id}/vault-encryption-requests



x

x

Report results of a vault encryption request

POST /v2/agents/{agent\_id}/vault-encryption-requests/{request\_id}



x

x

View results of vault encryption request

GET /v2/agents/{agent\_id}/vault-encryption-requests/{request\_id}



x

x

Request to verify the password for an agent's vault

POST /v2/agents/{agent\_id}/vault-password-verification-requests

x

x

x

Report results of a vault password verification request

POST
/v2/agents/{agent\_id}/vault-password-verification-requests/{request\_id}



x

x

View results of a vault password verification request

GET
/v2/agents/{agent\_id}/vault-password-verification-requests/{request\_id}

x

x

x

Listf OSs supported with the agent

GET /agents/supportedos

x

x

x

**Note:** Agent authentication can be performed only by the Anonymous
user role

Backups

Method

API command

Observer

Creator

Administrator

Start backup

POST /v2/backups



x

x

Get backups

GET /v2/backups{?marker, limit, sort\_dir}

x

x

x

Get backup details

GET /v2/backups/{backup\_id}

x

x

x

Update a backup

PATCH /v2/backups/{backup\_id}



x

x

Request to browse a backup's files

POST /v2/backups/{backup\_id}/browse-requests

x

x

x

View the results of a browse request

GET /v2/backups/{backup\_id}/browse-requests/{request\_id}

x

x

x

Get errors for a backup

GET /v2/backups/{backup\_id}/errors

x

x

x

List events for a backup

GET /v2/backups/{backup\_id}/events{?marker}

x

x

x

Cleanups

Method

API command

Observer

Creator

Administrator

Start a cleanup

POST /v2/cleanups



x

x

View cleanups for a project

GET /v2/cleanups{?marker,limit,sort\_dir}

x

x

x

Get details about a cleanup

GET /v2/cleanups/{cleanup\_id}

x

x

x

Update a cleanup

PATCH /v2/cleanups/{cleanup\_id}



x

x

Get errors for a cleanup

GET /v2/cleanups/{cleanup\_id}/errors

x

x

x

List events for a cleanup

GET /v2/cleanups/events

x

x

x

Configurations

Method

API command

Observer

Creator

Administrator

Create a configuration

POST /v2/configurations



x

x

List configurations

GET /v2/configurations

x

x

x

Get configuration details

GET /v2/configurations/{config\_id}

x

x

x

Update a configuration

PATCH /v2/configurations/{config\_id}



x

x

Delete a configuration

DELETE /v2/configurations/{config\_id}





x

List activities for a configuration

GET /v2/configuration/{config\_id}/activities{?marker, limit, sort\_dir,
state}

x

x

x

List events for a configuration

GET /v2/configurations/{config\_id}/events{?marker}

x

x

x

Events

Method

API command

Observer

Creator

Administrator

List events for a project

GET /v2/events

x

x

x

Process project events

POST /v2/events

x

x

x

Restores

Method

API command

Observer

Creator

Administrator

Start a restore

POST /v2/restores



x

x

List restores for a project

GET /v2/restores{?marker, limit, sort\_dir}

x

x

x

Get details about a restore

GET /v2/restores/{restore\_id}

x

x

x

Update a restore

PATCH /v2/restores/{restore\_id}



x

x

Get errors for a restore

GET /v2/restores/{restore\_id}/errors

x

x

x

List events for a restore

GET /v2/restores/{restore\_id}/events

x

x

x





[&lt; Permission Matrices for RBAC](/howto/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



