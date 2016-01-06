---
node_id: 662
title: How to remap database users in myLittleAdmin
permalink: article/how-to-remap-database-users-in-mylittleadmin
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 20:3706'
last_modified_by: stephanie.fillmon
products: Cloud Sites
body_format: tinymce
---

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 MSSQL Security](#MSSQL_Security)                                  |
| -   [2 Remapping MSSQL Users](#Remapping_MSSQL_Users)                    |
|     -   [2.1 Remapping Database Users to                                 |
|         Logins](#Remapping_Database_Users_to_Logins)                     |
+--------------------------------------------------------------------------+

MSSQL Security
--------------

MSSQL has two logical layers of security. The term **login** refers to
the account at the server level. The term **user** refers to the account
that lives inside the database. When you restore a database from one
server to another server you effectively sever the mapping between the
server-level login and the database-level users.

All databases have a single owner that is assigned to a server-level
login. That special owner login is mapped to the a special database user
called **dbo**. The owner login account and password is the primary
administrative account for your database.

You may need to reestablish the mappings between the server-level logins
and the database users in order for the new database to be accessible.

Your new server-level logins are found in your Rackspace Cloud control
panel under your MSSQL 2008 Database.

Remapping MSSQL Users
---------------------

To manage your MSSQL database, you'll first need to [login to the online
manager
(myLittleAdmin)](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-sites-essentials-mylittleadmin-database-management-interface "Working with a MSSQL database").

### Remapping Database Users to Logins

For additional login to user mappings that are not the special owner
account you can use the following command:

    ALTER USER [123456_olduser] WITH LOGIN = [123456_newlogin]

1.  Click **Tools** then **New Query**
2.  Please type in the following command to reassign ownership to the
    new login you created in the control panel (the brackets are
    required). Please remember to replace your database name and login
    name:

        ALTER AUTHORIZATION
        ON Database::[123456_database]
        TO [123456_login]

    ![mssql2.jpg](http://c0476992.cdn.cloudfiles.rackspacecloud.com/mssql2.jpg)

3.  Verify the command worked by going to your database and viewing the
    properties. The login should now be listed as the new owner


