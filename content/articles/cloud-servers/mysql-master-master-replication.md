---
node_id: 1119
title: MySQL Master-Master Replication
type: article
created_date: '2011-06-07 19:06:14'
created_by: RackKCAdmin
last_modified_date: '2016-01-14 15:4615'
last_modified_by: kyle.laffoon
product: Cloud Servers
body_format: tinymce
---

undefined&rsquo;s create the replication user, which will be used to
    synchronize the changes.

<!-- -->

     
    mysql> grant replication slave on *.* to slaveuser@'[private IP of debian502]' identified by '[some password]';
    mysql> flush privileges;
    mysql> exit

-   Do the same for debian502

<!-- -->

     
    mysql> grant replication slave on *.* to slaveuser@'[private IP of debian501]' identified by '[some password]';
    mysql> flush privileges;
    mysql> exit

-   Back on debian501, edit */etc/mysql/my.cnf* and insert/update or
    uncomment following entries:

<!-- -->

     
    bind-address = 0.0.0.0
    server-id = 1
    log-bin = /var/log/mysql/var/bin.log
    log-slave-updates
    log-bin-index = /var/log/mysql/log-bin.index
    log-error = /var/log/mysql/error.log
     
    relay-log = /var/log/mysql/relay.log
    relay-log-info-file = /var/log/mysql/relay-log.info
    relay-log-index = /var/log/mysql/relay-log.index
     
    auto_increment_increment = 10
    auto_increment_offset = 1
    master-host = [private IP address of debian502]
    master-user = [replication username]
    master-password = [replication password]
     
    replicate-do-db = <database name to be replicated>

-   Repeat the steps on the debian502 server

<!-- -->

     
    bind-address = 0.0.0.0
    server-id = 2
    log-bin = /var/log/mysql/bin.log
    log-slave-updates
    log-bin-index = /var/log/mysql/log-bin.index
    log-error = /var/log/mysql/error.log
     
    relay-log = /var/log/mysql/relay.log
    relay-log-info-file = /var/log/mysql/relay-log.info
    relay-log-index = /var/log/mysql/relay-log.index
     
    auto_increment_increment = 10
    auto_increment_offset = 2
    master-host =  [private IP address of debian501]
    master-user = [replication username]
    master-password = [replication user password]
     
    replicate-do-db = [database name to be replicated]

-   Now, restart both databases. If the service restart on either server
    fails, then please check the */var/log/mysql/error.log* file for any
    errors. Update the configuration and check for any typos, etc.,

 

Testing the scenarios
---------------------

For the purpose of testing our replication setup, we can create the
database specified in the configuration section above (replicate-do-db),
as well as a test table on one of the nodes and watch the log files in
/var/log/mysql directory. Note that all database changes should be
replicated to our other server immediately.

     
    mysql> create database [your-db-name];
    mysql> use [your-db-name]
    mysql> create table foo (id int not null, username varchar(30) not null);
    mysql> insert into foo values (1, 'bar');

-   An additional test is to stop the MySQL service on debian502, making
    database changes on the debian501 server and then restarting the
    MySQL service on debian502. The debian502 MySQL service should sync
    up all the new changes automatically.

-   You should also consider changing the default binary log rotation
    values (expire\_logs\_days and max\_binlog\_size) in the
    /etc/mysql/my.cnf file, as by default all the binary logs will be
    kept for 10 days. If you have high transaction count on your
    database application then it can cause significant hard disk space
    usage in logs. So, we recommend changing those values to match your
    server backup policies. For example, if you have daily backups setup
    of your MySQL node then it makes no sense to keep 10 days worth of
    binary logs.


