---
node_id: 416
title: PostgreSQL - Creating and Dropping Roles
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 17:3805'
last_modified_by: stephanie.fillmon
products: Cloud Servers
body_format: tinymce
---

undefined&mdash; important if
this superuser role will be specified for local and remote connections
to the database. We've also set the CREATEDB and CREATEROLE attributes.
With those attributes specified, our SQL statement will match the action
of the 'createuser -sPE' command.

