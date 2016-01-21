---
node_id: 4483
title: Rackspace Cloud Backup - Install the agent on Windows by using silent installation
type: article
created_date: '2015-01-20'
created_by: Rose Contreras
last_modified_date: '2015-09-01'
last_modified_by: Catherine Richardson
product: Cloud Backup
---

This article describes how to perform a fresh installation or update of
the Rackspace Cloud Backup agent on your Windows server by using the
silent installation method. If you are using a Linux server, see
\[Rackspace Cloud Backup - Install the Agent on
Linux\](http://www.rackspace.com/knowledge\_center/article/rackspace-cloud-backup-install-the-agent-linux)
for the parallel instructions. \*\*WARNING:\*\* The silent installation
procedure described in this article is for advanced users and should
only be run from an administrator account. Whenever possible, you should
install the Rackspace Cloud Backup agent using the interactive
installation described in the article \[Rackspace Cloud Backup - Install
the agent on
Windows\](https://admin.rackspace.com/knowledge\_center/node/4055/\#install).
\#\# Before you install \*\*NOTE:\*\* The Rackspace Cloud Backup agent
requires \*\*.NET 4.0 or higher\*\*. If you are reinstalling the agent
on a server, note that a new agent installation disconnects any
previously registered agents that were running on that server. The only
way to associate the backup data from a disconnected agent registration
is to perform a backup migration. You can perform a Vault Migration to a
connected agent via the Cloud Backup API call: -
\[http://docs.rackspace.com/rcbu/api/v1.0/rcbu-devguide/content/PUT\_migrateVault\_v1.0\_\_tenant\_id\_\_agent\_migratevault\_Agent.html\](http://docs.rackspace.com/rcbu/api/v1.0/rcbu-devguide/content/PUT\_migrateVault\_v1.0\_\_tenant\_id\_\_agent\_migratevault\_Agent.html)

Download the installer
----------------------

Determine whether your Windows server architecture is 64-bit or 32-bit,
and download the latest MSI installation file for that architecture from
\[http://agentrepo.drivesrvr.com/\](http://agentrepo.drivesrvr.com/). -
\[32-bit Windows
.msi\](http://97a6455ef60243cc8c74-57c93634a2c6eae60c16d098c741cf9b.r43.cf1.rackcdn.com/win32/driveclient-latest.msi)
- \[64-bit Windows
.msi\](http://97a6455ef60243cc8c74-57c93634a2c6eae60c16d098c741cf9b.r43.cf1.rackcdn.com/win64/driveclient-latest.msi)
(This file will almost always be the correct one for your server.) \#\#
Perform a silent installation Use the Windows package installer
(msiexec.exe) to install the Cloud Backup agent. A typical installation
from the command line or a batch file would be run as Administrator and
look like the following example: msiexec /i driveclient-latest.msi /qn
/l\*v %tmp%\\install-driveclient-latest.log APIUSER=myuser
APIKEY=abcdef1234567890abcdef1234567890
APIHOSTNAME=*region*.backup.api.rackspacecloud.com DATACENTER=IAD
DEBUGHIGH=true Use values for APIUSER, APIKEY, APIHOSTNAME, and
DATACENTER that match your installation. During a fresh installation,
the following options are used: - APIUSER (required): The user name that
you use to log in to Rackspace Cloud Control Panel. - APIKEY (required):
Your Rackspace Cloud API key. For information about viewing your API
key, see \[View and reset your API
key\](http://www.rackspace.com/knowledge\_center/article/view-and-reset-your-api-key).
- APIHOSTNAME is optional. The host address where the Cloud Backup API
endpoints reside. Host addresses for various data centers are listed in
the \[Service Access
Endpoints\](http://docs.rackspace.com/rcbu/api/v1.0/rcbu-devguide/content/Service\_Access\_Endpoints-d1e753.html).
The Service Access Endpoints should only be passing in the domain name
of the endpoint and not the full URL.

**Example**

**Good:**

`dfw.backup.api.rackspacecloud.com`

**Bad:**

`https://dfw.backup.api.rackspacecloud.com/v1.0/1234/`

- DEBUGHIGH (default \`false\`): Turns on debug-level logging in the MSI
custom actions and in the agent Updater service. - DATACENTER
(required): The data center associated with this server. Possible values
are ORD, DFW, SYD, IAD, HKG, and LON. Following are optional,
less-frequently used (expert) installation options that you can use: -
APIHOSTURL: The URL that is used for registration. Host addresses for
various data centers are listed in \[Service Access
Endpoints\](http://docs.rackspace.com/rcbu/api/v1.0/rcbu-devguide/content/Service\_Access\_Endpoints-d1e753.html)
in the API documentation. - FLAVOR (default \`raxcloudserver\`): \[Add
an explanation of what this option actually is.\] Possible values are
\`privatecloud\`, \`raxcloudserver\`, and \`personalmachine\`. -
INSTALLDIR (default \`\`%ProgramFiles%\\Driveclient\`\`): The
installation directory for agent executables. - UPGRADEARCH (default
\`win64\` or \`win32\` depending on the MSI agent type): The folder on
the download server where you find the MSI for the architecture that you
want. - UPGRADEBASEURL (default \`http://agentrepo.drivesrvr.com/\`):
The URL for the download server where the setup MSI files are stored.
For more options for installing MSI packages, see \[msiexec command line
options\](http://technet.microsoft.com/en-us/library/cc759262%28v=ws.10%29.aspx).
A successful installation results in two running services, the
Driveclient and the Updater. You can see these via \*\*services.msc\*\*.
For the verification steps to test the installation, see \[Test Windows
installation or
update\](https://admin.rackspace.com/knowledge\_center/article/rackspace-cloud-backup-install-the-agent-windows-using-silent-installation).



