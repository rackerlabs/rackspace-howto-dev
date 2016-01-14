---
node_id: 4657
title: Differences between Rackspace CDN and Rackspace Cloud Files
type: article
created_date: '2015-05-08 19:58:04'
created_by: Rackspace Support
last_modified_date: '2015-10-05 15:1258'
last_modified_by: catherine.richardson
product: Rackspace CDN
body_format: tinymce
---

Rackspace Cloud Files is storage service that enables users to store an
unlimited number of files and to publish and distribute content behind a
content delivery network (CDN). Following are some differences between
Rackspace CDN and Cloud Files:

-   Users of Rackspace CDN specify the origins that host the content,
    and the CDN pulls the content from these origins. Origins can be
    dedicated servers, cloud servers, cloud load balancers, or even
    servers hosted outside of Rackspace. Users of Cloud Files can
    CDN-enable a container, thereby distributing the contents of that
    container to the CDN&rsquo;s edge nodes. In Rackspace CDN, it is not yet
    possible to specify a Cloud Files container as an origin.
-   Rackspace CDN has no limit on purges. Cloud Files limits the number
    of purges per account, per day to 25.
-   Rackspace CDN does not yet support streaming video from Cloud Files
    CDN-enabled containers or serving CDN-enabled content over SSL/TLS.
    Cloud Files supports streaming video from CDN-enabled containers as
    well as serving CDN-enabled content over SSL/TLS.

These, and other differences, are summarized in the following table:

![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-10-01%20at%2011.45.33%20AM.png)

 

#### [\< Rackspace CDN terminology](https://www.rackspace.com/knowledge_center/article/rackspace-cdn-terminology)    -    [Access Rackspace CDN \>](https://www.rackspace.com/knowledge_center/article/access-rackspace-cdn)

 

 

 

