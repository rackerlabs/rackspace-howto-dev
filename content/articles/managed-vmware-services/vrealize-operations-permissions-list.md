---
node_id: 4942
title: VMware vRealize Operations 6.1 Permissions List
type: article
created_date: '2015-11-18 19:26:31'
created_by: erik.wilson
last_modified_date: '2016-01-13 15:3356'
last_modified_by: rose.contreras
product: Managed VMware Services
body_format: markdown_w_tinymce
---

Dedicated VMware<sup>®</sup> vCenter Server™, and Rackspace Private Cloud powered by VMware vCloud<sup>®</sup> customers are assigned the VMware® vRealize™ Operations™ (vROps) **PowerUserMinusRemediation** role and have privileges to perform all of the same actions as those who are assigned the Administrator role, EXCEPT for user management, cluster management or remediation actions.

The following table identifies the privileges that are **NOT** assigned to the PowerUserMinusRemediation role.

**Privilege Category** | **Privileges** | **Impact**
--- | --- | --- |
**Administration - Access Control** | - Add, edit or delete a role<br />- Manage object permission for user <br />- Manage user related operations <br />- Update password policy | The user can view, but cannot configure access control for other users.<br />For example, the user cannot configure authentication sources.
**Administration – Manage AuthSources** | - Configure AuthSources | The user can view, but cannot configure authentication sources.<br />For example, the user cannot add an Active Directory domain as authentication source in the vROps environment.
**Administration – Manage Cluster** |- All administrative actions | The user can view, but cannot perform any administration actions on the cluster.<br />For example, the user cannot add new vROps nodes to the cluster.
**Administration – REST APIs** | - Delete alert note | The user can use REST APIs to perform all provided activities, except delete alert notes.
**Content** | - Manage<br />- Heat map configurations<br />- Manage<br />- Plug-Ins | The user can manage all content, except heat map configurations and plug-ins.
**Environment** | - Action | The user cannot perform any of the out-of-the-box actions.
**Environment –<br />Alert Notes Management** | - Delete | User can add, but cannot delete alert notes.
