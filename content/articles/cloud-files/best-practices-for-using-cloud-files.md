---
node_id: 1269
title: Best Practices for Using Cloud Files
type: article
created_date: '2012-01-05 21:04:56'
created_by: RackKCAdmin
last_modified_date: '2014-05-16 18:1520'
last_modified_by: kyle.laffoon
products: Cloud Files
body_format: tinymce
---

undefined&rsquo;s
best to plan ahead for this.

### TTL {.MsoNormal}

In addition to the performance benefit of reduced time in listings, you
also get the improvement of being able to set the TTL (Time To Live
value) for containers containing objects on the CDN. TTL can only be set
on the Cloud Files container, and all objects inherit the
container-level setting. A particular object in a container cannot have
a TTL that is different than the other objects in the same container.
This means that you could set longer TTL values on content that is
unlikely to change often.  For website acceleration, you could use a
longer TTL (at the container-level) for files that are updated
infrequently, such as your CSS, javascript, and videos.  At the same
time, you can set a shorter TTL for rapidly changing objects, such as
user uploads.  Using an appropriate TTL for the object type in your
container will improve performance since, the longer the TTL, the more
consistent the performance as it renews the CDN cache from your cloud
files store less frequently. 

