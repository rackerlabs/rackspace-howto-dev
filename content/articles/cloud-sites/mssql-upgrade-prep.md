---
node_id: 679
title: MSSQL 2005 - 2008 Upgrade Testing
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-30 16:5521'
last_modified_by: stephanie.fillmon
products: Cloud Sites
body_format: tinymce
---

undefined7) The restore tool may notify you that the old users have no login
mapping on the new SQL 2008 cluster. At this point your new database
will be ready. The only access, at this point, is allowed to the owner
login that you used to restore the database. If you need to change the
owner to another login you created in the Cloud Sites Control Panel or
remap users in your database to new logins please refer to the KB
article on remapping database users and changing ownership in MSSQL.

