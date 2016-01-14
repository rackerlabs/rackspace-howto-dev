---
node_id: 4980
title: Cloud Files - FAQs
type: article
created_date: '2015-12-03 00:32:27'
created_by: Rackspace Support
last_modified_date: '2016-01-11 22:0652'
last_modified_by: kyle.laffoon
product: Cloud Files
body_format: tinymce
---

* * * * *

- Getting Started -
-------------------

### How can I get live support for Cloud Files?

Support is available by email at
[cloudfiles@rackspace.com](mailto:support@rackspacecloud.com "mailto:support@rackspace.com")
Monday through Friday, 9AM to 5PM CST. Tech support will be happy to
answer any questions you have about Cloud Files, except for code related
issues. If you do have questions about design or coding please try our
forums or documentation.

### How Can I Use Akamai's CDN With Cloud Files?

Rackspace Cloud Files uses [Akamai Technologies,
Inc](http://www.akamai.com/ "http://www.akamai.com/"). a leading, tier
one, global Content Delivery Network (CDN) provider to offer the
benefits to all Cloud Files users. Today Akamai handles tens of billions
of daily Web interactions for their customers such as Audi, NBC,
Fujitsu, U.S. Department of Defense, and NASDAQ.

The Rackspace CloudFiles/Akamai relationship brings full-fledged, robust
CDN capabilities and unlimited file storage to developers and corporate
IT departments alike. The CDN capability will greatly enhance the
quality of the end user experience by speeding the delivery of
bandwidth-heavy rich content, including audio and video. For literally
pennies per gigabyte of bandwidth and storage and no upfront
commitments, the CDN advantage is now available to all not just to the
giants of the internet. This partnership brings unlimited online
storage, scalable content delivery, and application acceleration
services, thereby allowing businesses to more easily and affordably
distribute content to millions of end users around the world. Together
with Akamai, Rackspace has democratized content delivery.

With Akamai&rsquo;s service, Cloud Files brings a powerful and easy way to
publish content over a world-class, industry leading CDN. A Cloud Files
user automatically gets access to this network. Users have to mark
containers for publishing to CDN, and then they are instantly accessible
through Akamai CDN. The propagation of content to the edge locations is
done automatically behind the scenes. The Rackspace Cloud/Akamai
offering is not a one-off solution; content published through it is
distributed across their entire infrastructure just as it is for other
customers.

In the Rackspace Cloud control panel, it is a matter of creating a
Container (the storage compartment for data), uploading Objects (the
files to serve over CDN), and marking the Container as &ldquo;public&rdquo;. The
Container is then assigned a unique URL which can be combined with
Object names to embed in web pages, email messages, blog posts, etc. For
example, a user could upload a photo to a Container called &ldquo;images&rdquo;.
When this Container is published, it will be assigned a unique URL like
http://c0000532.cdn.cloudfiles.rackspace.com. The user could then share
a link to the photo with link like
http://c0000532.cdn.cloudfiles.rackspace.com/IMG\_3432.jpg. When that
link is accessed, the photo is served from the CDN; it&rsquo;s that simple!

### What can I do with Cloud Files tools?

There is a growing list of tools and extensions. A sampling is as
follows.

**Rackspace CDN** is a WordPress plug-in that allows any media in your
WordPress uploads folder to be uploaded to Rackspace Cloud Files,
powered by CDN. Once the file is uploaded, it is deleted from the local
server. Link:
[https://wordpress.org/plugins/rackspace-cloud-files-cdn/](https://wordpress.org/plugins/rackspace-cloud-files-cdn/%20)

**Cyberduck** is a full-featured browser to publish your content on
Cloud Files and manage your CDN distributions with a click of a button.
Access your Rackspace Cloud Files remote storage using the familiar
Cyberduck browser interface to create containers and upload content
using drag and drop. Create a distribution to register that container
with the Akamai's Content Distribution Network through using the Info
panel of the browser that displays the CDN URL. Distribution can be
toggled on or off at any time. Supporting the latest and greatest
version of the Cloud Files protocol, you can also browse hierarchical
pseudo-folder structures. Link:
[http://cyberduck.ch/](http://cyberduck.ch/ "http://cyberduck.ch/")

**Django-Cloudfiles** is an extension to the management system of
Django, the popular website framework. Django-Cloudfiles lets you
synchronize the static content directory of your Django-powered website
to your Cloudfiles account effortlessly. Django-Cloudfiles is&mldr;Cool! 1.
it only uploads files that have been modified (but can force upload-all)
2. it can create a new container for you 3. it preserves your file
hierarchy by naming your remote files such that they emulate nested
directories: no need to flatten your existing structure! 4. it lets you
store credentials in your site&rsquo;s configuration file (for easy use) or
specify them on the command line (for greater security) 5. it ignores
files you probably don&rsquo;t want to upload, like .DS\_Store, .git,
Thumbs.db, etc. Original! 6. plug-ins for the Django management system
do exist (e.g. django-extensions), but none integrate with Cloudfiles
yet (or any CDN to my knowledge) Easy! 7. a dead simple drop-in (no
coding necessary) 8. no external dependancies required Going to be
Popular! 9. Django is all about reusability; Django developers always
look for an existing solution first (like this one)! 10. Django is
gaining steam: it&rsquo;s supported by Google App Engine, and it is gaining
traction. Link:
[http://github.com/rossdakin/django-cloudfiles/](http://github.com/rossdakin/django-cloudfiles/ "http://github.com/rossdakin/django-cloudfiles/")

**Media manager** plug-in will mirror your media library to your Cloud
Files CDN. All URL&rsquo;s to this content will use the Cloud Files path when
you insert them via the media manager. You can import all of your media
to the CDN.

New tools are added constantly - Check out [Cloud
Tools](https://cloudtools.rackspace.com/home "https://cloudtools.rackspace.com/home")

### Cloud Files Key Concepts

Cloud Files&trade; is not a &ldquo;file system&rdquo; in the traditional sense. You will
not be able to *map* or *mount* virtual disk drives like you can with
other forms of storage such as a SAN or NAS. Since Cloud Files is a
different way of thinking when it comes to storage, following is a
review of key concepts.

**Accounts**

The Cloud Files system is designed to be used by many different
customers. Your user account is your slice of the Cloud Files system. A
user must identify themselves with a valid Username and their API Access
Key. Once authenticated, that user has full read/write access to the
Objects (files) stored under that user account.

**Containers**

A Container is a &ldquo;storage compartment&rdquo; for your data and provides a way
for you to organize that data. You can think of a Container as a folder
in Windows(R) or a directory in UNIX(R). The primary difference between
a Container and these other &ldquo;file system&rdquo; concepts is that Containers
cannot be nested. You can, however, create up to 500,000 Containers
under your account.

**Objects**

An &ldquo;Object&rdquo; is the basic storage entity and its metadata that represents
the &ldquo;files&rdquo; you store in Cloud Files. When you upload data to Cloud
Files the data is stored as-is (no compression or encryption) and
consists of a location (Container), its name, and optional metadata
consisting of key/value pairs. For instance, you may chose to store a
backup of your digital photos and add a metadata key/value pair of
&ldquo;PhotoAlbum-CaribbeanCruise&rdquo;. Objects are grouped into Containers and
you can have any number of Objects within a Container.

**Operations**

Operations are the actions you perform against your account in Cloud
Files. Creating or deleting Containers, uploading or downloading
Objects, etc. The full list of operations is documented under the ReST
API section of the Developer Guide. Operations are performed via the
ReST web service API or a language-specific API (currently we support
Python, PHP, Java, and C\#/.NET).

**Permissions**

There are no permissions or access-controls around Containers or Objects
other than being split into separate accounts. Users must authenticate
with a valid API Access Key, but once authenticated they can
create/delete Containers and Objects only within that Account.

At this time, there is no way to make a storage object publicly
accessible.

**CDN-enabled Containers**

To publish your data so that it can be served by Akamai's Content
Distribution Network (CDN), you need to &ldquo;publish to CDN&rdquo; the Container
that houses that data. When a Container is published any files will be
publicly accessible and not require an authentication token for read
access. Uploading content into a CDN-enabled Container is a secure
operation and will require a valid authentication token.

Each published Container has a unique Uniform Resource Locator (URL)
that can be combined with its Object names and openly distributed in web
pages, emails, or other applications. For example, a published Container
named &ldquo;photos&rdquo; can be referenced as &ldquo;
http://c0344252.cdn.cloudfiles.rackspace.com &rdquo;. If that Container houses
an image called &ldquo;cute\_kids.jpg&rdquo;, then that image can be served by
Akamai's CDN with the full URL of
&ldquo;http://c0344252.cdn.cloudfiles.rackspace.com/cute\_kids.jpg&rdquo;. This URL
can be embedded in HTML pages, email messages, blog posts, etc. When
that URL is accessed, a copy of that image is fetched from the Cloud
Files storage system and cached in Akamai's CDN and served from there
for all subsequent requests.

### How do I use Cloud Files and CDN?

This guide provides an overview of Rackspace Cloud Files and its
features to help you get started quickly and serve content over Akamai's
CDN service.

Cloud Files allows you to store data on the Rackspace infrastructure.
The [Cloud Control
Panel](https://mycloud.rackspace.com/ "Cloud Control Panel") allows
customers to accomplish most tasks for managing data, but the [Cloud
Files
API](http://docs.rackspace.com/files/api/v1/cf-devguide/content/Overview-d1e70.html)
and some third-party tools are also available.

The basics of Cloud Files include:

-   Cloud Files is a &ldquo;cloud&rdquo; storage system and not a traditional file
    system.
-   Customers need to create &ldquo;Containers&rdquo; in the storage system to store
    data.
-   You cannot create Containers within other Containers.
-   Customers can have any number of top level Containers.
-   Your data is stored in &ldquo;Objects&rdquo; within those Containers.
-   You can have any number of Objects within a Container.
-   Objects can vary in size from a few bytes to very large.
-   Customers can interact with Cloud Files through the Rackspace Cloud
    Control Panel or language-specific programming interfaces.

More detail can be found in [Cloud Files Key
Concepts](https://admin.rackspace.com/knowledge_center/frequently-asked-question/cloud-files-key-concepts).

**Cloud Files Usage Scenarios**

* * * * *

There are a number of basic usage scenarios for Cloud Files. We have
classified them based on user objectives.

**For Application Developers**

* * * * *

-   A development guide is available at [Cloud Files Dev
    Guide](http://docs.rackspace.com/files/api/v1/cf-devguide/content/Overview-d1e70.html "http://docs.rackspace.com/files/api/v1/cf-devguide/content/Overview-d1e70.html")
-   Cloud Files has several [Software Development Kits
    (SDKs)](https://admin.rackspace.com/knowledge_center/article/sdks-for-java-ruby-python-nodejs-php-and-microsoftnet)
    for popular programming languages
-   An [API Getting Started
    Guide](http://docs.rackspace.com/files/api/v1/cf-getting-started/content/Overview-d1e01.html)
    is available for the Cloud Files API

**For Content Providers and Website Designers**

* * * * *

-   [Use Cloud Files to serve static content for
    websites](https://admin.rackspace.com/knowledge_center/index.php/Use_Cloud_Files_to_serve_static_content_for_websites "Use Cloud Files to serve static content for websites")
-   Check out some [Cloud Files
    tools](https://admin.rackspace.com/knowledge_center/frequently-asked-question/what-can-i-do-with-cloud-files-tools "What can I do with Cloud files tools ?")
    which can improve website performance and scalability.

**For IT Managers**

* * * * *

-   Check out some [Cloud Files
    tools](https://admin.rackspace.com/knowledge_center/frequently-asked-question/what-can-i-do-with-cloud-files-tools "What can I do with Cloud files tools ?")
    which can ease day to day operations such as data backup and
    archival.

**For all users**

* * * * *

-   [Getting your API key for Cloud
    Files](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-viewing-and-regenerating-your-api-key "Getting the key to use Cloud Files")
-   [Uploading to Cloud Files with
    Cyberduck](https://admin.rackspace.com/knowledge_center/article/configuring-rackspace-cloud-files-with-cyberduck)

**Additional Cloud Files Resources**

-   [Rackspace Official SDKs and
    Tools](https://developer.rackspace.com/sdks/ "Rackspace Official SDKs")
    for Java, .NET, node.js, PHP, Python, and Ruby

### Why Should I Use Cloud Files?

There are a number of reasons to choose the Cloud Files service over
similar services available in the market.

-   Simplicity of CDN functionality.
-   Utility pricing - paying only for what you use, after you use it.
-   Multiple APIs for developers to choose from.
-   Fast and reliable performance.
-   World class support

**Simplicity**

Cloud Files is simple to use for developers and non-developers alike.
Users can get started in as little as five minutes. Users do not have to
know how to code to use Cloud Files and CDN. Users can, within minutes,
sign up for Cloud Files, create a Container, upload a file and publish
that Container&rsquo;s content through the CDN (Refer to &ldquo;Cloud Files with CDN
QuickStart guide&rdquo;. The Cloud Files GUI is easy to navigate and use.
Rackspace browser based control panel let users easily upload files and
distribute on a CDN without writing any code.

All the content can be backed by a CDN without complex negotiations and
details of updating content for optimizing delivery. Given the
complexity of the CDN, users may have to make a series of choices such
as number of servers to use etc. before obtaining the service. After
making the choices users must ensure the usage bills are accurate. All
these issues are handled by Cloud Files. CDNs have, in the past, been
the prerogative of companies with more money but Cloud Files has changed
that.

Cloud Files is a user and developer friendly service. Security
mechanisms described in more detail in the Security section are simple
to use. Third party tools which further simplify use of the storage
service are available. Developers can use a language specific
application programming interfaces to develop utilities or applications.
The API&rsquo;s are easy to use and are documented with examples to get
started quickly.

**Affordability**

Pricing for Cloud Files with CDN is comprised of the amount of total
data you have stored (per GB), and the amount of bandwidth used to serve
the data (outbound bandwidth only, charged per GB to any edge location
on the CDN around the globe). There are no 'per request' fees for CDN.
The [current pricing for Cloud
Files](http://www.rackspace.com/cloud/cloud_hosting_products/files/pricing/)
can always be found on our website.

**Flexibility**

Cloud Files is a dynamically expanding storage system very flexible and
is built on the pay for use principle. Customers can use as much or
little storage as necessary, while paying only for storage space used.
There is no limit on total space use and individual files can range in
size from a few bytes to extremely large. The GUI control panel allows
users to check storage space used and bandwidth utilized. There are no
upfront fees or contracts and end users pay only for storage space used
and outgoing bandwidth that they use.

System administrators can use this for simple manual updates as well.
Users do not have to know how to code to use Cloud Files and CDN. No API
is required to share files. Non-developers have a simple web-interface,
that can be used to quickly and easily upload data and enable CDN
access. There are multiple third party tools (refer to Tools and
Applications section) which make it even more flexible for users of
specific environments such as the Mac OS.

Developers can use the ReST web service and language-speicifc API&rsquo;s in
PHP, Python, Java, Ruby, and C\#/.NET. The API's provide full support
for managing content in Cloud Files and publishing content over the CDN.
The API allow developers to work in the language they feel most
comfortable

**Superior performance**

Rackspace has built networks with superior performance for years. The
Akamai CDN capability improves the performance further for distribution
of digital content. In short, Akamai can bring data closer to end users
and serve popular content faster.

**World Class support**

With Cloud Files world-class free technical support is only a click
away. Live support, with real people is available 24/7. Fanatical
Support is built into the price. Users can get peace of mind knowing
that technical support is just a phone call or online chat away &ndash; at any
time of the day.

**Data Redundancy**

The Cloud Files storage system is designed to be highly available and
fault tolerant. Cloud Files achieves client data redundancy by
replicating three full copies on different storage nodes. Storage nodes
are grouped in logical Zones within Rackspace datacenters. Zones are
connected to redundant Internet backbone providers and reside on
redundant power supplies and generators. The system has been engineered
in such a way as to continue to by fully functional even in the event of
a major service disruption within a Datacenter. Content on the CDN
provides an additional layer of data redundancy.

**Security**

Cloud Files uses a number of different measures to ensure that your data
is kept safe. First and foremost, all traffic between clients and the
Cloud Files system uses SSL to establish a secure, encrypted
communication channel. This ensures that any data (usernames, passwords,
and content) cannot be intercepted and read by a third-party. Users
authenticate with a valid username and API Access Key and are granted a
session authentication token. These authentication tokens are used to
validate all operations against Cloud Files. There is no way to
terminate a valid session by the user, but the session tokens will
automatically expire after 24 hours, forcing clients to resend their
credentials.

The API Access Key is only available from within the Rackspace Cloud&rsquo;s
control panel. Users must enter their valid username and password to
gain access to view the API Access Key or to generate a new key.

It is important to note that Cloud Files does not apply any
transformations to data before storing it. This means that Cloud Files
\*will not\* store data in encrypted form unless the client encrypts it
prior to transmission. This allows users to select the type and level of
encryption best suited for their application.

When deleting storage Objects from the Cloud Files system, all copies of
data are permanently removed within a matter of minutes. Furthermore,
the physical blocks making up the customer&rsquo;s data is zeroed over before
that space is re-used for other customer data. In other words, after a
delete request, the data will be unrecoverable.

### What is Cloud Files?

**Introduction**

Cloud Files&trade; is an affordable, redundant, scalable, and dynamic storage
service offering. The core storage system is designed to provide a safe,
secure, automatically re-sizing and network accessible way to store
data.

You can store an unlimited quantity of files ranging in size from a few
bytes to extremely large. Users can store as much as they want and pay
only for storage space they actually use.

Cloud Files makes it easy to serve content through a CDN. This allows
users to take advantage of a proven world-class content distribution
network that is affordable and easy to use.

Cloud Files also allows users to store/retrieve files and CDN-enable
content with a simple Web Service (ReST: Representational State
Transfer) interface. There are also language-specific API&rsquo;s that utilize
the ReST API but make it much easier for developers to integrate into
their applications.

**Ideal uses for Cloud Files**

There are a number of uses for the Cloud Files service. Cloud Files is
an excellent storage solution for a number of scenarios and is well
suited for a number of applications such as:

-   Backing up or archiving data
-   Serving images/videos (streaming data to the user&rsquo;s browser)
-   Serving content with a world-class CDN (Akamai)
-   Storing secondary/tertiary, static web-accessible data
-   Developing new applications with data storage integration
-   Storing data when predicting storage capacity is difficult
-   Storing data for applications affordably

**Key Concepts**

Cloud Files&trade; is not a &ldquo;file system&rdquo; in the traditional sense. You will
not be able to map or mount virtual disk drives like you can with other
forms of storage such as a SAN or NAS. Since Cloud Files is a different
way of thinking when it comes to storage, please take a few moments to
[review the
concepts](https://admin.rackspace.com/knowledge_center/index.php/Key_Concepts).

**Using Cloud Files**

There are two ways to use Cloud Files:

1.  GUI interface such as the Rackspace Cloud Control Panel or
    Cyberduck.
2.  Programming interfaces via ReST, Python, PHP, Ruby, Java, or
    C\#/.NET.

**Control Panel Interface**

The Control Panel provides an browser based, intuitive, easy to use
graphical user interface. The interface allows you to manage your
Containers and Objects without any programming knowledge. From there,
users can CDN-enable the Container by marking it &ldquo;public&rdquo;. Any Objects
stored in a public, CDN-enabled Container are directly accessible over
the Akamai&rsquo;s CDN.

**Programming Interfaces**

There are several programming interfaces for Cloud Files that will allow
you to integrate the storage solution into your applications, or provide
automated ways of accessing the system. Currently, we support a ReST
web-services API and several programming language API&rsquo;s (Python, PHP,
Java, Ruby, and C\#/.NET).

Please refer to the Developer Guide for more details about using these
interfaces. You can access the Developer Guide on our [API documentation
site](http://docs.rackspace.com/api/).

### What is a Container in Cloud Files?

A Container is a &ldquo;storage compartment&rdquo; for your data and provides a way
for you to organize that data. You can think of a Container as analogous
to a folder in Windows&reg; or a directory in UNIX&reg;. The primary difference
between a Container and these other &ldquo;file system&rdquo; constructs is that
Containers cannot be nested. You can have up to 500,000 Containers in
your account, but they only exist at the &ldquo;top level&rdquo; of your account and
Containers cannot reside within other Containers.
![](/knowledge_center/sites/default/files/field/image/createContainer1.png)

**Note**: Containers scale to about one million objects before
peformance degrades. Containers can only be removed from Cloud Files if
they do NOT contain any storage Objects. In other words, make sure the
Container is empty before attempting to delete it.

### How do I access Cloud Files?

First you must make sure you have generated a valid API Access Key. Then
you can use either the Cloud Files user interface in the Rackspace Cloud
Control Panel or one of our programming interfaces.

Please see the [How do I use Cloud Files and
CDN?](https://admin.rackspace.com/knowledge_center/frequently-asked-question/how-do-i-use-cloud-files-and-cdn)
Knowledge Center article for more details.

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

**Account Services**

Can Cloud Files be used for my Cross-domain policy file?

[Edit](https://admin.rackspace.com/knowledge_center/node/4624/edit)

No. The Cloud Files CDN does not support exposing a custom
crossdomain.xml file, as this is a required file by the Openstack Swift
project. OpenStack Swift uses this as a global configuration file for
the installation, and can not be modified for multiple tenants, such as
our Public Cloud.

Is there a Cloud Files specific SLA?

[Edit](https://admin.rackspace.com/knowledge_center/node/2191/edit)

Please click here to view [The Rackspace Cloud Terms of
Service](http://www.rackspace.com/cloud/legal/).

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

**Security**

Why does uploading a file in the Control Panel set the Allow-Origin
header on my container?

[Edit](https://admin.rackspace.com/knowledge_center/node/3969/edit)

When you upload a file in the Cloud Control Panel, an Allow-Origin
header is set on the container to support cross-origin resource sharing
(CORS). Browsers prevent AJAX requests between different domains by
default. Because the Cloud Files API and the Control Panel reside on
different domains, CORS must be enabled to support uploads directly to a
container. When the upload succeeds, the CORS headers are removed.

By allowing the browser to upload directly to the Cloud Files API,
maximum upload performance can be achieved.

Read more about CORS at
[http://en.wikipedia.org/wiki/Cross-origin\_resource\_sharing](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing)
.

### Cloud Files - How do Permissions Work?

There are no permissions or access controls around containers or objects
other than being split into separate accounts. Users must authenticate
with a valid user name and API Access Key, but once authenticated, they
can create or delete containers and objects only within that account.

At this time, there is no way to publicly access the objects stored in
Cloud Files unless that container is published to CDN. Each request to
Cloud Files must include a valid "storage token" in an HTTP header
transmitted over a HTTPS connection.

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

Web Technologies
----------------

### Getting Started with Cloud Files Streaming

Streaming content through Cloud Files lets you deliver video content
quickly and easily, without making your users download the content
first. They can begin viewing your content immediately and can jump
around the video stream without needing to buffer.

Because Rackspace uses HTTP delivery for streaming content, you can use
the Akamai CDN network to deliver your content. This means the
performance should be identical to CDN speeds customers are used to.
Before you begin, you must CDN-enable the container that holds your
streaming content. In the Cloud Control Panel, click the gear icon of
the container and select "Make Public (Enable CDN)".

Once your container is CDN-enabled, you will need its Streaming URLs. In
the Cloud Control Panel, click the gear icon for the container and
select "View All Links...". Below is an example of the CDN links that
display:

    HTTP: http://cdc4c16471588d4846bf-cc339a649709710bbecd3db1e126ec2b.r3.cf1.rackcdn.com
    HTTPS: https://ac3c779acb946eaf4819-cc339a649709710bbecd3db1e126ec2b.ssl.cf1.rackcdn.com
    Streaming: http://b0c42c537095921be66c-cc339a649709710bbecd3db1e126ec2b.r3.stream.cf1.rackcdn.com
    iOS Streaming: http://09ac235af93af07922d6-cc339a649709710bbecd3db1e126ec2b.iosr.cf1.rackcdn.com

There are several different ways to stream your content with Cloud
Files. Click a link below to find out more for each approach.

-   [JW
    Player](https://admin.rackspace.com/knowledge_center/article/streaming-cloud-files-with-jw-player)
-   [FlowPlayer](https://admin.rackspace.com/knowledge_center/article/cloud-files-streaming-with-flowplayer-plugins)
-   [OSMF (Open Source Media
    Framework)](https://admin.rackspace.com/knowledge_center/article/cloud-files-streaming-with-osmf-plugins)
    , which allows you to build your own player
-   [iOS Device
    Streaming](http://docs.rackspace.com/files/api/v1/cf-devguide/content/iOS-Streaming-d1f3725.html)
    (link goes to API Developer Guide)

\
 Cloud Files Streaming FAQs
---------------------------

### Why have we chosen to support specific players?

Many Rackspace customers are not flash developers, but still want to use
a streaming offer. There are a few players that are dominating the
market, and we will plan to support each of them. Custom plugins are
required in order for Streaming delivery to work properly over the
Akamai network. As Akamai adds support for more players, our customers
will have access to them.

### Why are we not using RTMP?

-   RTMP is probably the most popular delivery format today, but the
    market is quickly moving towards HTTP delivery for Streaming
    content. Here are just a few reasons the market is moving towards
    HTTP.
-   Accessibility- Many firewalls block RTMP and RTSP streaming
    protocols because corporations don't want users watching video at
    work. HTTP appears to be normal web traffic, meaning that videos
    served over HTTP are usually left open.
-   Startup times- Akamai sees a significant reduction in stream startup
    times on average for traffic served via HTTP.
-   Throughput (image quality)- With the HTTP network being larger than
    many other networks, Akamai is closer to the end user on their HTTP
    network meaning they get better throughput of data. that means
    customers will experience higher bit rates uninterupted (and without
    buffering) and increase the end user's over all experience.

 

### Is this available internationally?

Yes, this is available to both US and UK Cloud customers.

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

Content Delivery Network
------------------------

### Does CDN management in Cloud Files support exposing a custom crossdomain.xml file?

Cloud Files CDN does not support exposing a custom crossdomain.xml file
because this file is required by the Openstack Swift project, on which
Cloud Files is based.

OpenStack Swift uses the crossdomain.xml file as a global configuration
file for installation. The file cannot be modified for multiple tenants,
such as our Rackspace Public Cloud.

For more information, see [Cross-domain Policy
File](http://docs.openstack.org/developer/swift/crossdomain.html).

If your site requires a custom crossdomain.xml file, we suggest you take
a look at [Rackspace
CDN](http://www.rackspace.com/cloud/cdn-content-delivery-network).
Rackspace CDN allows you to customize your configuration and define your
own origin web server.

### What is the TTL attribute in a Cloud Files container?

This article describes the use of the Time To Live (TTL) attribute and
how it works.

When you create a container in Cloud Files and you make that container
public, the files within that container have a designated TTL. The TTL
is the time interval after which the CDN will reread the contents of the
container. This attribute and its value can be modified in the CDN
through the Cloud Files user interface.

New values take effect after the current TTL cycle is completed. The TTL
can be any value between 15 minutes and 50 years. Use higher numbers for
static content that doesn't change often, and use smaller numbers for
content that changes more often. If you require a longer TTL, see the
following blog post about using the API to set TTL: Extending TTL for
Cloud Files CDN Users.

Use the following steps to modify a container&rsquo;s TTL within the Cloud
Control Panel:

1.  Log in to the [Cloud Control Panel](https://mycloud.rackspace.com).
2.  In the top navigation bar, select **Storage \> Files**.
3.  If the container is not already public, click the gear icon next to
    the container and select **Make Public (Enable CDN)**. In the popup
    box, click **Publish to CDN**.
4.  Click the gear icon next to the container again and select **Modify
    Time To Live (TTL)**.
5.  Enter the TTL for the container in seconds, and then click **Save
    TTL**.

How Do I Use the Cloud Files CDN Manager?

[Edit](https://admin.rackspace.com/knowledge_center/node/2198/edit)

This article describes how to create a container within Cloud Files and
manage files in it through the Cloud Files interface.

### What is the CDN?

Using the Akamai content delivery network (CDN) service, Cloud Files
brings you a powerful and easy way to publish content over a world-class
industry leading CDN. Customers automatically get access to this network
as part of using the Cloud Files service. The way it works is by
distributing the content that you upload to Cloud Files across a global
network of edge servers. What this means is that when someone is viewing
content from your site, your CDN-enabled content will be served to them
from the closest geographic edge server to their location. This feature
dramatically increases the speed at which websites can load, no matter
where your viewer is located.

This can be a great advantage when hosting content for an international
audience. Though you can also use the API to upload content to Cloud
Files, another way is to use the File Manager interface in the Cloud
Control Panel. To store content on Cloud Files, you start by creating a
container for your content. The container name should have no breaks,
spaces, or special characters. Unlike a folder or directory, a container
cannot have subdirectories. All your content will be at one level below
the container name.

**Create a container**

1.  Log in to the [Cloud Control Panel](http://mycloud.rackspace.com).
2.  In the top navigation bar, select **Storage \> Files**.
3.  Click **Create Container**.
4.  Name the container, and then click **Create Container**.
5.  Click the gear icon next to the container to be made public and
    select **Make Public (Enable CDN)**.
6.  Click **Publish to CDN**.

You can now share the files within the container.

**Upload files to the container**

1.  Click on the name of the container to which you want to upload
    files.
2.  Click **Upload Files** and select the files to upload.
3.  Click **Open**.
4.  After the file is uploaded, click **Close Window**.

The file appears the list of available files within the container.

5.  Click the gear icon next to your file and select **View All Links**.

Options for sharing your file are displayed.

To learn more about how to operate with Cloud Files through the API,
read the article[Connecting to Cloud
Files](https://www.rackspace.com/knowledge_center/article/connecting-to-cloudfiles)
and read the [API Developer Guides](http://docs.rackspace.com/).

Akamai Frequently Asked Questions
---------------------------------

### Who is Akamai?

Akamai Technologies, Inc. is publicly traded: (NASDAQ: AKAM) company
founded in 1998. Akamai has a pervasive, highly-distributed cloud
optimization platform with over 73,000 servers in 70 countries within
nearly 1,000 networks.

### What will I experience when Akamai is implemented as my new CDN provider?

Rackspace expects no customer impact during your transition to Akamai.
Once we flip the switch to have a customer&rsquo;s content served by Akamai,
Akamai will begin supporting both new URLs and all other existing CDN
provider URLs.

This means that CDN customers who currently have Limelight URLs coded
into their websites will continue to serve content using those URLs when
they are transitioned to Akamai, but they will be distributed over the
Akamai network. At this time, we do not have any plans to discontinue
the legacy URLs.

If a customer requests their URL (either in the Control Panel or via
API) for an object, they will be presented with a new Akamai URL. This
does not mean that old URLs are invalid. However, as Rackspace releases
new features like CNAME and SSL, customers will need to reference their
new Akamai URL instead of their legacy URL.

### Will customers have to change their code to use Akamai?

No.

### Will customers have to do anything different in the control panel?

No, as we add new features, we will educate our customers.

### Should customers anticipate any downtime during this implementation?

No downtime is expected during the implementation of the Akamai
platform.

### Will the Cloud Files API be different?

No, all customers facing API calls will remain the same.

What Are The Benefits Of Using a CDN?

[Edit](https://admin.rackspace.com/knowledge_center/node/2188/edit)

### Benefits of a CDN

-   Higher capacity and scale- Strategically placed servers increase the
    network backbone capacity and number of concurrent users handled.
    For instance, when there is a 10 Mbit/s network backbone and 100
    Mbit/s central server capacity, only 10 Mbit/s can be delivered. But
    when 10 servers are moved to 10 edge locations, total capacity can
    be 10\*10 Mbit/s.
-   Lower delivery costs - Strategically placed edge servers decrease
    the load on interconnects, public peers, private peers and
    backbones, freeing up capacity and lowering delivery costs. A CDN
    offloads traffic on a backbone network by redirecting traffic to
    edge servers.
-   Lower network latency and packet loss - End users experience less
    jitter and improved stream quality. CDN users can therefore deliver
    high definition content with high Quality of Service, low costs and
    low network load.
-   Higher Availability - CDNs dynamically distribute assets to
    strategically placed core, fallback and edge servers. CDNs may have
    automatic server availability sensing with instant user redirection.
    CDNs can thus offer 100% availability, even with large power,
    network or hardware outages.
-   Better Usage analytics &ndash; CDNs can give more control of asset
    delivery and network load. They can optimize capacity per customer,
    provide views of real-time load and statistics, reveal which assets
    are popular, show active regions and report exact viewing details to
    customers

### What is a CDN?

A content delivery network (CDN) is a network of computers that delivers
content to users across the globe. By leveraging a network, the content
provider can deliver information quicker to end users across the globe,
while improving performance, and increasing scalability and efficiency.
The place where the content is originally stored is the origin server,
and endpoint servers where users across the globe access the content are
called edge servers. The longer it takes for information to travel from
an edge server to the user, the slower the load time of the content.

The speed of delivery is constrained by the slowest network in the chain
of computers that deliver the content from origin to end user. CDNs
place servers around the world and, depending on where the end user is
located, serves them with the closest or most appropriate server. CDNs
cut down on the amount of travel your content must make. This is shown
in the following figures.\
 ![](/knowledge_center/sites/default/files/field/image/whatisaCDN1.png)\
 \
 ![](/knowledge_center/sites/default/files/field/image/whatisaCDN2.png)\
  

### Technology

CDNs focus on improving performance of web page delivery. CDNs like
Akamai's support progressive downloads, which optimizes delivery of
digital assets such as web page images. CDN nodes and servers are
deployed in multiple locations around the globe over multiple internet
backbones. These nodes cooperate with each other to satisfy data
requests by end users, transparently moving content to optimize the
delivery process. The larger the size and scale of their Edge Network
deployments, the better the CDN.

They generally push the Edge Network closer to end users. The Edge
Network is grown outward from the origins by purchasing co-location
facilities, bandwidth, and servers. CDNs choose the best location for
serving content while optimizing for performance. They may choose
locations that are the fewest hops or fewest number of network seconds
away from the requesting client. CDNs choose the least expensive
locations while optimizing for cost. CDNs use various techniques such as
web caching, server-load balancing, and request routing to achieve the
optimization goals.

Because closer is better, web caches store popular content closer to the
user. These shared network appliances reduce bandwidth requirements,
reduce server load, and improve the client response times for content
stored in the cache.

Server-load balancing uses a web switch, content switch, or multilayer
switch to share traffic among a number of servers or web caches. Here,
the switch is assigned a single virtual IP address. Traffic arriving at
the switch is then directed to one of the real web servers attached to
the switch. This has the advantages of balancing load, increasing total
capacity, improving scalability, and providing increased reliability by
redistributing the load of a failed web server and providing server
health checks.\
 ![](/knowledge_center/sites/default/files/field/image/Technology1.png)

Request routing directs client requests to the content source best able
to serve the request. This may involve directing a client request to the
service node that is closest to the client, or to the one with the most
capacity. A variety of algorithms for Global Server Load Balancing
(shown in diagram) are used to route the request. Choosing the closest
service node is done using a variety of techniques including proactive
probing and connection monitoring.

For more information, see [What are the benefits of using a
CDN?](https://admin.rackspace.com/knowledge_center/index.php/What_are_the_benefits_of_using_a_CDN%3F "What are the benefits of using a CDN?")

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

### General

What are the naming requirements for Cloud Files objects and containers?

[Edit](https://admin.rackspace.com/knowledge_center/node/3465/edit)

The naming requirements for Cloud Files objects and containers (such as
illegal characters and name length limits) include:

-   Container names may not exceed 256 bytes and cannot contain a slash
    (/) character.
-   Object names may not exceed 1024 bytes, but they have no character
    restrictions.
-   Object and container names must be URL-encoded and UTF-8 encoded.

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

File Transfers and File Sharing
-------------------------------

### Does Cloud Files support the transfer of large files?

Yes, the Rackspace Cloud now supports the transfer and storage of larger
files. Following is a list of frequently asked questions about our large
file support.

### How does Rackspace support the upload of large files to Cloud Files?

Although support for uploading content to Cloud Files through the Cloud
Control Panel is limited to files smaller than 5 GB, we can accommodate
the transfer of files larger than 5 GB by allowing you to segment your
files into multiple file segments.

### How large should my file segments be?

Rackspace does not enforce any lower limits on the file size. File
segments cannot be larger than 5 GB, and we recommend not storing file
segments that are smaller than 100 MB.

### Can I serve my large files over the CDN?

At this time, you cannot serve files larger than 10 GB from the CDN.

### Is there a simpler way to use this process?

We have created a tool called Swift to make this process easier. Swift
segments your large file for you, creates a manifest file, and uploads
the segments accordingly. After it uploads the segments, Swift manages
the segments for you, deleting and updating them as needed. You can get
[information about the Swift
Tool](http://docs.openstack.org/developer/swift/) and
[download](https://swiftstack.com/docs/integration/python-swiftclient.html "http://bazaar.launchpad.net/~hudson-openstack/swift/1.2/download/head:/st.py-20100712220340-zzyjabj9xczdm4cg-15/st")
the Swift tool.

### When should I use the API instead of the Swift tool?

If you are interested in developing against the Rackspace Large File
Support code to incorporate into your application, you should work
directly with the Cloud Files API. Use the following steps:

1.  Upload the segments:

    curl -X PUT -H 'X-Auth-Token: \<token\>' \\
    http://\<storage\_url\>/container/myobject/1 --data-binary '1'

    curl -X PUT -H 'X-Auth-Token: \<token\>' \\
    http://\<storage\_url\>/container/myobject/2 --data-binary '2'

    curl -X PUT -H 'X-Auth-Token: \<token\>' \\
    http://\<storage\_url\>/container/myobject/3 --data-binary '3'

2.  Create the manifest file:

    curl -X PUT -H 'X-Auth-Token: \<token\>' \\

    -H 'X-Object-Manifest: container/myobject/' \\
    http://\<storage\_url\>/container/myobject --data-binary ''

3.  Download the segments as a single object:

    curl -H 'X-Auth-Token: \<token\>' \\

    http://\<storage\_url\>/container/myobject

### When should I use the Swift tool instead of the API, and what is the process?

If you want to upload large files but do not want to incorporate our
code into an application, you might find it easier to use the [Swift
tool](https://swiftstack.com/docs/integration/python-swiftclient.html) for
your uploads and management. If you are using the tool, the process
looks as follows:

The following code uploads **large\_file** to **test\_container** in 10
MB segments and then creates the manifest file so the segments can be
downloaded as one.

    swift upload test_container -S 10485760 large_file 

You can change the size of the segments are by changing the value
following the -S option.

The following code downloads the large file as a single object:

    swift download test_container large_file

In the above example, Swift will upload all the segments into a second
container named **test\_container\_segments**. These segments will have
names using the format of
**\<name\>/\<timestamp\>/\<size\>/\<segment\>**. For example:

    large_file/1290206778.25/21474836480/00000000
    large_file/1290206778.25/21474836480/00000001

The main benefit for using a separate container is so the main container
will not be polluted with all the segment names. The naming format is so
that an upload of a new file with the same name won't overwrite the
contents of the first until the last moment when the manifest file is
updated.

For more information on using the swift tool, see the [OpenStack Swift
documentation](http://docs.openstack.org/developer/swift/).

### What will the download experience be like?

After files are segmented and uploaded with a manifest file, your large
file will be served as a single file, so the experience will mimic the
download or service of any other object retrieval.

### Do I have access to my file segments?

Yes, you can edit your file segments just like any other object within
Cloud Files.

### How do I ensure that my files are linked correctly?

Include your manifest file in your upload. You can change your file name
by editing this manifest file as well. We recommend using prefixing in
your file segments to easily map your manifest file to the portions of
your large file. For example, you could name your segments as follows:

        Myfavoritemovie-01
        Myfavoritemovie-02
        Myfavoritemovie-03
        ..etc.. 

In this case, you would point your manifest file to the prefix:
`Myfavoritemovie `.

### Can I use this feature from the Cloud Control Panel?

At this time, Rackspace has not implemented this functionality into the
Rackspace Cloud Control Panel.

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

Application Development
-----------------------

### Where can I find Cloud File Developer Guides?

Developer guides are available on the Rackspace API documentation site.
Documentation is available for the raw API and for language-specific
SDKs.

-   [Cloud Files API Getting Started
    Guide](http://docs.rackspace.com/files/api/v1/cf-intro/content/Introduction-d1e82.html)
-   [Cloud Files API Developer's
    Guide](http://docs.rackspace.com/files/api/v1/cf-devguide/content/Overview-d1e70.html)
-   [Cloud Files Language-specific Software Development
    Kits](http://docs.rackspace.com/sdks/guide/content/intro.html)

[**Back to
Top**](https://admin.rackspace.com/knowledge_center/product-faq/cloud-files#top)

* * * * *

API
---

### Where can I see the API?

The API documentation is available from the [Rackspace API documentation
site](http://docs.rackspace.com/api/).

