---
node_id: 668
title: 'I scheduled my cron job, but I haven’t received any email confirmation. Did my task run correctly?'
type: article
created_date: '2011-03-16'
created_by: Rackspace Support
last_modified_date: '2013-08-19'
last_modified_by: Matt Wheeler
product: Cloud Sites
body_format: tinymce
---

There are several reasons why you may not have recieved email
confirmation that your cron job completed successfully. Here are a few
things to check:

1\. Please confirm that you entered in your email address correctly
within the control panel. If so, please also check your "Junk Folder" to
make sure that the email notification was not delivered there
accidentally.

2\. There is the chance that your scrip may not work correctly. Check to
make sure that your script has no errors and has been tested and
performs as expected.

3\. For your script to be readable, the file permissions should be
appropriately set. Make sure that you set file permissions to at least
644.

4\. Is the path to the script correct? Note that the leading slash is not
required and your top-level domain directory is automatically appended
to the path.

5\. You can navigate through FTP to your /logs directory. Here you can
access your task log which will list any errors, or confirmation that
the cron job did run.


If you have any other questions on scheduling a task, please do not
hesitate to contact our support team.

