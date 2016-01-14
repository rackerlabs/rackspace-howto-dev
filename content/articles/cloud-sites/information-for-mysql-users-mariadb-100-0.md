---
node_id: 4729
title: Information for MySQL Users (MariaDB 10.0)
type: article
created_date: '2015-06-25 20:55:17'
created_by: alonzo.garza
last_modified_date: '2016-01-04 15:5953'
last_modified_by: Nate.Archer
product: Cloud Sites
body_format: tinymce
---

 
-

**What is changing?**
---------------------

Within our DFW datacenter, Cloud Sites will be updating existing MySQL
databases to MariaDB 10.0 which is a highly compatible, drop in
replacement for MySQL. This maintenance allows Cloud Sites to continue
to evolve and provide a more secure and reliable infrastructure for our
customers. Below are the upcoming changes:

-   Existing MySQL databases will be upgraded to Maria DB 10.0
-   External IPs used to manage your database will change. Please refer
    to the Control Panel for the new IP.
-   We will be deploying the latest version of phpMyAdmin for MySQL web
    administration.
-   URLs to access these services will be changing. Please refer to the
    table below for information on the new URL.
-   The URLs for site management will be available after September 1st.

  Current Website Testlink   NEW phpMyAdmin URL
  -------------------------- --------------------------------------------------------------------------------------
  Contains "DFW1-1"          [https://mysql.dfw3-1.websitesettings.com](https://mysql.dfw3-1.websitesettings.com)
  Contains "DFW1-2"          [https://mysql.dfw3-2.websitesettings.com](https://mysql.dfw3-2.websitesettings.com)

**Technology Reference for MariaDB 10.0**

-   Feature comparisons:
    [https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-features/](https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-features/)
-   Replacement for MySQL:
    [https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-compatibility/](https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-compatibility/)
-   MariaDB FAQ site:
    [https://mariadb.com/kb/en/meta/about-the-mariadb-knowledge-base/](https://mariadb.com/kb/en/meta/about-the-mariadb-knowledge-base/)

**What is not changing?**
-------------------------

-   Plugins and database connectors that utilize your DB will not need
    to be updated. Maria DB is a drop in replacement for MySQL
-   We will create an alias from the old hostname to the new hostname
    automatically. \*Note - In the future we will deprecate the former
    hostnames at end of Q2 2016
-   Cloud Database instances are not subject to this migration (Note:
    Our outbound IPs will be changing, if you are using any IP based
    ACLs on external resources, please see
    [here](http://rackspace.com/knowledge_center/article/information-for-customer-ips-dns-0)

 
-

**FAQ**
-------

**MySQL Workbench stopped connecting after the maintenance. What could
have occurred?**

-   External database Management IPs will be changing. These IPs will be
    visible in your control panel's page within the database section.

**How do I reference my database IP information?** 

-   Log into your Cloud Sites control panel
    at [manage.rackspacecloud.com](http://manage.rackspacecloud.com)
-   Click on 'Hosting' \>\> 'Cloud Sites' and select the domain under
    which the database was created
-   From the domain details page click on the 'Features' tab and select
    the active database you wish to reference:

![](/knowledge_center/sites/default/files/field/image/MySQL.png)

**Will my database content be affected after the maintenance?**

-   No. Data will not be modified during the maintenance. Only Hostname
    and IP information will be changing

**Will my former hostname information be affected after the
maintenance?**

-   External IPs for your instances will be updated and the former IPs
    will no longer be usable for connection strings
-   Former hostnames will automatically be aliased to the new database
    host

 

**Related Topics**

-   [Important scheduled maintenance: DFW environment
    migration](http://rackspace.com/knowledge_center/article/important-scheduled-maintenance-dfw-environment-migration)
-   [Information for Customer IPs &
    DNS](http://rackspace.com/knowledge_center/article/information-for-customer-ips-dns-0)
-   [Information for MS SQL
    changes](http://rackspace.com/knowledge_center/article/information-for-ms-sql-changes)
-   [Information for MySQL Users (MariaDB
    10.0)](http://rackspace.com/knowledge_center/article/information-for-mysql-users-mariadb-100-0)
-   [Information for new PHP 5.6 & Apache
    version](http://rackspace.com/knowledge_center/article/information-for-new-php-56-apache-version-0)


