---
node_id: 4727
title: Information for customer IP addresses and DNS
permalink: article/information-for-customer-ips-dns-0
type: article
created_date: '2015-06-25 20:47:40'
created_by: alonzo.garza
last_modified_date: '2015-09-26 01:0233'
last_modified_by: renee.rendon
products: Cloud Sites
body_format: full_html
---

**What is changing?**
---------------------

-   Outbound IP addresses for access to external services, such as
    Twitter or Facebook, will change. If you have an external service
    restricting access by IP address, use the following IP addresses
    your whitelist prior to September 1, 2015:
    IP address ranges
    *72.32.10.144/28&ndash;WC1.DFW3 outbound pool*
    *72.32.47.176/28&ndash;WC2.DFW3 outbound pool*
    *72.32.10.144 - 72.32.10.159 (WC1.DFW3)*
    *72.32.47.176 - 72.32.47.191 (WC2.DFW3)*
-   Outbound IP addresses for access to ServiceNet resources will
    change. If you have any ServiceNet resources such as Cloud Servers,
    Cloud Databases, etc., restricting access by IP address, please add
    **10.187.240.0/20** to your whitelists.\
    \
-   Database management IP addresses will change. Based on your
    technology, please reference
    [MSSQL](http://rackspace.com/knowledge_center/article/information-for-ms-sql-changes)
    or
    [MySQL](http://rackspace.com/knowledge_center/article/information-for-mysql-users-mariadb-100-0)
    for more information.\
    \
-   Test links for websites will be changing to reflect their new
    location. Test links should only be used for testing purposes and
    can change at any time. Please see the table below for new test link
    information.\
    \
-   The URLs for site management will be available after September 1,
    2015.
      Current Testlink URL   NEW Testlink URL
      ---------------------- -----------------------------------------------------------
      Contains "DFW1-1"      www.yoursite.com.*cluster.***dfw3-1**.websitetestlink.com
      Contains "DFW1-2"      www.yoursite.com.*cluster.***dfw3-2**.websitetestlink.com

**What is not changing?**
-------------------------

-   Customers will not need to update their DNS entries for their
    websites. We will be migrating SSL and cluster IPs over\*.\
    \
-   Customers using 3rd party DDoS mitigation services (such as
    CloudFlare) will not need to update anything on their end.\
    \
-   FTP records and IPs will also remain the same\*.

    **Note:** Old DNS entries (i.e., test links) will be retired by end
    of Q2 2016.

**How does this affect me?**
----------------------------

Most customers will not have to make any changes in order to continue
functioning correctly.

Customers that will likely be affected are those using outdated security
practices. Here are examples of websites likely affected:

-   Websites using external services (only if those have firewalls
    restricting by IP address)
-   Websites running a completely (or partially) from the testlink
-   Websites using the database management IP for external production
    access
-   Websites that have hard-coded IP addresses instead of a hostname

**FAQ**
-------

**My site feed (example: Twitter, Facebook, Instagram) stopped working
after the maintenance. What could have occurred?**

-   The outbound IPs will be changing. If your site connects to external
    applications or services, these will need to be updated.

**My site connects to my Cloud Server to manage my databases and
caching, but after the maintenance, it stopped working. What could have
occurred?**

-   The outbound IP addresses have changed. If your site connects to
    another Rackspace service like a Cloud Server, add the following IP
    addresses to your network rules to accept the connections:
    IP address ranges
    *72.32.10.144/28&ndash;WC1.DFW3 outbound pool*
    *72.32.47.176/28&ndash;WC2.DFW3 outbound pool*
    *72.32.10.144 - 72.32.10.159 (WC1.DFW3)*
    *72.32.47.176 - 72.32.47.191 (WC2.DFW3)*

**MySQL Workbench/SQL Server Management Studio stopped connecting after
the maintenance. What could have occurred?**

-   External database management IPs will be changing.Based on your
    technology, please
    reference [MSSQL](http://rackspace.com/knowledge_center/article/information-for-ms-sql-changes) or [MySQL](http://rackspace.com/knowledge_center/article/information-for-mysql-users-mariadb-100-0) for
    more information

**My test links stopped working after the maintenance. What occurred?**

-   After the maintenance, test links will be changing to a new format
    to reflect the new datacenter. Please see test link table above.

 

**Related Topics**

-   [Important scheduled maintenance: DFW environment
    migration](http://rackspace.com/knowledge_center/article/important-scheduled-maintenance-dfw-environment-migration)
-   [Information for ASP.NET
    changes](http://rackspace.com/knowledge_center/article/information-for-aspnet-changes-0)
-   [Information for CRON
    changes](http://rackspace.com/knowledge_center/article/information-for-cron-changes)
-   [Information for Customer IPs &
    DNS](http://rackspace.com/knowledge_center/article/information-for-customer-ips-dns-0)
-   [Information for MS SQL
    changes](http://rackspace.com/knowledge_center/article/information-for-ms-sql-changes)
-   [Information for MySQL Users (MariaDB
    10.0)](http://rackspace.com/knowledge_center/article/information-for-mysql-users-mariadb-100-0)
-   [Information for new PHP 5.6 & Apache
    version](http://rackspace.com/knowledge_center/article/information-for-new-php-56-apache-version-0)


