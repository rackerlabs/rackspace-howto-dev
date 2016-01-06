---
node_id: 3648
title: 'Known Issues and Suggested Workarounds: Role-Based Access Control (RBAC)'
permalink: article/known-issues-and-suggested-workarounds-role-based-access-control
type: article
created_date: '2013-08-16 21:20:33'
created_by: renee.rendon
last_modified_date: '2013-09-26 19:3758'
last_modified_by: kyle.laffoon
products: Cloud Hosting
body_format: tinymce
---

This is a list of known issues with Role-based Access Control (RBAC). We
are diligently working to resolve these issues. If you are experiencing
an issue that is not listed, please contact customer support at
1-800-961-4454.

### Custom Role 

**Known Issue:** After a user has been assigned the custom role, the
account owner cannot change this role to a multiproduct role by using
the Cloud Control Panel. 

**Workaround:** The account owner can simulate the full access role by
assigning to the user the admin role for all available products. To
simulate the read-only access role, the account owner can assign to the
user the observer role for all available products. 

     **Note:** The custom role will not be updated automatically when
new Rackspace products become RBAC enabled. The account owner must
update custom roles to include the new products.

You can also change the custom role to a multiproduct role by contacting
Support at 1-800-961-4454.    

### Multiple Roles for One User

**Known Issue:** Multiple roles for one user can only be assigned
through the [API](http://docs.rackspace.com/). The Cloud Control Panel
displays only the first role assigned to users that have multiple
roles. 

**Workaround:** A user's multiple roles can be viewed through the
[API](http://docs.rackspace.com/).

### Suspended Account

**Known Issue:** When an account is suspended, all users of the account
are disabled. Users are not automatically re-enabled when the account is
reactivated.

**Workaround:** When the account is reactivated, the account owner must
re-enable users through the API or by contacting support at
1-800-961-4454. 

 [\< RBAC FAQs](http://www.rackspace.com/knowledge_center/article/faq-role-based-access-control-rbac)    -    [Getting Started with RBAC \>](http://www.rackspace.com/knowledge_center/article/getting-started-with-role-based-access-control-rbac-0) {.MsoNormal style="mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; line-height: 16.65pt; background: white;"}
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

