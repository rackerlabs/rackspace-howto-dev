---
node_id: 1139
title: How to Serve Multiple Domains Using Virtual Hosts
type: article
created_date: '2011-06-17 21:15:52'
created_by: RackKCAdmin
last_modified_date: '2015-12-31 14:4405'
last_modified_by: stephanie.fillmon
product: Cloud Servers
body_format: tinymce
---

undefined&rdquo; the log. For example:

    tail -f /var/log/httpd/error_log

### Common Permissions-Related Errors

To round off our exploration of common Apache configuration errors, here
are some examples of how some common permissions-related configuration
errors appear in Apache's logs

    1. [Sun May 15 20:06:17 2011] [error] [client 203.0.113.96] (13)Permission denied: file permissions deny server access: /var/www/vhosts/vh2/index.html

This log entry shows that permissions on the index.html file for
vh2.example.com are denying access to Apache.

    2. [Sun May 15 20:07:37 2011] [error] [client 203.0.113.96] (13)Permission denied: access to /index.html denied

This log entry shows that permissions on the /var/www/vhosts/vh2
directory are blocking Apache's read request.

    3. [Sun May 15 20:11:32 2011] [error] [client 203.0.113.96] (13)Permission denied: access to / denied

This log entry shows that Apache does not have execute or read
permissions on one of the directories above DocumentRoot.

###  

