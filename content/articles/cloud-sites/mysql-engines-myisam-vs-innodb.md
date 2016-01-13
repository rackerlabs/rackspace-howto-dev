---
node_id: 681
title: MySQL Engines - MyISAM vs Innodb
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-30 16:5659'
last_modified_by: stephanie.fillmon
products: Cloud Sites
body_format: tinymce
---

MySQL supports several different types of Table Engines also known as
"Table Types". A database can have its tables being a mix of different
table engine types or all of the same type. Here is more information on
each of the different types of table engines that MySQL offers:

[http://dev.mysql.com/doc/refman/5.0/en/storage-engines.html](http://dev.mysql.com/doc/refman/5.0/en/storage-engines.html "http://dev.mysql.com/doc/refman/5.0/en/storage-engines.html")

The two most commonly used on most [Cloud Sites MySQL
servers](http://www.rackspace.com/cloud/sites/web-hosting/mysql/) use **Innodb**
and **MyISAM** engines.

The purpose of this document is to briefly cover the two types and
identify which ones are more recommended under what circumstances in the
Cloud Sites environment. Please note that the purpose of this document
is however not to go over a performance comparison of each of the two
engine types as far as comparing via running specific sql test
benchmarks, which if you are interested are well done on the two links
below:

[http://www.mysqlperformanceblog.com/2007/01/08/innodb-vs-myisam-vs-falcon-benchmarks-part-1/](http://www.mysqlperformanceblog.com/2007/01/08/innodb-vs-myisam-vs-falcon-benchmarks-part-1/ "http://www.mysqlperformanceblog.com/2007/01/08/innodb-vs-myisam-vs-falcon-benchmarks-part-1/")

[http://tag1consulting.com/MySQL\_Engines\_MyISAM\_vs\_InnoDB\#comment-115](http://tag1consulting.com/MySQL_Engines_MyISAM_vs_InnoDB#comment-115 "http://tag1consulting.com/MySQL_Engines_MyISAM_vs_InnoDB#comment-115")

MyISAM is the default table engine type for MySQL 5.0 but the Cloud
Sites environment defaults the storage engine to Innodb. In other words
Cloud Sites is partial to Innodb if you do not explicity specify your
engine type in your table DDL. We have also tuned the database servers
to generally perform best with using the Innodb Engine type.

 

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 MyISAM vs Innodb - Quick comparison                               |
|     Table:](#MyISAM_vs_Innodb_-_Quick_comparison_Table:)                 |
| -   [2 When MyISAM tables are seen to be mostly                          |
|     useful?](#When_MyISAM_tables_are_seen_to_be_mostly_useful.3F)        |
| -   [3 When we have seen conversion of table engine from MyISAM to       |
|     Innodb as being most                                                 |
|     beneficial?](#When_we_have_seen_conversion_of_table_engine_from_MyIS |
| AM_to_Innodb_as_being_most_beneficial.3F)                                |
| -   [4 How to change your table Engine type from MyISAM to               |
|     Innodb?](#How_to_change_your_table_Engine_type_from_MyISAM_to_Innodb |
| .3F)                                                                     |
+--------------------------------------------------------------------------+

MyISAM vs Innodb - Quick comparison Table:
------------------------------------------

MyISAM

Innodb

Not \*ACID compliant and non-transactional

\*ACID compliant and hence fully transactional with ROLLBACK and COMMIT
and support for Foreign Keys

MySQL 5.0 Default Engine

Rackspace Cloud Default Engine

Offers Compression

Offers Compression

Requires full repair/rebuild of indexes/tables

Auto recovery from crash via replay of logs

Changed Db pages written to disk instantly

Dirty pages converted from random to sequential before commit and flush
to disk

No ordering in storage of data

Row data stored in pages in PK order

Table level locking

Row level locking

-   ACID - Atomicity, Consistency, Isolation, Durability (read more on
    it here:
    [http://en.wikipedia.org/wiki/ACID](http://en.wikipedia.org/wiki/ACID "http://en.wikipedia.org/wiki/ACID"))

\
 If you need to see further details on each of the two engine types,
please refer to the following MySQL documentations:

-   Innodb Storage Engine:
    [http://dev.mysql.com/doc/refman/5.0/en/innodb-storage-engine.html](http://dev.mysql.com/doc/refman/5.0/en/innodb-storage-engine.html "http://dev.mysql.com/doc/refman/5.0/en/innodb-storage-engine.html")
-   MyISAM Storage Engine:
    [http://dev.mysql.com/doc/refman/5.0/en/myisam-storage-engine.html](http://dev.mysql.com/doc/refman/5.0/en/myisam-storage-engine.html "http://dev.mysql.com/doc/refman/5.0/en/myisam-storage-engine.html")

 

When MyISAM tables are seen to be mostly useful?
------------------------------------------------

There can be several other reasons that fit your requirement for
choosing the MyISAM engine. For example reads can be faster on MyISAM vs
Innodb despite what the general claims on the above two links when
MyISAM table has fixed (not dynamic) row size i.e. when it uses more
CHARs for example versus VARCHARs. Still there could be other reasons
besides this why you choose or have chosen MyISAM over Innodb. Another
reason why you may have chosen MyISAM over Innodb is perhaps due to the
fact that Innodb must perform additional checks owing to its ACID
compliant nature - so for example a FK check needs to be checked which
could potentially cause an operational overhead. Unless you have
benchmarked this to be the case, I would not recommend you believing
this to be the case as default as per the links above, you may find out
otherwise.

 

When we have seen conversion of table engine from MyISAM to Innodb as being most beneficial?
--------------------------------------------------------------------------------------------

1.  If you need ACID compliance and need your db to be transactional
    then choosing Innodb is an obvious choice and you ought to make the
    necessary conversion including adding any FK constraints, etc if you
    need them.
2.  If you are not disproportionately read-only heavy and are doing a
    mix of reads (not requiring full text indexing) and writes then we
    do recommend that you go with Innodb.
3.  Most commonly we have observed that MyISAM tables would rather be
    converted to Innodb when you face frequent table lock escalations
    for long periods of time.
4.  If a read is slow or hasn't completed and a read/write is waiting on
    the first read to finish then the MyISAM table referenced in the
    read is held in a locked state till the resultset is made available
    to the query. This also causes a rise in the load average on the
    server and slows your site down. During this time no reads or writes
    can complete ofcourse as MyISAM only has table-level locking.

So to summarize, the queries that are victims of lock escalations under
heavy but slow reads would do much better as a table converted to
Innodb.

 

How to change your table Engine type from MyISAM to Innodb?
-----------------------------------------------------------

You do so by simply issuing the "ALTER TABLE" DDL statement:

    ALTER TABLE <table-name> ENGINE=INNODB;

Below is a step by step process for altering a table in PHPMyAdmin:

![DB\_article.png](http://c0935082.cdn.cloudfiles.rackspacecloud.com/DB_article.png)

1.  Log into the PHPMyAdmin utility through your control panel. If you
    are unsure how, please see [Working with a MySQL
    database](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-sites-essentials-phpmyadmin-database-management-interface "/knowledge_center/index.php/Working_with_a_MySQL_database")
    for instruction on how to login to PHPMyAdmin.
2.  Select the database which contains the **Table-Name**
3.  Click on the SQL tab
4.  Paste in the query provided above. Be sure to replace **table-name**
    with the correct name of your table
5.  Click the **GO** button.

**Note:** A MyISAM table that is using FULL TEXT Indexing can not be
converted to an Innodb Table Engine type.

