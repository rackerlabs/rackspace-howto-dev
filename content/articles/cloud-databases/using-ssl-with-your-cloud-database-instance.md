---
node_id: 4281
title: Using SSL with your Cloud Database instance
type: article
created_date: '2014-10-02 16:01:44'
created_by: neha.verma
last_modified_date: '2014-10-17 20:5948'
last_modified_by: jered.heeschen
products: Cloud Databases
body_format: tinymce
---

undefined&mdash;ssl-ca=/path/to/ca-cert.pem

More information about using SSL with MySQL can be found in the [MySQL
5.6
documentation](http://dev.mysql.com/doc/refman/5.6/en/using-ssl-connections.html).

Require SSL connections
-----------------------

You can also set up restrictions on a user to require SSL when
communicating with the database. MySQL supports the `GRANT` statement
modifier `REQUIRE SSL`. For example, to restrict `database_user` to have
read, write, and delete permissions for `prod_database` only when
connected with an SSL connection, log in to MySQL as root and then issue
the following command.

    GRANT SELECT, INSERT, UPDATE, DELETE ON prod_database.* TO 'database_user'@'%' REQUIRE SSL;

**Note:** If the user already exists, you must revoke all existing
privileges for the user and then use the preceding `GRANT` statement to
give the appropriate privileges to the user.

Remember to run a `FLUSH PRIVILEGES` for the database to make the
privilege change take effect.

