---
node_id: 3151
title: RackConnect v2.0 Operational Limits
type: article
created_date: '2012-10-30 12:59:30'
created_by: juan.perez
last_modified_date: '2016-01-05 22:1721'
last_modified_by: rose.contreras
product: RackConnect
body_format: tinymce
---

**APPLIES TO**: RackConnect v2.0

This article details the recommended RackConnect Operational Limits to
use when building multiple Cloud Servers through the Cloud Servers API.

**IMPORTANT:** These limits are guidelines and might not exactly match
what is possible in your environment. Some variables that can affect the
limits for your environment include:

-   The number of RackConnect network policies that are active in your
    environment
-   The type of Net Devices you are using with RackConnect

For details about the performance capabilities associated with each of
the Network Devices supported by RackConnect, see the [RackConnect
Network Device
Comparison](http://www.rackspace.com/knowledge_center/article/rackconnect-network-device-comparison)
article.

### RackConnect Operational Limits

API Limits

**Maximum Number of Total Cloud Servers connect to RackConnect when
bursting**

The maximum number of cloud servers that you can deploy in your
environment before you can expect to begin receiving consistent
RackConnect deployment failures. If you need to deploy more than this
amount of Cloud Servers, we highly recommend contacting your RackConnect
Support Team first.

**Note:** Not all customer environments (Net Devices) will be capable of
handling 500 active cloud servers adequately.

500

**API: Optimal number of concurrent builds (bursting)**

The maximum number of cloud servers you should burst at the same time.
Exceeding this value might lead to a degradation in performance or to
build errors or failures.

50

**API: Optimal time delay between builds**

The minimum amount of time you should wait between cloud server builds.
This limit applies even between cloud servers built during a single
bursting process. Exceeding this value might lead to a degradation in
performance or to build errors or failures.

3 seconds

**API: Optimal time delay between groups of builds**

After bursting a group of cloud servers, the amount of time you should
wait before bursting another group of cloud servers. The Once All
Deployed time delay signifies that after bursting a group of cloud
servers, you should wait until that group is fully deployed with
RackConnect before attempting to burst another group of cloud servers.

Once All Deployed

Linux Limits

**Total Potential 512 MB Linux Builds Per Hour (bursting 50 at a time)**

The total number of Linux cloud servers that you can expect to build in
an hour by bursting 75 cloud servers, waiting for them to fully deploy
with RackConnect, then immediately bursting 75 more cloud servers,
repeating this same bursting process for a full hour.

150\*

**Potential Time to Build 100 (512 MB) Linux Cloud Servers (bursting 50
at a time)**

The total amount of time that you can expect it to take to build 100
Linux cloud servers by bursting 75 cloud servers, waiting for them to
fully deploy with RackConnect, then immediately bursting 25 more cloud
servers.

40 minutes\*

Windows Limits

**Total Potential 1 GB Windows Builds Per Hour (bursting 50 at a time)**

The total number of Windows cloud servers that you can expect to build
in an hour by bursting 75 cloud servers, waiting for them to fully
deploy with RackConnect, then immediately bursting 75 more cloud
servers, repeating this same bursting process for a full hour.

100\*

**Potential Time to Build 100 (1 GB) Windows Cloud Servers (bursting 50
at a time)**

The total amount of time that you can expect it to take to build 100
Windows cloud servers by bursting 75 cloud servers, waiting for them to
fully deploy with RackConnect, then immediately bursting 25 more cloud
servers.

60 minutes\*

\* These values are estimates and might not always match your results.

Summary of findings
-------------------

-   If you need to create more than 500 cloud servers in your
    RackConnect environment, we recommend contacting your RackConnect
    Support Team first. Because of the time requirements when deploying
    more than 500 Cloud Servers, it might be feasible only in static
    environments that will not change often.
-   For the best results, there should always be a 3-second time delay
    between API build calls when building multiple cloud servers at
    once.
-   For the best results, you should burst no more than 50 cloud servers
    at once (with a 3-second delay between builds), wait for them to all
    go into a RackConnect Deployed status, then burst no more than 50
    more, repeating the same bursting process until the number of cloud
    servers you need is reached.
-   The Once All Deployed time delay signifies that after bursting a
    group of cloud servers, you should wait until that group is fully
    deployed with RackConnect before attempting to burst another group
    of cloud servers.
-   As long as you follow the limits in this article, there should not
    be a significant time difference (normally less than 20 percent)
    between building smaller and larger cloud server flavors.

For more information about using the available APIs, see the following
documentation:

-   -   [Next gen Cloud Servers API
        documentation](http://docs.rackspace.com/api/)
    -   [The RackConnect v2.0
        API](http://www.rackspace.com/knowledge_center/article/the-rackconnect-v20-api)
    -   [How to programmatically determine the RackConnect v2.0
        automation status of your cloud
        servers](http://www.rackspace.com/knowledge_center/article/how-to-programmatically-determine-the-rackconnect-v20-automation-status-of-your-cloud)

 

