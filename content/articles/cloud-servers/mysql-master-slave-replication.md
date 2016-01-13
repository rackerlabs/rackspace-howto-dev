---
node_id: 1118
title: Set up MySQL master-slave replication
type: article
created_date: '2011-06-02 23:37:51'
created_by: RackKCAdmin
last_modified_date: '2015-08-27 13:3545'
last_modified_by: stephanie.fillmon
products: Cloud Servers
body_format: tinymce
---

undefined&ndash;on-master-status];
        mysql> START SLAVE;
        mysql> SHOW SLAVE STATUS\G

    The **Slave\_IO\_State** field should show "Waiting for master to
    send event". If it shows "Connecting to Master" please check your
    MySQL log file. By default it is (CODE)/var/log/mysqld.log(/CODE)
    but it may be configured differently on your system. As always
    (CODE)/etc/my.cnf(/CODE) will define the location of your log file.

 

### Test replication

To test the replication setup, create a new database and associated
table on db01, and insert data to confirm that the changes are mirrored
on db02. In the following example, the new database is called
**testing** and the new table is called **users**:

     
    # mysql -u root -p
    mysql> create database testing;
    mysql> use testing
    mysql> create table users(id int not null auto_increment, primary key(id), username varchar(30) not null);
    mysql> insert into users (username) values ('foo');
    mysql> insert into users (username) values ('bar');
    mysql> exit

The changes should be visible on db02 immediately.

