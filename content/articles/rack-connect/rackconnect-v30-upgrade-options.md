---
node_id: 5071
title: Rackconnect v3.0 upgrade options
permalink: article/rackconnect-v30-upgrade-options
type: article
created_date: '2015-12-21 17:10:18'
created_by: Rackspace Support
last_modified_date: '2016-01-04 19:1155'
last_modified_by: Nate.Archer
products: RackConnect
body_format: tinymce
---

Customers can now upgrade from RackConnect v2.0 to RackConnect v3.0.
This article explains the upgrade options that are available.

**Note:** Some customers might require software version updates to be
eligible for RackConnect v3.0. Contact your Rackspace Account Manager or
Service Delivery Manager for additional details and to ensure that you
have no other potential issues that would prevent you from upgrading to
RackConnect v3.

Options fo migrating to RackConnect v3.0
----------------------------------------

You can follow on of two paths to upgrade to RackConnect v3.0 from
RackConnect v2.0.

### Upgrade path A

Upgrade path A is ideal for customers who want to run RackConnect v2.0
and RackConnect v3.0 side-by-side. However, this path might require
significant manual effort, depending on the total number of cloud
servers that you have. Following are the requirements and caveats for
this upgrade path: 

-   **An additional cloud account is required for the RackConnect v3.0
    configuration**: This requirement means that any other cloud
    services being used (including your cloud account's Role Based
    Access Control settings) must be re-created on the new cloud account
    used for RackConnect v3.0.\
      
-   **RackConnect v3.0 and v2.0 run in parallel at the same time**:
    RackConnect v3.0 is set up on the same dedicated network devices
    used for RackConnect v2.0, but it does not replace the current
    RackConnect v2.0 configuration. Both v2.0 and v3.0 run in parallel
    without interfering with each other. As a result, you can migrate as
    slowly as necessary while maintaining the ability to communicate
    between RackConnect v3.0 and v2.0 cloud servers.\
      
-   **Each cloud server to be migrated must have a snapshot image taken
    and shared with the new cloud account used for RackConnect v3.0**:
    The snapshot image is saved on the cloud account used for
    RackConnect v2.0 [[KH1]](#_msocom_1) and is shared with the new
    cloud account used for RackConnect v3.0. A data migration must occur
    for Windows devices.\
      
-   **You will lose the existing public and private IP addresses of your
    cloud servers**: Because the server itself isn't being moved, the IP
    addresses assigned to the server on RackConnect v2.0 will *not* be
    migrated with the snapshot image. As a result, the new RackConnect
    v3.0 server replacement can&rsquo;t receive the old IP addresses used by
    the RackConnect v2.0 server. Any necessary changes to your
    applications or environment must take into account the IP address
    changes that will be occurring.\
      
-   **You can test RackConnect v3.0 before fully committing to the
    migration**: You can test v3.0 before you migrate your
    existing infrastructure. You can also migrate devices as quickly
    or as slowly as you like.\
      
-   All RackConnect v2.0-supported images are currently fully compatible
    with this upgrade path.

### Upgrade path B

 

Most customers prefer upgrade path B. It requires, at minimum, a
one-hour maintenance window. However, maintenance window times depend on
the total number of cloud servers that need to be migrated to
RackConnect v3.0. Following are the requirements and caveats for this
upgrade path:

-   **The same cloud accounts are used for both RackConnect v2.0 and
    RackConnect v3.0**: No additional account is necessary.\
      
-   **A configuration freeze is necessary for RackConnect v2.0**: After
    migration has started, RackConnect v2.0 still exists (and allows
    v2.0 cloud servers to communicate as normal), but RackConnect
    automation can&rsquo;t make any v2.0-related changes to your network
    devices or cloud servers. \
      
-   **Your cloud servers keep their original public IP address and
    ServiceNet IP** address: Your server's assigned public IP address is
    kept after you migrate the server to RackConnect v3.0, but the
    address is NAT translated to the server's private IP address (from
    the  cloud network). The ServiceNet IP address remains the same as
    well, but is now used only to communicate with other cloud services
    (such as Cloud Databases and Cloud Monitoring). Your RackConnect
    v3.0 cloud servers will be unable to use their ServiceNet IP address
    to communicate with your other cloud servers or dedicated servers;
    the cloud network IP address is used to accomplish this in
    RackConnect v3.0. \
      
-   You *cannot* create or delete RackConnect v2.0 cloud servers.\
      
-   You *cannot* make changes to your RackConnect v2.0 Network Policy
    rules during the migration.\
      
-   You *can* create new RackConnect v3.0 cloud servers.\
      
-   **After the upgrade maintenance process starts, it should be
    completed in one batch**: The upgrade *can* occur in multiple
    batches upon request, but the configuration freeze for RackConnect
    v2.0 must be in place for the entire process (until the upgrade is
    complete)*. *

Next step
---------

After you determine which upgrade option best meets your needs, call
your Account Manager or Server Delivery Manager to being the migration
process. Also, your Account Manager can schedule a call with one of our
RackConnect specialists to answer any outstanding questions that you
might have.

