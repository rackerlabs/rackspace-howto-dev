---
node_id: 4387
title: Cloud server name transitions
type: article
created_date: '2014-10-28 18:10:40'
created_by: TFDuesing
last_modified_date: '2014-11-05 16:1700'
last_modified_by: kyle.laffoon
products: Cloud Servers
body_format: tinymce
---

Rackspace has recently changed the names of the flavors that you can
choose when creating cloud servers. The goal of this change is to
simplify flavor selection by aligning the flavor names with the intended
workloads. The old flavor names are officially deprecated but will still
be recognized in API commands for a time. The new names are the only
flavor names visible in the Cloud Control Panel.

The following table maps the old flavor names to the new ones. 

  ---------------------------------------------------------
  Previous flavor\   Current virtual\     OnMetal flavor\
   class name         flavor class name    class name
  ------------------ -------------------- -----------------
  Standard           Standard              

  Performance 1      General Pupose        

  Performance 2      I/O Optimized        OnMetal I/O

                     Compute Optimized    OnMetal Compute

                     Memory Optimized     OnMetal Memory
  ---------------------------------------------------------

The new flavor names also reflect new functional differences. We now
offer servers that are optimized for memory, compute, and I/O.
Additionally, the General Purpose servers (which were previously
Performance 1) can have a larger system disk instead of using split
system and data disks.

The different types of servers are part of the expected growth life
cycle of using cloud servers. That life cycle goes from general purpose
virtual servers to workload-optimized virtual servers to
workload-optimized OnMetal servers. For more information about this
cloud server life cycle, see the graphic on the [Cloud
Servers](http://www.rackspace.com/cloud/servers/) product page.

