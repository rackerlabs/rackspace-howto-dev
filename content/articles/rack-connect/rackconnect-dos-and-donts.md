---
node_id: 2053
title: RackConnect v2.0 Best Practices
type: article
created_date: '2012-08-23 17:35:12'
created_by: juan.perez
last_modified_date: '2015-09-04 17:2031'
last_modified_by: constanze.kratel
products: RackConnect
body_format: tinymce
---

undefined&rdquo; to get RackConnect to work with your server.

#### Do not prevent the root user from logging in using Password Authentication via SSH before the completion of the initial RackConnect process

RackConnect does not support key-based authentication, so password
authentication must be allowed for the root user during the RackConnect
automation process.\
 \
 The PermitRootLogin entry must be set to YES in the sshd config file
during the initial process of connecting your Linux Cloud Servers
through RackConnect. After the "rackconnect" user has been added to the
server, and your server is properly deployed with RackConnect, SSH
access by the root user can be disabled because RackConnect uses the
"rackconnect" user from that point forward.

#### Do not modify the standard port used by SSH (Port 22)

If you modify the port number, RackConnect automation breaks. Rackspace
does not have the ability to support non-standard SSH ports at this
time.

#### Do not mount an NFS on a dedicated hosted system before completion of the initial RackConnect process

The RackConnect initial process gives the cloud server access to the
dedicated network, so mounting a network file share before the process
is complete causes the process to fail.

#### **Do not use overly complicated network configurations with RackConnect Cloud Servers**

Complex networking configurations, such as bridged interfaces, will
likely break RackConnect automation.

#### **Do not enable SELinux on RackConnect Cloud Servers**

Rackspace does not currently support Security-Enhanced Linux (SELinux).
If it is enabled, disable it or set it to Permissive mode.

#### Do not remove any basic system utilities like sed, awk, or ip from Linux Cloud Servers

Removing basic system utilities such as sed, awk, or ip can break the
RackConnect automation process.

 

