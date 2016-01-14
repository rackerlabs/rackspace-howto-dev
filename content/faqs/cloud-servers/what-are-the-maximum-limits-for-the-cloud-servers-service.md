---
node_id: 4920
title: What are the maximum limits for the Cloud Servers service?
type: frequently_asked_question
created_date: '2015-11-11 17:13:18'
created_by: cat.lookabaugh
last_modified_date: '2015-11-11 20:4744'
last_modified_by: kyle.laffoon
product: Cloud Servers
body_format: tinymce
---

The maximum limits are as follows:

+--------------------------+--------------------------+--------------------------+
| Limit Name               | Description              | Value                    |
+==========================+==========================+==========================+
| maxImageMeta             | The maximum number of    | 40                       |
|                          | metadata key value pairs |                          |
|                          | associated with a        |                          |
|                          | particular image.        |                          |
+--------------------------+--------------------------+--------------------------+
| maxPersonality           | The maximum number of    | 5                        |
|                          | file path/content pairs  |                          |
|                          | that can be supplied     |                          |
|                          | when a server is built   |                          |
|                          | or rebuilt.              |                          |
+--------------------------+--------------------------+--------------------------+
| maxPersonalitySize       | The maximum size, in     | 1000                     |
|                          | bytes, for each          |                          |
|                          | personality file.        |                          |
+--------------------------+--------------------------+--------------------------+
| maxServerMeta            | The maximum number of    | 40                       |
|                          | metadata key value pairs |                          |
|                          | associated with a        |                          |
|                          | particular server.       |                          |
+--------------------------+--------------------------+--------------------------+
| maxTotalCores            | This limit is disabled,  | -1                       |
|                          | so no limits exist on    |                          |
|                          | the total number of      |                          |
|                          | cores.                   |                          |
+--------------------------+--------------------------+--------------------------+
| maxTotalInstances        | The maximum number of    | 100                      |
|                          | cloud servers that can   |                          |
|                          | exist in your account at |                          |
|                          | any one time.            |                          |
+--------------------------+--------------------------+--------------------------+
| maxTotalPrivateNetworks  | The maximum number of    | 10                       |
|                          | isolated networks that   |                          |
|                          | you can create. Set to   |                          |
|                          | **0** when Cloud         |                          |
|                          | Networks is disabled,    |                          |
|                          | **10** when Cloud        |                          |
|                          | Networks enabled.        |                          |
+--------------------------+--------------------------+--------------------------+
| maxTotalRAMSize          | The maximum total amount | 131072                   |
|                          | of RAM (MB) of all cloud |                          |
|                          | servers in your account  |                          |
|                          | at any one time.         |                          |
+--------------------------+--------------------------+--------------------------+



