---
node_id: 1504
title: Importing data into Cloud Databases
permalink: article/importing-data
type: article
created_date: '2012-07-24 00:29:31'
created_by: RackKCAdmin
last_modified_date: '2016-01-06 17:1240'
last_modified_by: cat.lookabaugh
products: Cloud Databases
body_format: tinymce
---

This article describes how to import the data of an existing MySQL
database into a Cloud Database. If you haven't already created a Cloud
Database instance and an empty database to receive the imported data,
you will need to do that first.

The import process includes the following steps:

1.  Use the [Cloud Control Panel](http://mycloud.rackspace.com) to
    create a Cloud Database instance with an empty database and a
    username and password to access it.
2.  When the database instance is created, click on it and take note of
    the Hostname. You'll use it in a later step. The Hostname looks
    something like this:

![Database
Hostname](http://c691244.r44.cf2.rackcdn.com/Hostname%20of%20Database.png)

3.  On the machine where your existing database is currently located,
    run the following MySQL command to export your database:

<!-- -->

    mysqldump -u username -p database_name > database_name.sql

database\_name is the name of your existing datatabase.
database\_name.sql will be the name of the exported database file.
 Replace "username" with the username you use to access the original
database.

4.  Using SFTP, copy the exported .sql file to the Cloud Server that
    will access your Cloud Database.
5.  With the .sql file copied to your Cloud Server, use ssh to log into
    the server.
6.  If you don't have a mysql client installed on your server, install
    it now.

On Ubuntu and Debian, install the client with the following command:

    sudo apt-get install mysql-client

On Fedora and CentOS, install the client with this command:

    sudo yum install mysql

7.  Run the following MySQL import command, substituting that long
    hostname you copied from the control panel for the address in the
    command, your database username for "username", and your database
    name for "database\_name":

<!-- -->

    mysql -h 31blah2d.rackspaceclouddb.com -u username -p database_name < database_name.sql

The database is imported and ready to accept new data.

### External Links

[MYSQL Documentation](http://dev.mysql.com/doc/)

