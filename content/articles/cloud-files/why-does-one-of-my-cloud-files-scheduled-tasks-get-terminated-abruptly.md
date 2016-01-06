---
node_id: 750
title: Why does one of my Cloud Files scheduled tasks get terminated abruptly?
permalink: article/why-does-one-of-my-cloud-files-scheduled-tasks-get-terminated-abruptly
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2014-03-25 20:4955'
last_modified_by: kyle.laffoon
products: Cloud Files
body_format: tinymce
---

The Rackspace Cloud system restricts the maximum execution time of any
one cron job to 15 minutes. Please make sure that your script is well
tested and can complete its intended job within this time frame.

