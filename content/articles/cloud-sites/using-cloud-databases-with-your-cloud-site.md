---
node_id: 1869
title: Using Cloud Databases with your Cloud Site
type: article
created_date: '2012-08-01 19:30:50'
created_by: chris.farmer
last_modified_date: '2014-11-13 16:5513'
last_modified_by: David Hendler
product: Cloud Sites
body_format: tinymce
---

undefined4. Connect your MySQL workbench by selecting OK and you can then import
your database, edit user permissions, etc.

###  

### Using your MySQL instance on your Cloud Site

In this last section, we're going to use Wordpress as an example;
however, the same concept applies to any CMS or application on your
website. All you need to do is plug in your database name, user name,
and your database host (this will be your MySQL instance hostname, not
your load balancer IP address, you do not need a load balancer to
connect to your database from your website) and you're good to go!

![](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/8.png)

There you have it! You've created a MySQL instance and database using
Cloud Databases, a Load Balancer to connect and manage your database,
and have connected that dedicated database to your Cloud Sites
application.

*Note: Cloud Sites will continue to offer the current shared MySQL
databases for you to consume, so you are not required to use Cloud
Databases. However, should you find that you need more dedicated
performance, security, and database management features, we highly
recommend using Cloud Databases to meet your DB needs. You can feel free
to consume both shared Cloud Sites databases as well as Cloud databases
as your hosting needs change. Please remember that all management and
updates to your Cloud Datbases must be done via the Cloud Control Panel,
and will not be integrated into the Cloud Sites Control Panel. This is
intentional, so you have access to the latest features when they go live
in the Cloud Control Panel.*

