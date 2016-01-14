---
node_id: 664
title: Migrate a Cloud Site from MSSQL2005 to MSSQL2008
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2016-01-12 20:1812'
last_modified_by: stephanie.fillmon
product: Cloud Sites
body_format: tinymce
---

undefined&rdquo; may cause session
    issues between the two MyLittleAdmin versions. For example:
    `https://mssqladmin.websitesettings.com/mlb`![mlb1.JPG](http://c0476992.cdn.cloudfiles.rackspacecloud.com/mlb1.JPG)
4.  Login to your original MSSQL 2005 source
    database.![mlb2.JPG](http://c0476992.cdn.cloudfiles.rackspacecloud.com/mlb2.JPG)
5.  Now back up your MSSQL 2005 database use the MyLittleAdmin tool.
    When the backup has completed click on the file link to save the
    backup file to your local machine.
6.  Log in to the MyLittleAdmin link again using your MSSQL 2008
    database and login. Remember the login you use to restore will
    become the new owner of the database. Choose restore and upload the
    backup file you just downloaded in Step 5. Proceed with the
    restore.![mlb3.JPG](http://c0476992.cdn.cloudfiles.rackspacecloud.com/mlb3.JPG)
7.  The restore tool may notify you that the old users have no login
    mapping on the new SQL 2008 cluster. At this point your new database
    will be ready. The only access, at this point, is allowed to the
    owner login that you used to restore the database. If you need to
    change the owner to another login you created in the control panel
    or remap users in your database to new logins please refer to the KB
    article [How to Change ownership and remap database users using the
    web based admin tool for
    MSSQL.](http://www.rackspace.com/knowledge_center/article/how-to-remap-database-users-in-mylittleadmin "How to Change ownership and remap database users using the web based admin tool for MSSQL.")
8.  Once the migration is complete, update all connection strings to
    point to the new database. After you verify that everything is
    working from the MSSQL2008 database, delete your MSSQL2005 database
    and confirm with Cloud Sites Support that the migration is complete.
    This will ensure that you are not billed for the additional database
    in the future.

-- C. Tannery

 

