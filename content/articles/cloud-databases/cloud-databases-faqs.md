---
node_id: 5026
title: Cloud Databases - FAQ
type: article
created_date: '2015-12-10'
created_by: Rackspace Support
last_modified_date: '2016-01-15'
last_modified_by: Stephanie Fillmon
product: Cloud Databases
body_format: tinymce
---

- Getting Started -
-------------------

### Can I provision Cloud Databases if I don't have Cloud Servers, Cloud Load Balancers, or Cloud Sites on my account?

Yes, but instances are provisioned only with network interfaces on their
data center's internal service network (ServiceNet). Connecting to a
Cloud Database instance remotely requires either a Cloud Server or Cloud
Load Balancer to [proxy the
connection](/howto/connect-to-a-cloud-databases-instance).

^[back\\ to\\ top](#top)^

### What kind of storage solution does Cloud Databases offer?

Each Cloud Database instance comes with an attached storage volume.
Storage volumes are automatically provisioned on a shared Internet Small
Computer System Interface (iSCSI) storage area network (SAN) that
provides for increased performance, scalability, availability, and
manageability. Applications with high I/O demands are
performance-optimized and data is protected through both local and
network RAID-10. Additionally, network RAID provides synchronous
replication of volumes with automatic failover and load balancing across
available storage clusters.

^[back\\ to\\ top](#top)^

### How is performance better than running a MySQL database on a Cloud Server?

Every Cloud Databases instance is optimized for performance. Cloud
Databases uses container-based virtualization, which eliminates the
performance bottlenecks of the traditional hardware virtualization and
enables your database to run at near bare metal speeds. It also uses
dedicated SAN storage and high speed networking to give you faster
access to your data.

^[back\\ to\\ top](#top)^

### What is Cloud Databases?

Cloud Databases is a stand-alone, API-based, relational database service
built on OpenStack&reg; cloud that allows Rackspace customers to easily
provision and manage multiple MySQL database instances. Instances are
provisioned in a single-tenant, container-based environment per account
and are accessible via the Rackspace internal ServiceNet network. Each
database instance is optimized for performance. You can run a database
instance with MySQL, Percona, or MariaDB as the database technology.

^[back\\ to\\ top](#top)^

### What are the benefits of using Cloud Databases?

Cloud Databases provides a complete solution for customers demanding a
high-performance, purpose-built infrastructure designed for relational
databases backed and supported by engineers who specialize in MySQL
workloads. Cloud Databases is a fully managed service for customers who
want to focus on developing their applications and not worry about the
underlying infrastructure. The service offers on demand backups and
restores, integrated monitoring, redundant storage, scalability to grow
based on your application needs, and full control of your database.

^[back\\ to\\ top](#top)^

### What instance sizes do you currently support?

For the most up-to-date information about available instance sizes, see
the [Cloud Databases website](http://www.rackspace.com/cloud/databases/)
or the "[List
Flavors](http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/GET_getFlavors__version___accountId__flavors_flavors.html)"
[section](http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/GET_getFlavors__version___accountId__flavors_flavors.html)
of the Cloud Databases Developer Guide.

^[back\\ to\\ top](#top)^

### What types of Rackspace products / accounts can use Cloud Databases?

Any US or UK customer with a Cloud account will be able to provision
multiple ServiceNet database instances, manage multiple databases and
users (within resource limits). This service is also available to
RackConnected Cloud Servers. Both First and Open Cloud Servers can
connect to Cloud Databases, as well as any product with access to our
internal ServiceNet network within the same regional datacenter.

^[back\\ to\\ top](#top)^

### Can Cloud Databases be used with Dedicated servers?

No, Cloud Databases are available only to customers with Cloud account
credentials. Managed Operations Service Level or Dedicated customers
with RackConnect (that is those customers who also have a Cloud account)
have access, but can use the service only with their Rackspace Cloud
product resources.

^[back\\ to\\ top](#top)^

### Is Cloud Databases available in the Control Panel?

Yes. Click **Databases** in the [Cloud Control
Panel](http://mycloud.rackspace.com/). Connecting to a Cloud Database
instance remotely requires either a Cloud Server or Cloud Load Balancer
to [proxy the
connection](/howto/connect-to-a-cloud-databases-instance).

^[back\\ to\\ top](#top)^

------------------------------------------------------------------------

Account Services
----------------

### Does Cloud Databases support SSL for communication between my application and my database instance?

Yes, Cloud Databases supports connecting to your instance using SSL. An
SSL certificate is installed for each Cloud Databases instance that
enables a secure connection between your application and the instance.
When an SSL connection is established, any data transfer between the
instance and application is encrypted.

^[back\\ to\\ top](#top)^

------------------------------------------------------------------------

Backups
-------

### Can I write to my database instance during a backup?

The behavior of your instance during a backup depends on the storage
engine that you are using for tables. If you use only InnoDB, write
access to your database instance is not suspended. Conversely, if you
have MyISAM tables, those databases are write-locked during the backup
process.

^[back\\ to\\ top](#top)^

### What storage engines do you support for database backups?

MySQL supports several types of table engines, also know as *table
types*. The tables on a Cloud Databases instance can use a mix of
different table engine types or they can all use the same type.
Currently we support backups of databases that use InnoDB and MyISAM.

^[back\\ to\\ top](#top)^

### How much do you charge for database backups?

Backups are stored in your Cloud Files account, and you are charged for
storage used. Standard rates for Cloud Files storage apply. For current
costs, see the [Cloud Files pricing
page](http://www.rackspace.com/cloud/files/pricing/).

^[back\\ to\\ top](#top)^

### How do you perform database backups?

Backups are created by using Percona XtraBackup to perform a hot copy of
all databases on an instance. The resulting database files are streamed
directly to your Cloud Files account for storage.

^[back\\ to\\ top](#top)^

### Do you provide database backup and restore features?

Manual backup and restore operations are currently supported from within
the Control Panel. For more information, please read the article
[Managing Backups for Cloud
Databases](/howto/managing-backups-for-cloud-databases).
Alternately you can manage backup operations[via the Cloud Databases
API](http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/backups.html),
or by using the [Trove command line tool
(CLI)](http://docs.rackspace.com/cdb/api/v1.0/cdb-getting-started/content/Install_Trove_Client.html).

Although Cloud Databases provides built-in data replication, as a best
practice, we encourage our Cloud customers to back up their data using
MySQL tools like mysqldump. Managed Operations Service Level customers
can request assistance with backups from their support team.

^[back\\ to\\ top](#top)^

### How long does a database backup take?

The duration of the backup will depend on the size of your databases and
any network saturation during the backup.

^[back\\ to\\ top](#top)^

### How do I restore a database backup?

To restore a database backup, you must create a new database instance,
specifying the backup that you want to restore during the create
request. Your backup is loaded to the new instance, and you will receive
a DNS endpoint for the new instance. After the restore operation is
complete, you can update your application to use the new endpoint.

The original instance is not altered during a restore operation and may
remain in use or be deleted through the API, CLI, or Control Panel.

^[back\\ to\\ top](#top)^

### How many database backups can I request?

There are no limits on how many database backups you can create. Note
that you can run only one backup at a time; duplicate requests result in
a 422 error.

^[back\\ to\\ top](#top)^

### When a Cloud Database is deleted how is the data removed?

Cloud databases run off of SAN storage using a mount point. Once an
instance is deleted, the mount point is destroyed.

### Are database backups deleted when a database is deleted?

Backups are not deleted when an instance is deleted. You must manually
remove any stored backups.

------------------------------------------------------------------------

Monitoring and Troubleshooting
------------------------------

### What Cloud Databases operations are supported at different service levels?

Support coverage information for Managed Infrastructure and Managed
Operations Service Level is available on [the Cloud Databases support
matrix page](http://www.rackspace.com/cloud/databases/support/).

^[back\\ to\\ top](#top)^

### Where can I find the Cloud SLA?

The [Cloud service level agreement
(SLA)](http://www.rackspace.com/information/legal/cloud/sla) on the
Rackspace website.

^[back\\ to\\ top](#top)^

### How can I monitor my resource use on Cloud Databases?

Monitoring is available for all Cloud Databases instances through
pre-configured Cloud Monitoring checks, including load average, CPU,
memory, disk storage, network, and a number of MySQL metrics. You can
monitor your Cloud Databases instances using the[Cloud Control
Panel](/howto/monitoring-cloud-databases-in-the-cloud-control-panel),
the[Cloud Monitoring
API](http://docs.rackspace.com/cm/api/v1.0/cm-getting-started/content/Introduction.html),
or the [Cloud Monitoring command-line
tool](/howto/getting-started-with-rackspace-monitoring-cli).

You can also set up alarms to send you email alerts based on thresholds
you define. An alert for disk space is set up by default for every
instance. You can also use our [Cloud Intelligence beta
site](https://intelligence.rackspace.com/) to observe usage patterns or
any unexpected changes in your environment.

^[back\\ to\\ top](#top)^

### Can I create a Cloud Databases support ticket?

Yes. A Cloud Databases support ticket category is available in the
[Cloud Control Panel](https://mycloud.rackspace.com/).

^[back\\ to\\ top](#top)^

------------------------------------------------------------------------

Databases
---------

### What are the differences between InnoDB and MyISAM?

InnoDB is the default storage engine for Cloud Databases. InnoDB
enforces ACID transactions allowing for commit, rollback, and crash
recovery capabilities to protect user data.

During a backup, a hot copy process is used on all tables. InnoDB tables
record all transactions during the copy in order to replay them during a
restore operation.

MyISAM tables are write-locked during the copy process in order to
create a consistent backup. While the instance is being backed up you
cannot add or delete databases, add or delete users, or delete, stop, or
reboot the instance.

For more information about these engine types, see the MySQL
documentation:

-   [InnoDB Storage Engine
    documentation](http://dev.mysql.com/doc/refman/5.1/en/innodb-storage-engine.html)
-   [MyISAM Storage Engine
    documentation](http://dev.mysql.com/doc/refman/5.1/en/myisam-storage-engine.html)



^[back\\ to\\ top](#top)^

### How many connections does each database instance size support?

Details about maximum connections and access to my.cnf file settings per
database size are listed in the following table:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Size</strong></p></td>
<td align="left"><p><strong>Max connections</strong></p></td>
<td align="left"><p><strong>Max User Connections</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>512 MB</p></td>
<td align="left"><p>50</p></td>
<td align="left"><p>40</p></td>
</tr>
<tr class="odd">
<td align="left"><p>1 GB</p></td>
<td align="left"><p>110</p></td>
<td align="left"><p>100</p></td>
</tr>
<tr class="even">
<td align="left"><p>2 GB</p></td>
<td align="left"><p>210</p></td>
<td align="left"><p>200</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4 GB</p></td>
<td align="left"><p>410</p></td>
<td align="left"><p>400</p></td>
</tr>
<tr class="even">
<td align="left"><p>8 GB</p></td>
<td align="left"><p>810</p></td>
<td align="left"><p>800</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16 GB</p></td>
<td align="left"><p>1610</p></td>
<td align="left"><p>1600</p></td>
</tr>
<tr class="even">
<td align="left"><p>32 GB</p></td>
<td align="left"><p>3210</p></td>
<td align="left"><p>3200</p></td>
</tr>
<tr class="odd">
<td align="left"><p>64 GB</p></td>
<td align="left"><p>6410</p></td>
<td align="left"><p>6400</p></td>
</tr>
</tbody>
</table>

^[back\\ to\\ top](#top)^

### What is the maximum scalable capacity of a Cloud Database instance?

Instances can be provisioned with up to 64GB of memory and up to 500GB
of disk storage. You can increase storage up to the maximum using the
[Cloud Control Panel](https://mycloud.rackspace.com/). Note that disk
storage cannot be decreased on a running instance.

^[back\\ to\\ top](#top)^

### Can I set up a read-only MySQL user in Cloud Databases?

Yes, but by default all users created through the Control Panel, API,
and command line interface (CLI) have full permissions.

To create read-only users, you first must enable the root user and use
that user to generate and manage additional users with read-only
privileges.

^[back\\ to\\ top](#top)^

### Can I enable a root (super) user?

Yes. Currently, the root user can only be enabled via the public API or
command line interface (CLI). We do plan to integrate this feature into
the Cloud Control Panel at a later date.

Once root is enabled, it cannot be disabled.

^[back\\ to\\ top](#top)^

### What versions of MySQL do you offer?

Cloud Databases supports MySQL 5.6, Percona 5.6 and MariaDB 10. For all
newly created Cloud Database instances, MySQL 5.6 is the default. We
will continue to support MySQL 5.1 for legacy instances, but we
recommend our customers use the latest version of MySQL, Percona, or
MariaDB because they offer significant performance improvements and
newer features. For more information to help you choose the right
database version for your application, see [Choosing the right data
store](/howto/choosing-the-right-database-with-rackspace-cloud-databases).

^[back\\ to\\ top](#top)^

### What bandwidth limitations are enforced on the ServiceNet network?

The following table shows bandwidth, in megabits per second (Mbps),
based on instance size.

**Instance Size**

**Bandwidth**

512 MB

20 Mbps

1 GB

100 Mbps

2 GB

200 Mbps

4 GB

300 Mbps

8 GB

400 Mbps

16 GB

500 Mbps

32GB

1000 Mbps

64GB

2000 Mbps

^[back\\ to\\ top](#top)^

### Where can I find the Cloud Databases documentation?

Release notes, API documentation, and a getting started guide for Cloud
Databases are all available on the Rackspace [API Documentation
site](http://docs.rackspace.com/api/).

^[back\\ to\\ top](#top)^

### Are there API or account limits for my Cloud Database instances?

Yes. All accounts, by default, have a preconfigured set of thresholds
(or limits) to manage capacity and prevent abuse of the system. The
system recognizes two kinds of limits: rate limits and absolute limits.
Rate limits are thresholds that are reset after a certain amount of time
passes. Absolute limits are fixed at the account level. For the most
up-to-date information about rate and absolute limits (which include
instance and volume limits), see the Limits section in the [Rackspace
Cloud Databases Developer Guide](http://docs.rackspace.com/).

^[back\\ to\\ top](#top)^

### If my database instance is unavailable, what happens to my data?

If you cannot access your Cloud Databases instance, your data is still
protected on a redundant SAN.

^[back\\ to\\ top](#top)^

### How can I access my database instance?

Cloud Databases provides several options for connecting to your
database, giving you complete flexibility in how you access your
database. For increased security, your database is available only on the
Rackspace private network by default. However, you can connect to your
database by using several methods described at the following links:

[Public Vs. Private
Access](/howto/public-and-private-access-for-cloud-databases)

[Connecting to Your
Database](/howto/connect-to-a-cloud-databases-instance)

Additionally, you can use the Cloud Control Panel, API, or command line
interface (CLI) to manage your database instance. Some of the features
are not available in the Control Panel but can be accessed through API
or through the CLI. More information about the API and CLI is located in
the [Cloud Databases API documentation](http://docs.rackspace.com/), in
both the API developers guide and the getting started guide.

^[back\\ to\\ top](#top)^

### How do I set the default time zone for MySQL?

You can set the default time zone for a Cloud Databases instance of
MySQL by creating a configuration group that sets the
default\_time\_zone parameter to the offset from UTC (for example,
"-6:00" for CST).

For more information, see [Setting the time zone for a Cloud Databases
instance](/howto/setting-the-time-zone-for-a-cloud-databases-instance).

^[back\\ to\\ top](#top)^

### Do you support importing and exporting data into the database?

You can use standard MySQL client tools to import data into and export
data from your instance. Knowledge Center articles that detail the
processes
of [importing](/howto/importing-data-into-cloud-databases)
or
[exporting](/howto/exporting-data-from-mysql)
data are available.

^[back\\ to\\ top](#top)^

### Do you support MySQL configuration (my.cnf) file modifications?

Yes. Configuration settings for Cloud Databases instances can be stored
and applied using the[Cloud Control
Panel](https://mycloud.rackspace.com/) and the [Cloud Databases
API](http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/overview.html).
You can save your settings in configuration groups, and each
configuration group can be applied to multiple instances. You can
maintain multiple configuration groups to account for different
workloads.

^[back\\ to\\ top](#top)^

### What level of access do I have to my database instance?

Access to MySQL is allowed only over port 3306; shell-level access is
not available. Full MySQL access can be obtained by enabling the root
user on the database instance.

^[back\\ to\\ top](#top)^

### What is the default database storage engine?

The default storage engine is InnoDB, but other storage engines included
with MySQL 5.1, such as MyISAM, also work for certain use cases.

^[back\\ to\\ top](#top)^

------------------------------------------------------------------------

High Availability
-----------------

### What is High Availability for Cloud Databases?

A Cloud Databases High Availability (HA) instance group includes a
source database instance with one or two replicas. If the source
database instance becomes unavailable, an automatic failover is
initiated to one of the replicas. The automatic failover and promotion
of the new instance is completed within a short downtime (approximately
10-30 seconds).

^[back\\ to\\ top](#top)^

### What flavors are supported for HA instance groups?

You can choose any flavor from 1 GB to 64 GB for provisioning an HA
instance group.

^[back\\ to\\ top](#top)^

### Can I create a backup of the High Availability instances?

Currently backups, resizes, and custom configurations cannot be
performed for instances that are part of the HA setup. Backups and
incremental backups can be created for the HA group rather than an
individual instance.

^[back\\ to\\ top](#top)^

### Can I resize the RAM for my HA instances?

Resizing is not currently supported for HA instances for Cloud
Databases. Rackspace will start supporting resizing for HA instances in
a future release.

^[back\\ to\\ top](#top)^

### What is the underlying technology for creating HA Cloud Databases instances?

Technical architecture details are provided in the [High Availability
for Cloud
Databases](/howto/high-availability-for-cloud-databases)
article.

^[back\\ to\\ top](#top)^

### Do HA instances support automatic failover?

Yes. Rackspace ensures that if the source database instance becomes
unavailable, an automatic failover is initiated to the replicas within
10-30 seconds of downtime.

^[back\\ to\\ top](#top)^

### What is the pricing for HA instances for Cloud Databases?

For the product introduction, Rackspace is charging the same price for
HA instances as for single instances for a limited time. In the future,
there will be an increase in the price of HA instances.

^[back\\ to\\ top](#top)^

### Which databases are supported for HA instances for Cloud Databases?

Rackspace currently supports MySQL 5.6, Percona 5.6, and MariaDB 10 for
HA database instances.

^[back\\ to\\ top](#top)^

### How many replicas can I add to the HA group?

You can add a maximum of two replicas to the primary source database
instance. So you can have a maximum of three instances in the HA group,
one primary and two replicas. In the future, we will increase the number
of replicas that can be added to the HA group.

^[back\\ to\\ top](#top)^

### Where can I find more technical details about High Availability (HA)?

See the article [High Availability for Cloud
Databases](/howto/high-availability-for-cloud-databases).

^[back\\ to\\ top](#top)^

------------------------------------------------------------------------

Replication
-----------

### Can I monitor replication?

Yes. You can monitor replication using the monitoring agent installed on
the instance. For more information, see [Monitoring Read
Replication](http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/Monitoring_Read_Replication-d1e3694.html)
in the API documentation.

^[back\\ to\\ top](#top)^

### Is replication supported between different versions of the database?

No. You can only add replica of the same database type and version as
your source database instance.

^[back\\ to\\ top](#top)^

### Is replication supported between different regions?

No. You can only add a replica in the same region as your source
database instance.

^[back\\ to\\ top](#top)^

### Does setting up replication require downtime?

When you add a replica to the source DB instance, the instance gets
restarted. So your database will be unavailable until the instance
restarts.

^[back\\ to\\ top](#top)^

### Is there a charge for replication?

Each read replica added is charged the same way as a new instance.

^[back\\ to\\ top](#top)^

### Does replication support auto failover?

Currently replication does not support auto failover. In case your
database instance goes down and you would like to use replica instance
for minimizing downtime, you will have to do a manual failover to the
replica instances. For manual failover, you must detach the replica from
the source instance and change the application endpoint to this new
source database instance.

^[back\\ to\\ top](#top)^

### Is replication supported for all database types?

Replication is supported for MySQL 5.6, Percona 5.6, and MariaDB 10. We
do not support replication for MySQL 5.1 as this is an older version of
MySQL and there have been significant improvements for replication
support in newer versions of MySQL. We highly recommend all users to
[upgrade from MySQL 5.1 to MySQL
5.6](/howto/upgrade-a-cloud-databases-instance-from-mysql-51-to-mysql-56).

^[back\\ to\\ top](#top)^

### Do you support replication?

Yes we do support Master Slave Replication. You can add and manage
replicas using [Cloud Control Panel](https://mycloud.rackspace.com/) and
Cloud Databases API. For more information about managing replication
with API, see [API docs for
replication](http://docs.rackspace.com/cdb/api/v1.0/cdb-devguide/content/Replication-Overview-dle5733.html).

^[back\\ to\\ top](#top)^

------------------------------------------------------------------------

Billing
-------

### How much does Cloud Databases cost?

Pricing information is available at [the Cloud Databases pricing
page](http://www.rackspace.com/cloud/databases/pricing/). Standard
charges apply for any Cloud Servers, Cloud Load Balancers, or Cloud
Sites that are used to access your Cloud Database instances.

^[back\\ to\\ top](#top)^

