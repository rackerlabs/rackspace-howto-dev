---
node_id: 4065
title: Magento FAQ
type: article
created_date: '2014-05-07 16:01:13'
created_by: mike.hicklen
last_modified_date: '2014-12-17 16:0924'
last_modified_by: kyle.laffoon
products: Cloud Sites
body_format: tinymce
---

undefined&mdash;you can set up a cron job to re-index the cataloginventory\_stock
index every minute, 5 minutes, 10 minutes, or another frequency. Be sure
to set the frequency to something reasonable; you do not want cron jobs
running on top of each other, using too much CPU, and causing stress on
the MySQL database server.

### What other maintenance tasks can I do with the Magento shell scripts?

You can use the following script to clean logs:

`/usr/bin/php /var/www/vhosts/domain.tld/shell/log.php clean`

You also have the Magento Compiler, which can produce performance
benefits by reducing the number of include paths (four, by default) to
one include path. This change is useful if Magento is using too much
CPU, but you should use it with caution because the compiler tends to
not interact well with extensions.

Check the state in which the compiler currently resides by running the
following command:

     /usr/bin/php /var/www/vhosts/domain.tld/shell/compiler.php state

Use the following script to disable or enable the compiler, and run the
compile process:

    /usr/bin/php /var/www/vhosts/domain.tld/shell/compiler.php disable
    /usr/bin/php /var/www/vhosts/domain.tld/shell/compiler.php compile
    /usr/bin/php /var/www/vhosts/domain.tld/shell/compiler.php enable

### "An Error Log Record Number" doesn't tell me anything meaningful. Where can I find the actual error instead of just a number?

The number you get references a plain text file of the same name in your
Magento directory under **var/report/1234567890**. Look at the contents
of the file, which is easily readable with the **cat**command via SSH or
in a text editor. It can offer some insight into your issue.

