---
node_id: 3403
title: 'Overview: Role Based Access Control (RBAC)'
permalink: article/getting-started-with-role-based-access-control-rbac
type: article
created_date: '2013-04-14 21:20:30'
created_by: renee.rendon
last_modified_date: '2016-01-03 16:0733'
last_modified_by: renee.rendon
products: 'Cloud Hosting,Cloud Servers,Cloud Files,Cloud Load Balancers,Cloud Databases'
body_format: tinymce
---

This guide is designed to get administrators started with Role-Based
Access Control (RBAC) and to answer questions about the service. 

### What is RBAC? {#GettingStartedwithRBACRoughDraft-WhatisRBAC .field-items}

RBAC is a secure method of restricting account access to authorized
users. This method enables the account owner to add users to the account
and assign each user to specific roles. Each role has specific
permissions defined by Rackspace. RBAC allows users to perform various
actions based on the scope of their assigned role.

The account owner has the ability to create up to 100 users, each with
their own password, secret question and answer, and API key.

### Why implement RBAC?

RBAC is important because it provides customers a greater degree of
control over cloud resource utilization with the added layer of system
security.

### What are roles? {#GettingStartedwithRBACRoughDraft-Whatareroles .field-items}

*Role* describes the level of access users have for their account. By
assigning roles to users, administrators can allow multiple users to
complete tasks safely. RBAC limits risk by ensuring that users do not
have access beyond their training or level of control.

Roles grant access across all resources of a single product or for
multiple products. RBAC does not restrict access to specific files,
directories, or servers. 

### What roles are available through RBAC? {#GettingStartedwithRBACRoughDraft-WhatrolesareavailablethroughRBAC .field-items}

RBAC provides the following roles.

### Multiple-product roles {#GettingStartedwithRBACRoughDraft-TIER1-Theaccountadminrole}

