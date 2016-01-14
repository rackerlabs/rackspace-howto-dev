---
node_id: 2157
title: Multi-region support in Cloud Files
type: article
created_date: '2012-09-12 18:31:38'
created_by: David Hendler
last_modified_date: '2014-12-23 19:0132'
last_modified_by: rose.contreras
product: Cloud Files
body_format: tinymce
---

Rackspace allows you to choose the data center where you would like to
store your content. You may select our Dallas (DFW), Chicago (ORD),
North Virginia (IAD), Hong Kong (HKG), or Sydney, Australia (SYD)
locations through our multi region support. This means you can have your
Cloud Servers or Dedicated Servers in one location and your data in
another. Or, you can keep them in the same data center to reduce latency
and take advantage of free bandwidth using our internal data center
network, ServiceNet.\
 \
 Customers who only serve certain geographic regions may also find it
helpful to locate the Cloud Files objects as close to that region as
possible.  Note that not all third-party libraries that communicate with
Cloud Files have been updated to support multiple regions.  In some
cases if the tool you use isn't uploading to the region you expect, you
can contact Support and ask them to change your account's default
region.  That may get the tool to use your preferred region for file
transfers.

###  

### How do I set up Multi Region?

You do&rsquo;t need to do anything to set up multi region capabilities for
your account. All U.S. accounts have access to multiple regions.  If you
use the Auth 1.1 or 2.0 API, you may choose which endpoint to interact
with; once you've authenticated against the regional endpoint, your
Cloud Files operations will only affect that region's content. So, if
you have content in two locations and you want to make edits, you will
have to make those edits in both locations.

\
 MyRackspace and [Cloud Control Panel](http://mycloud.rackspace.com)
users can also take advantage of the multi region feature. When you
create a container, choose the data center where you would like it. Your
control panel will reflect the location of your container.\
 \
 The following screenshots illustrate this new capability:

MyRackspace Portal - Create New Container:

![](/knowledge_center/sites/default/files/field/image/CreateContainer.png)

Cloud Control Panel - Create New Container:

![](/knowledge_center/sites/default/files/field/image/TestContainerVirginia_0.png)

 

Cloud Control Panel - Upload Files or click the Containers link in the
breadcrumb trail to see your container list.

![](/knowledge_center/sites/default/files/field/image/ContainerContent_0.png)

 

Cloud Control Panel - List Containers

![](/knowledge_center/sites/default/files/field/image/ContainerList_0.png)

Our API users will also see changes in their Service Catalog, which now
shows multiple endpoints for&ldquo;object stor&rdquo;:

![](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/cf%20-%20api%20access%20points.png)

 

Cloud Files does NOT automatically replicate data across regions.
Customers who would like to have their data in both places should ensure
PUTs are done to both endpoints and they will be charged for data stored
in both locations along with related bandwidth charges.\
 \
 All customers existing previous to September 1, 2012 had their current
region set as their&ldquo;default", which orders it first in the list of
endpoints when authenticating against Cloud Files using our Auth 1.1 or
2.0 APIs. Customers using Auth 1.0 will still only have a single
endpoint returned.\
 \
 If you have customers around the world, do&rsquo;t forget that you can
deliver your content rapidly with Akama&rsquo;s Content Delivery Network
(CDN), which caches content at global edge locations and saves users
time because the requested content is received from within the region
instead of coming from the origin data center.

