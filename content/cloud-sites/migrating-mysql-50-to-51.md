---
node_id: 1393
title: Migrating MySQL 5.0 to 5.1
type: article
created_date: '2012-05-15'
created_by: Rackspace Support
last_modified_date: '2015-12-31'
last_modified_by: Stephanie Fillmon
product: Cloud Sites
product_url: cloud-sites
---

### Now available in Cloud Sites - MySQL 5.1!

Read on to learn the process of migrating your current Cloud Sites
running MySQL 5.0 to begin running on a MySQL 5.1 database.

Migrating your sites to a newer version of MySQL will require a
maintenance period during which your sites will be unavailable.  To
minimize the impact of the migration, you just need to plan ahead and
control the timing and presentation of your site during the process.Here
is an easy-to-follow, five-step process for migrating a MySQL 5.0
database to a MySQL 5.1 database:

### Step 1 - Close the Blinds and Lock the Doors

-   Begin by putting up a splash page on your site stating that you are
    currently migrating and then revoke all user access to the database
    to be migrated.  You can successfully revoke access to the database
    by using your administrative priveleges to rename the configuration
    file containing your database link information to a filename with
    the *.*`mig` extension.  An example would be naming the config.php
    file to config.php.mig.  Once the filename is changed wait for user
    transactions to be completed or kill them.  Threads can be killed
    with the `KILL` statement.  To learn more, consult the MySQL
    documentation from their website and see the section [KILL
    Syntax](http://dev.mysql.com/doc/refman/5.0/en/kill.html)<span
    class="s2">. </span> To determine if all user connections have been
    completed or successfully killed, use the command
    `SHOW FULL PROCESSLIST. `To learn more about this command, please
    consult the MySQL documentation from their website and look for the
    section [SHOW PROCESSLIST
    Syntax](http://dev.mysql.com/doc/refman/5.0/en/show-processlist.html).

### Step 2 - Back it Up!

-   Proceed to backing up your current MySQL 5.0 database.  You may wish
    to use the the process we describe in the Knowledge Center article:
    [How to backup your MySQL database with
    phpMyAdmin](/how-to/backup-your-mysql-database-with-phpmyadmin).

### Step 3 - Create Your New Database

-   You will next need to provision a new MySQL 5.1 database to contain
    the newly migrated database.  Do this by following the instructions
    in our Knowledge Center article: [Adding a MySQL
    Database](/how-to/rackspace-cloud-sites-essentials-mysql-databases).

### Step 4 - Import Your Saved DB Backup

-   The next step is to import your saved database backup into your
    newly provisioned MySQL 5.1 database. You should be able to use the
    [PHPmyAdmin Database Management
    Interface](/how-to/rackspace-cloud-sites-essentials-phpmyadmin-database-management-interface) to
    handle imports for databases which are less than 16MB in size
    without issue.  There may be times where you need to import more
    than 16MB of data, in which case you should follow the directions in
    the [Cloud Sites
    FAQ](/how-to/cloud-sites-faq).

### Step 5 - Update Your References

-   Finally, you will need to modify all references in your
    code/configuration files from the old database server host name, IP
    address, username, and password to the respective new locations and
    values on the newly provisioned and migrated database server.
    Rename the config file back to its original name without the *.mig*
    extension.  Assuming your new user information is valid, the site
    should begin processing against the new database in the same manner
    as before.


