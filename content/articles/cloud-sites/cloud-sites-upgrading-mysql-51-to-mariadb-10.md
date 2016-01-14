---
node_id: 4554
title: Migrate a MySQL 5.1 database to MariaDB 10 on Cloud Sites
type: article
created_date: '2015-02-09 16:42:56'
created_by: thomas.hester
last_modified_date: '2015-09-15 00:1707'
last_modified_by: kelly.holcomb
product: Cloud Sites
body_format: tinymce
---

Cloud Sites has added MariaDB 10 as a database option. Although it is a
different engine, it is fully compatible with the MySQL connections and
syntax. This upgrade is an effort to keep Cloud Sites up-to-date with
current software, security, and usability. New databases can be
provisioned with MariaDB, and users can migrate their databases from
MySQL 5.1 to MariaDB by creating a backup and then importing to a new
MariaDB database. This article provides the steps for such a migration.

**Notes:**

-   MySQL 5.1 can still be provisioned, and no databases will be forced
    to migrate.<br>
      
-   Currently, customers cannot perform backups that call
    **mysqldump**because the version on the servers is incompatible with
    MariaDB 10. However, Support can perform these backups.

**Availability of MariaDB**
---------------------------

MariaDB is now available in the ORD data center and will be available in
the DFW data center in the future. We do not currently have a timeline
for deployment in DFW.

**MariaDB instead of MySQL 5.6**
--------------------------------

MariaDB has several features available on top of what is available for
MySQL 5.6. See the following links for more information:

-   [https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-features/](https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-features/)

-   [https://mariadb.com/kb/en/meta/about-the-mariadb-knowledge-base/](https://mariadb.com/kb/en/meta/about-the-mariadb-knowledge-base/)

-   [https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-compatibility/](https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-compatibility/)

**Migrate your database from MySQL to MariaDB**
-----------------------------------------------

### **Step 1: Create your MariaDB database in the Cloud Sites control panel**

1.  Log in to the Cloud SItes Control Panel.<br>
      
2.  Navigate to the site for which you want to add the database.<br>
      
3.  Click the **Features**tab.<br>
      
4.  Under Databases, click **Add**.<br>
      
5.  Enter a unique name for the database, select **MariaDB**from the
    **Database Type** menu, and then click **Continue**. <br>
      
6.  Enter the username and password to use for the database, and then
    click **Finish**.<br>
     <br>
     The **Features**tab is displayed again.<br>
      
7.  Click on the newly created database to display the hostname
    information, whcih you will need in Step 3.

    ![Database connection
    information](/knowledge_center/sites/default/files/field/image/db_info.png)

### **Step 2: Put your site into maintenance mode and export your current database**

There are multiple ways to put a site into maintenance mode, or
otherwise take it offline temporarily, but those instructions are beyond
the scope of this article. The most simple method is to rename your
content folder in an FTP client and create a new content folder with an
**index.html** file that contains your maintenance message. After the
database migration is completed, you reverse this action.

Export your current MySQL database either by [using
phpMyAdmin](/knowledge_center/node/661) or by [using a cron
task](/knowledge_center/node/644).

After it is exported, you will import the database backup to MariaDB by
using the same method that you used to export the file.

### **Step 3: Update your connection strings to the new MariaDB settings**

Open any files that contain the connection settings for your database,
and update them to the MariaDB settings from the database
information window that was displayed at the end of Step 1.

### **Step 4: Put your site back online**

Take the site out of maintenance mode and refresh any caches on your
site to ensure that all references are updated for the new connections.
The data is the same as it was, but it's good practice to refresh after
a technology change to ensure that everything is up-to-date and works as
expected.

