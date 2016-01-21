---
node_id: 4942
title: VMware vRealize Operations 6.1 Permissions List
type: article
created_date: '2015-11-18'
created_by: Erik Wilson
last_modified_date: '2016-01-13'
last_modified_by: Rose Contreras
product: Managed VMware Services
---

Dedicated VMware^&reg;^ vCenter Server&trade;, and Rackspace Private Cloud powered
by VMware vCloud^&reg;^ customers are assigned the VMware&reg; vRealize&trade;
Operations&trade; (vROps) \*\*PowerUserMinusRemediation\*\* role and have
privileges to perform all of the same actions as those who are assigned
the Administrator role, EXCEPT for user management, cluster management
or remediation actions. The following table identifies the privileges
that are \*\*NOT\*\* assigned to the PowerUserMinusRemediation role.
\*\*Privilege Category\*\* | \*\*Privileges\*\* | \*\*Impact\*\* --- |
--- | --- | \*\*Administration - Access Control\*\* | - Add, edit or
delete a role
- Manage object permission for user
- Manage user related operations
- Update password policy | The user can view, but cannot configure
access control for other users.
For example, the user cannot configure authentication sources.
\*\*Administration &ndash; Manage AuthSources\*\* | - Configure AuthSources |
The user can view, but cannot configure authentication sources.
For example, the user cannot add an Active Directory domain as
authentication source in the vROps environment. \*\*Administration &ndash;
Manage Cluster\*\* |- All administrative actions | The user can view,
but cannot perform any administration actions on the cluster.
For example, the user cannot add new vROps nodes to the cluster.
\*\*Administration &ndash; REST APIs\*\* | - Delete alert note | The user can
use REST APIs to perform all provided activities, except delete alert
notes. \*\*Content\*\* | - Manage
- Heat map configurations
- Manage
- Plug-Ins | The user can manage all content, except heat map
configurations and plug-ins. \*\*Environment\*\* | - Action | The user
cannot perform any of the out-of-the-box actions. \*\*Environment &ndash;
Alert Notes Management\*\* | - Delete | User can add, but cannot delete
alert notes.

