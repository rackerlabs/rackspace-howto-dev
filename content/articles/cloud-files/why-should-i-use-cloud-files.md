---
node_id: 1056
title: Why Should I Use Cloud Files?
permalink: article/why-should-i-use-cloud-files
type: article
created_date: '2011-03-28 20:10:43'
created_by: RackKCAdmin
last_modified_date: '2015-09-28 17:1148'
last_modified_by: cat.lookabaugh
products: Cloud Files
body_format: tinymce
---

There are a number of reasons to choose the Cloud Files service over
similar services available in the market.

-   Simplicity of CDN functionality.
-   Utility pricing - paying only for what you use, after you use it.
-   Multiple APIs for developers to choose from.
-   Fast and reliable performance.
-   World class support

 

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 Simplicity](#Simplicity)                                          |
| -   [2 Affordability](#Affordability)                                    |
| -   [3 Flexibility](#Flexibility)                                        |
| -   [4 Superior performance](#Superior_performance)                      |
| -   [5 World Class support](#World_Class_support)                        |
| -   [6 Data Redundancy](#Data_Redundancy)                                |
| -   [7 Security](#Security)                                              |
+--------------------------------------------------------------------------+

### Simplicity

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

### Affordability

Pricing for Cloud Files with CDN is comprised of the amount of total
data you have stored (per GB), and the amount of bandwidth used to serve
the data (outbound bandwidth only, charged per GB to any edge location
on the CDN around the globe). There are no 'per request' fees for CDN.
 The [current pricing for Cloud
Files](http://www.rackspace.com/cloud/cloud_hosting_products/files/pricing/)
can always be found on our website.

 

### Flexibility

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

### Superior performance

Rackspace has built networks with superior performance for years. The
Akamai CDN capability improves the performance further for distribution
of digital content. In short, Akamai can bring data closer to end users
and serve popular content faster.

### World Class support

With Cloud Files world-class free technical support is only a click
away. Live support, with real people is available 24/7. Fanatical
Support is built into the price. Users can get peace of mind knowing
that technical support is just a phone call or online chat away &ndash; at any
time of the day.

 

### Data Redundancy

The Cloud Files storage system is designed to be highly available and
fault tolerant. Cloud Files achieves client data redundancy by
replicating three full copies on different storage nodes. Storage nodes
are grouped in logical Zones within Rackspace datacenters. Zones are
connected to redundant Internet backbone providers and reside on
redundant power supplies and generators. The system has been engineered
in such a way as to continue to by fully functional even in the event of
a major service disruption within a Datacenter. Content on the CDN
provides an additional layer of data redundancy.

 

### Security

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

 

