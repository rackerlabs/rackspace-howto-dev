---
node_id: 4368
title: FAQ for Seamless sign-on between MyRackspace and the Cloud Control Panel
type: article
created_date: '2014-10-15 23:30:45'
created_by: David Hendler
last_modified_date: '2014-10-21 22:3507'
last_modified_by: David Hendler
products: Dedicated
body_format: tinymce
---

Get quick answers to common questions about Seamless sign-on (SSO)
between the MyRackspace Customer Portal and the Rackspace Cloud Control
Panel.

-   [What is seamless sign-on (SSO)?](#whatis)
-   [How do I use SSO?](#howdoi)
-   [How do I disable SSO?](#disable)
-   [What permissions do I have when using SSO?](#permissions)
-   [How do MyRackspace persmissions map to Cloud Control Panel
    permissions?](#mapping)
-   [How are user permissions set or changed for
    SSO?](#changepermissions)
-   [Can I link to MyRackspace from the Cloud Control Panel?](#linkback)
-   [Can I log in to the Cloud Control Panel and seamlessly link to and
    be logged in to MyRackspace?](#seamless)
-   [Can I manage all my tickets, biling, and users in one place
    now?](#manageeverything)
-   [How do I add or modify metadata?](#metadata)
-   [What are the limitations of SSO?](#limitations)

### What is seamless sign-on (SSO)?

Rackspace allows dedicated customers to manage your public cloud
environment without having to sign on multiple times. After you log in
to the MyRackspace Customer Portal, you can seamlessly move between your
dedicated account and its corresponding linked cloud accounts.

([back to top](#top))

### How do I use SSO?

SSO is integrated into our products as much as possible. When you
navigate Cloud accounts in the MyRackspace portal, hyperlinks for
products such as Cloud Servers, Cloud Networks, and Cloud DNS take you
to the Cloud Control Panel where you are logged in automatically.

![MyRackspace screenshot - Access SSO from the cog next to the user
name](/knowledge_center/sites/default/files/field/image/sso_howto_use.png)

([back to top](#top))

### How do I disable SSO?

You may remove user permissions from any linked Cloud account for which
you do not want someone to have SSO access. Manage your user permissions
the MyRackspace portal by navigating to **Account \> Permissions \>
Assign by Product**.

([back to top](#top))

### What permissions do I have when using SSO?

Permissions are based on the access set for the individual Cloud account
you are trying to access.

![MyRackspace screenshot - layout of permissions
screen](/knowledge_center/sites/default/files/field/image/sso_permissions_layout.png)

([back to top](#top))

### How do MyRackspace permissions map to Cloud Control Panel permissions?

+--------------------------+--------------------------+--------------------------+
|  MyRackspace             |  \>\>\>                  |  Cloud Control Panel     |
+==========================+==========================+==========================+
|  NONE                    |  =                       |  NONE                    |
+--------------------------+--------------------------+--------------------------+
|  VIEW                    |  =                       | OBSERVER                 |
+--------------------------+--------------------------+--------------------------+
|  EDIT                    |  =                       |  ADMIN                   |
+--------------------------+--------------------------+--------------------------+
| ADMIN                    | =                        | ADMIN                    |
+--------------------------+--------------------------+--------------------------+

([back to top](#top))

### How are user permissions set or changed for SSO?

User permissions for SSO are directly mapped based on the user's Cloud
account permission settings.You can view permissions by user or by
product.

**View permissions by user:**

![MyRackspace screenshot - Assign SSO permissions by
user](/knowledge_center/sites/default/files/field/image/sso_permissions_by_user.png)

**View permissions by product:**

![MyRackspace screenshot - Assign SSO permissions by
product](/knowledge_center/sites/default/files/field/image/sso_permission_by_product.png)

([back to top](#top))

### Can I link back to MyRackspace from the Cloud Control Panel?

Yes. Click the **Back to MyRackspace** link in the upper-left corner of
the Cloud Control Panel.

([back to top](#top))

### Can I log in to the Cloud Control Panel and seamlessly link to and be logged in to MyRackspace?

No, not at this time.

([back to top](#top))

### Can I manage all my tickets, billing, and users in one place now?

No, not at this time. Tickets, billing, and users are currently managed
separately in the respective interfaces.

([back to top](#top))

### How do I add or modify metadata?

With the introduction of this new functionality, one of the features
that will no longer be available is the ability to edit Cloud Server
metadata via a user interface (like MyRackspace). In lieu of this
functionality, there are 3 options:

1.  Use the Nova Client to issue these commands. The Nova Client can be
    installed quickly and allows you to provision and delete servers,
    work with metadata, and more. See the [Python Nova Client command
    reference](/knowledge_center/article/useful-python-novaclient-commands)
    for more information.
2.  Use the Cloud Servers API to specify your server's metadata. The
    [Cloud Servers Developer's
    Guide](http://docs.rackspace.com/servers/api/v2/cs-devguide/content/Create_or_Replace_Metadata-d1e5358.html)
    provides instructions on how to do this.
3.  Enlist your Rackspace Support team by phone or ticket to make these
    changes on your behalf.

([back to top](#top))

### What are the limitations of SSO?

-   Tickets are not consolidated to one location. Cloud and Dedicated
    support tickets are still handled in their respective interfaces.
-   User management is not consolidated to one location. Cloud and
    MyRackspace users are still managed separately.
-   The following items are not available when you are logged in to the
    Cloud Control Panel via SSO from MyRackspace:
    -   Billing and Payments
    -   Usage Overview
    -   Account Settings
    -   User Management
    -   Service level upgrades

To access these features, log out and then log in directly to the [Cloud
Control Panel](http://mycloud.rackspace.com) with your cloud
credentials.

([back to top](#top))

