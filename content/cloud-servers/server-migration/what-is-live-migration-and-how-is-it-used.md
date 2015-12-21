---
node_id: 4955
title: Live migration overview
permalink: article/what-is-live-migration-and-how-is-it-used
type: article
created_date: '2015-11-24 15:11:50'
created_by: ari.liberman
last_modified_date: '2015-12-11 20:3953'
last_modified_by: kyle.laffoon
products: Cloud Servers
categories: Server Migration
body_format: markdown_w_tinymce
---

<p>Live migration is the process of moving a virtual server from one host hypervisor to another by using virtual memory streaming. A duplicate of the original virtual server is created on another host, in real-time, from the disk contents, right down to the last byte of RAM in use. When the process is ready, the original virtual server is switched to the new one.<br />
&nbsp;<br />
Using live migration means that, where possible, customer workloads can be moved off of a host that needs to be patched and rebooted to a host that is already updated. During live migration, most customers experience no downtime; a small percentage may notice a brief pause in their workloads, but the reult is generally of low impact compared to a full reboot of a host and virtual server.</p>
