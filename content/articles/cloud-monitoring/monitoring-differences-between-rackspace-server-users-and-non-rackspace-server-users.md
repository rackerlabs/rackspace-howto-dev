---
node_id: 4104
title: 'Monitoring: Differences Between Rackspace Server Users and Non-Rackspace Server Users'
type: article
created_date: '2014-06-16'
created_by: Maria Abrahms
last_modified_date: '2016-01-05'
last_modified_by: Kyle Laffoon
product: Cloud Monitoring
body_format: tinymce
---

Rackspace Cloud Monitoring can be used on Rackspace servers and
non-Rackspace servers. When using a Rackspace server, you can be a
managed or an unmanaged user. There are some differences between what
you can do in any one of these circumstances. This page describes those
differences.

Please Note: The **Rackspace Managed** **Infrastructure Servers** column
(in the middle) overlaps at times with both the
**<span>Rackspace </span>Managed** **Operations Servers** and
**Unmanaged Non-Rackspace Servers** as the table indicates. There are no
managed non-Rackspace servers.

<span>Rackspace </span>Managed Operations Servers

<span>Rackspace </span>Managed Infrastructure Servers

Unmanaged Non-Rackspace Servers

Entities for Rackspace servers and databases are managed automatically,
this means:

-   Monitoring entities are created automatically for new Cloud Servers
    or new Cloud Database.
-   When a Cloud Server or Cloud Database is deleted, the associated
    entity is deleted in monitoring.
-   When the Cloud Server name is changed, the name is changed in
    monitoring automatically. (You cannot change the instance name for
    Cloud Database)

Entities for non-Rackspace servers and databases must be managed
manually, this means:

-   <span>Monitoring entities need to be created manually for new
    servers</span> <span>.</span> When configuring the default
    monitoring agent, you either select an entity you already created
    for it,or let the setup process create one for you.
-   When a server is deleted, you must delete the associated monitoring
    entity through the API or CLI.
-   When the server name is changed, you must manually change the name
    in monitoring.

The label for Rackspace Cloud Servers can only be changed on the Cloud
Server directly. The change will be propagated to monitoring system
quickly.

The instance name for Cloud Database cannot be changed.

CAN delete monitoring entities or change the label for servers.

Have the default notification plan: **npTechnicalContactsEmail** and
have an additional notification entry: **npManaged**

Have the default notification plan, **npTechnicalContactsEmail**, only.

The agent only needs the agent token to authenticate with the monitoring
server. This value is stored as **monitoring\_token** in the agent
configuration file.

The agent is able to identify the server it is installed on to the
server.

The agent needs the agent token to authenticate with the monitoring
server. This value is stored as **monitoring\_token** in the agent
configuration file.

In addition, the agent needs to know which entity it is installed on.
This value is the **agent\_id** associated with the entity on the
monitoring server. This is also a field in the agent configuration file

If you are going to create an image out of a non-Rackspace server to be
used to spin up more servers, you need to remove the **agent\_id** field
(*before you generate the image*) in the agent configuration file that
is generated when you run agent setup. Otherwise, the agent will be
associated with the same entity that the image was created from and the
checks won't work properly.

Agent configuration file location:

-   Ubuntu, CentOS: /etc/rackspace-monitoring-agent.cfg
-   Windows: c:\\ProgramData\\Rackspace
    Monitoring\\config\\rackspace-monitoring-agent.cfg

Learn more about agent configuration with the [Install the Cloud
Monitoring
Agent](/howto/install-and-configure-the-rackspace-monitoring-agent)
article.

By default, the monitoring agent is installed and turned ON and the
monitoring is configured automatically. For details, see Managed
accounts Hosting
([rackspace.com/managed-hosting/](http://rackspace.com/managed-hosting/)).



By default, the monitoring agent must be manually installed. For
details, see [Manually Configure the
Agent](http://docs.rackspace.com/cm/api/v1.0/cm-getting-started/content/install-configure.html#agent-config-manual)
in the *Cloud Monitoring Getting Started Guide*.

For Cloud Database customers, the monitoring agent is installed with
monitoring configured automatically, by default. For details, see Cloud
Database documentation
(<http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/Monitoring_Cloud_Databases-d1e4673.html>).

N/A

You can access some monitoring features through the Control Panel and
all the features through API. You can see more monitoring features, as
well as metrics, through the [Cloud
Intelligence interface](https://intelligence.rackspace.com).

<span>You can see monitoring features, as well as</span><span> metrics,
through the </span>[Cloud
Intelligence interface](https://intelligence.rackspace.com)<span>. </span>



