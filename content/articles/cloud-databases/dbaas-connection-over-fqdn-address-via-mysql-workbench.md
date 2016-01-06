---
node_id: 1892
title: Connect to a cloud database with a FQDN Address via MySQL Workbench
permalink: article/dbaas-connection-over-fqdn-address-via-mysql-workbench
type: article
created_date: '2012-08-02 20:35:08'
created_by: Rae D. Cabello
last_modified_date: '2015-09-04 02:0911'
last_modified_by: constanze.kratel
products: Cloud Databases
body_format: tinymce
---

*Note: To complete this process, you will need both a cloud server and a
cloud database.*

Use the following steps to connect to Cloud Databases by using MySQL
Workbench.

1.  Go
    to [http://www.mysql.com/products/workbench/](http://www.mysql.com/products/workbench/)
    and install MySQL WorkBench.\
    The following platforms are supported: Windows, Fedora, Ubuntu,
    Oracle and Redhat, and Mac OS X. Registration is required before you
    download.
2.  Launch MySQL Workbench, and select the **New Server Instance**
    option under **Server Administration**.\
    \
    ![](/knowledge_center/sites/default/files/field/image/1.png)\
    \
3.  In the next screen, select the **Remote Host** option and enter the
    URL that was returned to you when you created the database instance
    and click **Continue**.\
    \
    ![](/knowledge_center/sites/default/files/field/image/2.png)\
    \
4.  On the next screen, from the **Connection Method** menu, select
    **Standard TCP/IP over SSH**.
5.  Change the value for **SSH HostName** to the name or ip address of a
    Cloud Server that you have created and that is in the same data
    center as the database instance. For example, if the database
    instance that you created is in the DFW data center, select a cloud
    server in the DFW data center.
6.  For S**SH Username**, enter the user name that you use to log in to
    the cloud server that you just specified.
7.  For **MySQL Hostname**, enter the host name that was returned when
    you created the database instance via the API.
8.  For **Username**, enter the username that was created when you
    created  the database instance.\
    \
    ![](/knowledge_center/sites/default/files/field/image/3.png)\
    \
9.  Click **Continue**. \
    You are prompted for the database instance password. If everything
    is correct, the following information is displayed:\
    \
    ![](/knowledge_center/sites/default/files/field/image/4.png)\
    \

After the database connection is tested, the following screen is
displayed. You can now work with your database instance.\
\
![](/knowledge_center/sites/default/files/field/image/5.png)\
\

*Note: If you did not save your password, when you perform any actions,
you will be prompted for the password to either the instance or the
server.*

