---
node_id: 4449
title: Cloud Server Configuration options
type: article
created_date: '2014-12-01 18:46:29'
created_by: rose.contreras
last_modified_date: '2015-07-09 22:1012'
last_modified_by: rose.contreras
product: Managed Operations
body_format: full_html
---

undefined&rdquo; directories   |
|                    |                    |                    | are backed up:     |
|                    |                    |                    |                    |
|                    |                    |                    | **For Linux        |
|                    |                    |                    | Managed Cloud      |
|                    |                    |                    | servers:**         |
|                    |                    |                    |                    |
|                    |                    |                    | `/etc           /h |
|                    |                    |                    | ome           /var |
|                    |                    |                    | /www           /va |
|                    |                    |                    | r/lib/mysqlbackup  |
|                    |                    |                    |         `          |
|                    |                    |                    |                    |
|                    |                    |                    | For Windows        |
|                    |                    |                    | Managed Cloud      |
|                    |                    |                    | servers:           |
|                    |                    |                    |                    |
|                    |                    |                    | c:\\ users\        |
|                    |                    |                    | \                  |
|                    |                    |                    |  c:\\ InetPub\     |
|                    |                    |                    | \                  |
+--------------------+--------------------+--------------------+--------------------+
| `monitoring_agent_ | Y                  | Y                  | Installs the Cloud |
| only`              |                    |                    | Monitoring agent.  |
+--------------------+--------------------+--------------------+--------------------+
| `monitoring_defaul | Y                  | Y                  | Installs the Cloud |
| ts`                |                    |                    | Monitoring agent   |
|                    |                    |                    | and configures     |
|                    |                    |                    | default            |
|                    |                    |                    | Monitoring, Disk,  |
|                    |                    |                    | and CPU checks.    |
|                    |                    |                    | For Managed        |
|                    |                    |                    | Operations service |
|                    |                    |                    | level customers,   |
|                    |                    |                    | this option also   |
|                    |                    |                    | configures default |
|                    |                    |                    | file system alerts |
|                    |                    |                    | that are sent to   |
|                    |                    |                    | Rackspace.         |
+--------------------+--------------------+--------------------+--------------------+
| `auto_updates`     | Y                  | Y                  | Enables automatic  |
|                    |                    |                    | updates of server  |
|                    |                    |                    | software.          |
+--------------------+--------------------+--------------------+--------------------+

\

You can combine the `build_config` options. For example:

-   **`monitoring_defaults` + `auto_updates` -**installs the monitoring
    agent configured with Rackspace best practices, and turns on
    automatic updates.\
    \
-   **`backup_agent_only`** installs the Rackspace Cloud Backup agent
    but does not configure Rackspace backups. You must separately
    identify the directories that you want backed up after the agent is
    installed.

Build options for configuration management software (Chef, Puppet, Ansible, and Salt)
-------------------------------------------------------------------------------------

Using the API to build a server with a core option passed does not
conflict with configuration management software. Such builds have a
Rackspace account and nothing more. If you want additional components,
you must pass them with the `build_config` metadata key.

The following example shows the build option for a Chef server
management.

    nova boot --flavor 2 --image [image] --meta build_config=core www.example.com

The following example shows the build option for building a file server
with a Rackspace user name and password only and backup ability.

    nova boot --flavor 2 --image [image] --meta build_config=core,driveclient fileserver.example.com

This following example shows a good option for a customer who wants a
database server that has monitoring and backups available, but no
updates or additional packages.

    nova boot --flavor 2 --image [image] --meta build_config=core,driveclient,monitoring db.example.com

If you use configuration management software, wait for the post-build
configuration to complete before performing your configuration
management. For standard and workload-optimized cloud servers only, you
can obtain the Managed Operations post-build automation status via the
Cloud Servers API. Look for the metadata key value
`informationrax_service_level_automation`. Depending on the current
status of the Managed Cloud post-build automation process, the metadata
key will have one of the following values:

-   Pending
-   In Progress
-   Complete
-   Build Error
-   Authentication Error

When the metadata key is set to **Complete**, you can begin your
configuration management.

 

