---
node_id: 4132
title: Choosing the right database with Rackspace Cloud Databases
type: article
created_date: '2014-07-16'
created_by: Ross Diaz
last_modified_date: '2014-07-25'
last_modified_by: Rose Contreras
product: Cloud Databases
body_format: tinymce
---

Cloud Databases supports MySQL 5.6, Percona 5.6, and MariaDB 10.
Innovation is happening in each of these communities, and this article
highlights some of the key aspects to consider when choosing a MySQL
based datastore that best fits your application.

### MySQL

MySQL, an open-source database developed by Oracle, is the recommended
choice of the MySQL database administrator community, and is a good fit
for customers concerned about maintaining compatibility with upstream,
and who prefer a quick release schedule for upstream updates. MySQL 5.6
is the latest version that is in general availability (since February
2013). MySQL 5.6 offers great improvements in performance, InnoDB
scalability, transparency, and replication. For more information, see
the [MySQL documentation](http://dev.mysql.com).

### Percona server

Percona Server is a good solution for customers who want improved
performance right out of the box and want to maintain close (but not
exact) compatibility with the upstream source. It has many optimizer
improvements when compared to the upstream MySQL. Percona Server
includes XtraDB, a drop-in replacement for InnoDB with many
optimizations that improve performance on multicore systems. For more
information, see the [Percona Server
documentation](http://www.percona.com/software/percona-server).

### MariaDB

MariaDB was developed by many of the original developers of MySQL, and
has a long-term goal of maintaining compatibility with MySQL. It is a
good database choice for customers who are less concerned with
maintaining direct compatibility with upstream, and it offers the best
performance and features out of the box. It does not merge with code
provided by upstream, but attempts to re-implement features as they are
released, if they were not already provided. MariaDB contains the best
optimizer performance of all three solutions and has the largest
selection of storage engines by default. For more information, see the
[MariaDB documentation](https://mariadb.org/en/about/).

The following table displays the major features and differences among
MySQL, Percona Server, and MariaDB 10.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"> </th>
<th align="left">MySQL 5.6</th>
<th align="left">Percona Server 5.6</th>
<th align="left">MariaDB 10</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Pros</strong></p></td>
<td align="left"><p>Upstream controlled by Oracle</p></td>
<td align="left"><ul>
<li><p>Drop-in replacement for MySQL</p></li>
<li><p>Remerges with upstream source code after each new MySQL release, to maintain compatibility</p></li>
<li><p>Includes community patching</p></li>
<li><p>Improved performance on multiprocessor systems</p></li>
<li><p>Improved query optimizer</p></li>
<li><p>Increased log verbosity options, status and performance counters, and increased <code>INFORMATION_SCHEMA</code> content</p></li>
<li><p>Thread pool option without the need for Enterprise MySQL</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Drop-in replacement for MySQL</p></li>
<li><p>Re-implements features as they are released by Oracle</p></li>
<li><p>Fork of MySQL with many new features and a long-term goal to maintain binary compatibility</p></li>
<li><p>Includes community patching</p></li>
<li><p>Improved performance on multiprocessor systems</p></li>
<li><p>Improved query optimizer</p></li>
<li><p>Increased log verbosity options, status and performance counters, and increased <code>INFORMATION_SCHEMA</code> content</p></li>
<li><p>Thread pool option without the need of Enterprise MySQL</p></li>
<li><p>Increased Quantity of Storage Engines by default</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cons</strong></p></td>
<td align="left"><p>Bug fixes are delayed behind forks that might have already been resolved by community patches</p></td>
<td align="left"><p>After using features specific to Percona, you might not be able to directly roll back the database</p></td>
<td align="left"><ul>
<li><p>After using features specific to MariaDB, you might not be able to directly roll back the database</p></li>
<li><p>Started from MySQL upstream, but much of the MySQL source code has been directly modified</p></li>
<li><p>Inmany cases, upstream bugs are already resolved, but not in all cases and you might need to await re-implementation of the patch</p></li>
</ul></td>
</tr>
</tbody>
</table>



