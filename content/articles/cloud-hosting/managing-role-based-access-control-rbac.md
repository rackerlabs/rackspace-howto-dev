---
node_id: 3567
title: 'Managing: Role-Based Access Control (RBAC)'
permalink: article/managing-role-based-access-control-rbac
type: article
created_date: '2013-06-28 20:57:29'
created_by: renee.rendon
last_modified_date: '2016-01-08 19:3924'
last_modified_by: kelly.holcomb
products: Cloud Hosting
body_format: tinymce
---

### Implementing RBAC through the Cloud Control Panel

The account owner implements RBAC by adding users to the account and
assigning roles. This article will guide the account owner through this
process using the [Cloud Control
Panel](https://mycloud.rackspace.com/). 

For information about setting up RBAC through the API, see the [Cloud
Identity Admin Developer
Guide](http://docs.rackspace.com/auth/api/v2.0/auth-client-devguide/content/Overview-d1e65.html).

     **Note:** It is possible to assign a mix multiple-product roles and
per-product roles to one user through the API. The most permissive role
will determine the user's level of access.

### Account Credentials

Rackspace recommends that the account owner change the account password
and secret question before adding new users to the account.

When new users are created, a temporary password is assigned to them,
which they should change at their first login.

Also, new users must be informed that they have been added to the
account. Rackspace does not notify them automatically. Account owners
may use the following text to notify their users:

**Your access to this account has changed. You have been added as a new
user, and you must update your credentials (password and secret
question) as soon as possible. See \<Insert Name\> for your temporary
access information.**

### Creating New Users  {#GettingStartedwithRBACRoughDraft-CreatingnewusersthroughtheNewCloudControlPanel}

1. In the upper-right corner of the [Cloud Control
Panel](https://mycloud.rackspace.com/), click userName (accountNumber).

2. From the menu, select **User Management.**

![](/knowledge_center/sites/default/files/field/image/UserManagement_1.png)

3. In the **User Management** box, click **Create User**.

4. Complete the **Username**, **Password**, **Security Question**, and
**Security Answer** fields.  

     **Note:** Username must be unique. You cannot recover the username
of a deleted user.

5. Select a role to assign to the user.

-   If the **Custom** role is chosen, go to step 6.
-   If the **Full Access** or **Read-only Access** role is chosen, skip
    to step 7.

6. In the **Product Access** section, select a role for each user. For
optimal product interaction see [Suggested Role
Configurations.](#configuration) 

**     Note: **Once a user has been assigned the custom role, this role
cannot be changed to a multi-product role through the Cloud Control
Panel. For more information about changing a custom role to a full
access or read-only access role see[ custom
role](http://www.rackspace.com/knowledge_center/article/known-issues-and-suggested-workarounds-role-based-access-control-rbac).

7. In the **Contact Information** section, select the contact type.

8. Specify the contact&rsquo;s name and email address.

9. If the primary contact&rsquo;s details will be used for the user, slect
the **Use Primary Contact Details check box**. Otherwise, specify the
user's contact details.

10. Click **Create User**.

**     Note:** The Control Panel view is different for each user
depending on the roles assigned.

### Suggested Role Configurations 

Rackspace recommends the following custom role configurations for
optimal product interaction.

PRODUCT

IF:

AND:

THEN:

**First Generation Cloud Servers**

A user has been assigned any First Generation Cloud Server role

 

In First Generation Cloud Servers, give the user the Observer
role (minimum action)

**First Generation Cloud Servers** 

A user needs to backup an image

The user has been assigned any First Generation Cloud Server role 

In First Generation Cloud Servers & Cloud Files, give the user the Admin
role 

**Cloud Load Balancers**

A user has been assigned any Cloud Load Balancers role

 

In First Generation and Next Generation Cloud Servers, give the user the
Observer role (minimum action)

**Cloud Load Balancers**** **

A user wants to add a node by using "Add Nodes: Add Cloud Server ..." in
the Cloud Control Panel

The user has been assigned any Cloud Load Balancers role

In First Generation or Next Generation Cloud Servers, give the user any
role 

**Cloud Databases**

A user wants to create a backup in Cloud Databases

 

In Cloud Files, give the user the Admin role

### **Adding a User Login and Custom Role to an Existing Contact** {.MsoNormal}

1. In the **User Management** box, click the actions cog next to the
contact's name.

2. Click **Add Login...**

3. Complete the **Username**, **Password**, **Security Question**, and
**Security Answer** fields.

4. Click **Save User Information** after choosing the custom role.

5. Click the actions cog next to that user's name and configure the
custom role.

### Rackspace Customers with Multiple Accounts

Rackspace customers with more than one account may want to allow the
same user to access to each account. In this situation, the account
owner will need to configure that user with a different username for
each account. The following graphic illustrates this scenario.

![](/knowledge_center/sites/default/files/field/image/MutiAccountsRBAC.png)

 

[\< Overview of RBAC ](http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac)  -   [Using RBAC with MyRack \>](http://www.rackspace.com/knowledge_center/article/using-rbac-with-myrackspace)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 

