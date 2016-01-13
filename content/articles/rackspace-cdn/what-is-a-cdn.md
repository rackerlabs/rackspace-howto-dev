---
node_id: 120
title: What is a CDN?
type: article
created_date: '2011-03-10 19:09:46'
created_by: RackKCAdmin
last_modified_date: '2016-01-08 22:2148'
last_modified_by: catherine.richardson
products: Rackspace CDN
body_format: tinymce
---

undefined&rsquo;s browser. The speed of delivery is also constrained by the slowest
network in the chain. The solution is a CDN that places servers around
the world and, depending on where the end user is located, serves the
user with data from the closest or most appropriate server. CDNs reduce
the number of hops needed to handle a request. The difference is shown
in the following figures.

#### **Before the Use of a CDN**

-   End user requests www.rackspace.com (origin server) in browser.
-   End user's browser receives content through multiple servers.

![](/knowledge_center/sites/default/files/field/image/CDN-BEFORE_0.png)

 

#### **After the Use of a CDN**

-   End user requests www.rackspace.com (origin server) in browser.
-   End user's browser receives content from the optimum servers.

![](/knowledge_center/sites/default/files/field/image/CDN-AFTER_0.png)

###  

CDNs focus on improving performance of web page delivery. CDNs like the
Akamai CDN support progressive downloads, which optimizes delivery of
digital assets such as web page images. CDN nodes and servers are
deployed in multiple locations around the globe over multiple Internet
backbones. These nodes cooperate with each other to satisfy data
requests by end users, transparently moving content to optimize the
delivery process. The larger the size and scale of a CDN's Edge Network
deployments, the better the CDN.

CDNs generally push the Edge Network closer to end users. The Edge
Network grows outward from the origin server by the addition of
co-location facilities, bandwidth, and servers. CDNs choose the best
location for serving content while optimizing for performance. They may
choose locations that are the fewest hops or fewest number of network
seconds away from the requesting client. CDNs choose the least expensive
locations while optimizing for cost. CDNs use various techniques such as
web caching, server-load balancing, and request routing to achieve the
optimization goals.

-   Because closer is better, web caches store popular content closer to
    the user. These shared network appliances reduce bandwidth
    requirements, reduce server load, and improve the client response
    times for content stored in the cache.
-   Server-load balancing uses a web switch, content switch, or
    multilayer switch to share traffic among a number of servers or web
    caches. In CDNs, the switch is assigned a single virtual IP address.
    Traffic arriving at the switch is then directed to one of the real
    web servers attached to the switch. This has the advantages of
    balancing load, increasing total capacity, improving scalability,
    and providing increased reliability by redistributing the load of a
    failed web server and providing server health checks.

##### Global Server Load Balancing

 

[![](/knowledge_center/sites/default/files/field/image/CDN-thirdIMAGE.png)](#_msocom_4)

-   Request routing directs client requests to the content source best
    able to serve the request. This may involve directing a client
    request to the service node that is closest to the client, or to the
    node with the most capacity. A variety of algorithms for Global
    Server Load Balancing (shown in preceding diagram) are used to route
    the request. Choosing the closest service node is done using a
    variety of techniques including proactive probing and connection
    monitoring.

 

