---
node_id: 3401
title: 'FAQ: Role-Based Access Control (RBAC)'
permalink: article/role-based-access-control-rbac-faq
type: article
created_date: '2013-04-12 17:52:10'
created_by: renee.rendon
last_modified_date: '2014-10-27 19:5005'
last_modified_by: David Hendler
products: Cloud Hosting
body_format: tinymce
---

### What is the cost to opt in to RBAC? {#GettingStartedwithRBACRoughDraft-WhatisthecosttooptintoRBAC}

RBAC is a free feature that is available to selected open cloud services
with an API.

### Can a customer opt out of RBAC? {#GettingStartedwithRBACRoughDraft-CanacustomeroptoutofRBAC}

Customers can opt out by simply removing the account users.  

### Is RBAC available internationally? {#GettingStartedwithRBACRoughDraft-IsRBACavailableinternationally}

Yes, RBAC is available to all Rackspace customers.

### Can I configure custom role assignments when I add a user login to an existing contact?

Yes, you can. See [Managing: Role-Based Access Control
(RBAC)](http://www.rackspace.com/knowledge_center/article/managing-role-based-access-control-rbac) for
instructions.

### How do I query the capability of a given user? {#GettingStartedwithRBACRoughDraft-HowdoIquerythecapabilityofagivenuser}

You can query the roles for a given user by using the List User Global
Roles API operation described in the [Cloud Identity Client Developer
Guide](http://docs.rackspace.com/auth/api/v2.0/auth-client-devguide/content/Overview-d1e65.html). Additionally,
you can view the roles that a user has through the [Cloud Control
Panel](http://MyCloud.rackspace.com).

### Can I view multiple accounts in the Cloud Control Panel? {#GettingStartedwithRBACRoughDraft-CanIviewmultipleaccountsintheNewCloudControlPanel}

You may view only one account at a time in the Cloud Control Panel.

### Can Rackspace display per-billing or per-user usage?

No. Per-billing and per-user usage are not offered at this time.

### Which users can create support tickets? {#GettingStartedwithRBACRoughDraft-Whichuserscancreatetickets}

All users can create support tickets; however, only the account owner is
updated on the ticket status.

### Will I be able to delegate all functionality as an account owner? {#GettingStartedwithRBACRoughDraft-WillmultipleAccountAdministratorsbeallowed}

Not at this time, but we are working on developing and delivering that
functionality.

### Does RBAC provide fine-grained access control for specific servers, directories, or files? {#GettingStartedwithRBACRoughDraft-DoesRBACallowfine-grainedaccesscontroloverspecificserversdirectoriesorfiles}

RBAC is limited to granting a user control over a given product. It is
not granular enough to restrict access to individual servers, files, or
directories.

### Does the API offer more features for RBAC than the Cloud Control Panel offers?

Yes, at this time more features are available through the API. For more
information about using the API for RBAC see the [Rackspace API
Documentation](http://docs.rackspace.com/).

### Will account users automatically inherit the RackConnect and Managed Cloud features? {#GettingStartedwithRBACRoughDraft-WillaccountusersautomaticallyinherittheRackConnectandManagedCloudfeatures}

Yes.

### How does RBAC work with MyRackspace? {#GettingStartedwithRBACRoughDraft-HowwillRBACworkwithMyRack}

With the implementation of RBAC, account owners can leave permissions as
they are in MyRackspace or set up restricted access to specific products
for users through the Cloud Control Panel. For more detailed information
see [Using RBAC with
MyRackspace](http://www.rackspace.com/knowledge_center/article/using-rbac-with-myrackspace).

### Is there a way to link dedicated, hybrid, and cloud permissions? {#GettingStartedwithRBACRoughDraft-Isthereapathtolinkdedicatedhybridandcloudpermissions}

These permissions cannot be linked at this time. Having a common
permission scheme between dedicated, hybrid, and cloud customers will be
addressed in the future. 

### Are servers/containers/files/databases/load-balancers shared, or do users have their own set of resources?

All resources for an account are shared across users that have the
correct roles. In other words, account users do not have their own set
of resources but share a pool of resources that other users of the
account may have access to. 

### Where can I view the pop-up window that appeared when I initially enabled RBAC?

This is the initial pop-up window that appears when you enable RBAC. 

[![](/knowledge_center/sites/default/files/field/image/RBAC%20Initial%20PDF_0.png)](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/RBAC%20Initial%20PDF_0.png)

For information about additional products that will be RBAC enabled in
the future, see [RBAC
Overview](http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac).

For information about changing your admin credentials, see [Managing
RBAC](http://www.rackspace.com/knowledge_center/article/managing-role-based-access-control-rbac).

For access to the Cloud Control Panel, see the [Cloud Control
Panel](https://mycloud.rackspace.com/).

  
--

### [\< RBAC Permissions Matrix](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)  -  [Known Issues and Suggested Workarounds for RBAC\>](http://www.rackspace.com/knowledge_center/article/known-issues-and-suggested-workarounds-role-based-access-control)

