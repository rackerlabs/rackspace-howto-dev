---
node_id: 1435
title: Checking running services on Linux
type: article
created_date: '2012-06-21 14:48:12'
created_by: RackKCAdmin
last_modified_date: '2015-12-31 20:3225'
last_modified_by: stephanie.fillmon
products: Cloud Servers
body_format: tinymce
---

undefined&rsquo;t running, starting it may have resolved the issue.
Let's give it a test to find out.

If the program is running you should see something similar to the
following when you check it with service:

~~~~ {.pre .codeblock}
$ sudo service xinetd status
xinetd (pid  8795) is running...
~~~~

If you cannot start your application take a look at your logs to see if
they contain further information regarding the issue. This guide should
help with making use of your logs.

### Continuing onward {.title .topictitle1}

Once you're sure the application is running you'll want to [take a look
at the server resources it is
consuming](http://www.rackspace.com/knowledge_center/article/checking-system-load-on-linux).