-   **Full access** - The full access role has the permissions to
    create, read, update, and delete resources within multiple
    designated products where access is granted. These permissions apply
    to products that are currently [RBAC enabled products](#enabled) and
    to products as they become RBAC-enabled in the future.

-   **Read-only access** - The read-only access role has permissions to
    view given resources within multiple designated products where
    access is granted. These permissions apply to products that are
    currently [RBAC enabled products](#enabled) and to products as they
    become RBAC-enabled in the future.

**Note**: Users with the full access or the read-only roles will have
automatic access to all new products that become RBAC-enabled, with the
exception of account administration tasks such as billing. Product roles
do not include Account roles.

### **Custom roles** {#GettingStartedwithRBACRoughDraft-TIER3-Thefollowingsingle-productrolesareavailable}

The Custom roles provide a useful mix of permission levels for assigning
permissions per product. After the user is assigned the Custom roles,
roles can be changed only per product.

-   **Product:admin** - The *product* admin role has permissions to
    create, read, update, and delete resources within the designated
    product where access is granted. 

-   **Product:creator** - The *product* creator role has permissions to
    create, read, and update resources within the designated product
    where access is granted. The creator role cannot delete a resource.
    (Any destructive actions are prohibited.)

-   **Product:observer** - The *product* observer role has permission to
    read given resources within the designated product where access is
    granted. This role is read-only.

 

### **Account roles**

Assign Account roles to users who manage your Rackspace customer
account. 

-   **Billing:admin &ndash;** The *account* role of billing admin has
    permissions to create, read, update, and delete given billing and
    payment resources within the designated product where access is
    granted.

-   **Billing:observer &ndash;** The *account* role billing observer has
    permission to read given billing and payment resources within the
    designated product where access is granted. This role is read-only.

To give a new user account permissions without product permissions,
choose the Custom setting and keep all Product roles set to No Access.
Then assign the appropriate Account role to the user.

**Note:** A user may be assigned Product roles and Account roles.

 

### What types of users does RBAC have?

RBAC has the following types of users:

-   **Account owner - **The account owner is the primary contact for the
    account and has full permissions to execute all capabilities for
    every product available. Each account is allowed only one account
    owner.

-   **Account user - **The account user is a user that has been added by
    the account owner and has been assigned to specific product or
    account roles.

 

### What actions are restricted to the account owner role?

Only the account owner role can perform the following actions:

-   Create new users, modify existing users, and delete users.
-   Make contact changes, including the billing contact.

 

### **What are the contact types in the Control Panel?** {.p1}

The following types of contacts are shown in the Control Panel. Contact
types are similar to tags that can assist with user management. 

-   **Primary &ndash;** This contact type is automatically assigned to the
    owner of the account. Only one Primary contact is allowed per
    account.
-   **Billing -** This contact type is automatically assigned to the
    account. Only one Billing contact is allowed per account. It is not
    necessary to assign a username to the Billing contact. This contact
    holds the address that Rackspace uses as the billing address.
-   **Administrative &ndash;** This contact type can be assigned to users that
    primarily perform administrative duties such as billing and
    payments. Administrative contacts do not receive technical alerts
    from our automated systems. No specific account implications come
    with this role. For example, if administrative users change their
    address, the change does not affect the billing address. 
-   **Technical &ndash;** This contact type can be assigned to users that
    primarily perform technical tasks. These users receive monitoring
    alerts by default unless the notification plan is changed. 

 

### When is it beneficial to implement RBAC?

RBAC should be implemented in the following situations:

-   In an effort to minimize downtime and accidental changes to the
    cloud resources, the account owner would like to restrict access to
    the accounts to only a few people.
-   In an effort to synchronize cloud product access to the functions of
    an employee&rsquo;s job, the account owner would like to grant access to
    employees based on the nature of their position.
-   In an effort to help prevent unauthorized access to cloud products
    through the sharing of admin credentials, the account owner would
    like each user of the cloud accounts to have their own credentials.

 

### When is it not necessary to implement RBAC?

RBAC does not need to be implemented when only one credential set is
needed for an account.

 

### Who can use RBAC? {#GettingStartedwithRBACRoughDraft-WhocanuseRBAC .field-items}

RBAC is available to all Rackspace customers. 

 

### How can I get RBAC? {#GettingStartedwithRBACRoughDraft-HowcanIgetRBAC .field-items}

Adding users to the account activates RBAC. Account owners can add users
through the Cloud Control Panel or through API.

For more information about specific RBAC-related APIs, see the Rackspace
API documentation
at [http://docs.rackspace.com](http://docs.rackspace.com/).

 

### Which products are currently RBAC enabled? {#GettingStartedwithRBACRoughDraft-WhichservicesincludeRBACasofnow .field-items}

-   [Next Generation
    Servers](http://www.rackspace.com/knowledge_center/getting-started/cloud-servers)
-   [First Generation
    Servers](http://www.rackspace.com/knowledge_center/video/upgrade-to-next-gen-cloud-servers)
-   [Cloud
    Files](http://www.rackspace.com/knowledge_center/getting-started/cloud-files-0)
-   [Cloud
    Databases](http://www.rackspace.com/knowledge_center/getting-started/cloud-databases)
-   [Cloud Load
    Balancers](http://www.rackspace.com/knowledge_center/getting-started/cloud-load-balancers)
-   [Cloud
    Queues](http://www.rackspace.com/knowledge_center/article/creating-cloud-queues)
-   [Cloud
    Monitoring](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-monitoring-0) 
-   [Cloud
    Backup](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview)
-   [Cloud
    Networks](http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/ch_overview.html)
-   [Cloud Block
    Storage](http://www.rackspace.com/knowledge_center/article/cloud-block-storage-overview)
-   [Auto
    Scale](http://www.rackspace.com/knowledge_center/article/getting-started-with-auto-scale-introduction)
-   [Cloud
    Images](http://docs.rackspace.com/images/api/v2/ci-devguide/content/ch_image-service-dev-overview.html)
-   [Cloud Big Data
    v1](/knowledge_center/article/detailed-permissions-matrix-for-cloud-big-data) 
-   [Cloud Big Data
    v2](/knowledge_center/article/detailed-permissions-matrix-for-cloud-big-data-v2) 
-   [Cloud
    Orchestration](http://www.rackspace.com/knowledge_center/product-faq/cloud-orchestration)
-   [Cloud
    DNS](http://docs.rackspace.com/cdns/api/v1.0/cdns-getting-started/content/DB_Overview.html) 
-   [Cloud
    Feeds](http://docs.rackspace.com/cloud-feeds/api/v1.0/feeds-getting-started/content/Feeds_Overview.html)
-   [Rackspace
    CDN](http://www.rackspace.com/knowledge_center/getting-started/rackspace-cdn) 
-   [Billing and Payment
    Services](/knowledge_center/article/rackspace-cloud-billing-faq%20)

 

### Which products will be RBAC enabled in the future? {#GettingStartedwithRBACRoughDraft-WhichserviceswillincludeRBACinthefuture}

-   Rackspace Orchestration Service
-   New products as they are launched

 

### Which products will not have RBAC? {#GettingStartedwithRBACRoughDraft-WhichservicesdonotincludeRBAC}

-   Cloud Sites
-   RackConnect
-   Mailgun

 

[\< Getting Started with RBAC](http://www.rackspace.com/knowledge_center/article/getting-started-with-role-based-access-control-rbac-0)    -   [Managing RBAC \>](http://www.rackspace.com/knowledge_center/article/managing-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 

