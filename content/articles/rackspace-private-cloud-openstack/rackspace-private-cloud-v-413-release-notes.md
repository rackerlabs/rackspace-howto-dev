---
node_id: 3798
title: Rackspace Private Cloud v. 4.1.3 Release Notes
permalink: article/rackspace-private-cloud-v-413-release-notes
type: article
created_date: '2013-12-03 20:33:21'
created_by: Karin Levenstein
last_modified_date: '2014-01-16 18:1147'
last_modified_by: jered.heeschen
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

Rackspace Private Cloud v 4.1.3 has the following changes and
documentation. For the full list of known issues and information from
the Rackspace Private Cloud v 4.0 and v. 4.1.2 releases, refer to:

-   [Rackspace Private Cloud v. 4.0 Release
    Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-40-release-notes)
-   [Rackspace Private Cloud v. 4.1.2 Release
    Notes](http://www.rackspace.com/knowledge_center/article/rackspace-private-cloud-v-412-release-notes-0)

Rackspace Private Cloud v 4.1.3 has the following changes.

-   [Cookbook Changes](#cookbook-download-4.1.3 "Cookbook Changes")
-   [Upgrading to v4.1.3 from
    v4.1.2](#upgrade-4.1.3 "Upgrading to v4.1.3 from v4.1.2 in HA Environments")
-   [Upgrading to v4.1.3 on
    CentOS](#upgrade-4.1.3-centos "Upgrading to v4.1.3 on CentOS")
-   [General Changes](#general-4.1.3 "Rackspace Private Cloud Changes")
-   [High Availability](#high-availability-4.1.3 "High Availability")
-   [OpenStack Compute](#openstack-compute-4.1.3 "OpenStack Compute")
-   [OpenStack
    Dashboard](#openstack-dashboard-4.1.3 "OpenStack Dashboard")
-   [OpenStack Image
    Storage](#openstack-image-4.1.3 "OpenStack Image Storage")
-   [OpenStack Metering](#openstack-metering-4.1.3 "OpenStack Metering")
-   [OpenStack
    Networking](#openstack-networking-4.1.3 "OpenStack Networking")
-   [Resolved Issues](#resolved-4.1.3 "Resolved Issues")

Cookbook Changes {.title style="clear: both;"}
----------------

The latest cookbook version number is `v4.1.3`{.filename}. This change
is reflected in the instructions under [Install the Rackspace Private
Cloud
Cookbooks](http://www.rackspace.com/knowledge_center/article/installing-openstack-with-rackspace-private-cloud-tools#install-cookbooks).

Upgrading to v4.1.3 from v4.1.2 in HA Environments {.title style="clear: both;"}
--------------------------------------------------

When upgrading to v4.1.3 from v4.1.2 in HA environments, you will need
to follow this procedure to ensure that the services update correctly.

1.  Edit the environment by changing the
    `do_package_upgrades`{.filename} and `image_upload`{.filename}
    override attributes. This forces the package upgrades and also
    disables image uploading, which enables you to work around issues
    related to Glance.

    ~~~~ {.screen}
        "override_attributes": {
          "osops": {
            "do_package_upgrades": true
          },
          [...]
          "glance": {
            "image_upload": false
          },
          [...]
          }
                            
    ~~~~

2.  On the `ha-controller2`{.filename} node, stop all services except
    for mysql. You will need to wait about 30 seconds for the services
    to stop. The following commands can be used to restart the services.

    ~~~~ {.screen}
    for i in `monit status | grep Process | awk '{print $2}' | grep -v mysql | sed "s/'//g"`;
      do monit stop $i;
    done
                                
    ~~~~

3.  Stop Keepalived on `ha-controller2`{.filename} and wait
    approximately ten seconds for the VIPs to migrate to
    `ha-controller1`{.filename}.
4.  Run chef-client on `ha-controller1`{.filename} to perform the
    upgrade.

    On Ubuntu, you will run chef-client twice:

    ~~~~ {.screen}
    # chef-client

    INFO: Processing mysql_database[create keystone database] action create (keystone::setup line 34)
    ================================================================================
    Error executing action `create` on resource 'mysql_database[create keystone database]'
    ================================================================================
    [sample output truncated]

    # chef-client
                                
    ~~~~

    On CentOS, you will have to run chef-client twice, restart
    Keepalived, and run chef-client again. This is related to a known
    issue

    ~~~~ {.screen}
    # chef-client

    INFO: Processing mysql_database[create keystone database] action create (keystone::setup line 34)
    ================================================================================
    Error executing action `create` on resource 'mysql_database[create keystone database]'
    ================================================================================
    [sample output truncated]

    # chef-client

    INFO: Processing keystone_register[Recreate keystone Endpoint] action recreate_endpoint (openstack-ha::default line 184)
    [sample output truncated]

    # service keepalived restart
    # chef-client
                                
    ~~~~

5.  Run chef-client on `ha-controller2`{.filename}, then on
    `ha-controller1`{.filename}, and finally on the compute nodes.
6.  Restart the services on `ha-controller2`{.filename}. The following
    commands can be used to restart the services.

    ~~~~ {.screen}
    for i in `monit status | grep Process | awk '{print $2}' | grep -v mysql | sed "s/'//g"`;
      do monit start $i;
    done
                                
    ~~~~

7.  Reboot the devices to ensure that the OpenvSwitch module is active.

Upgrading to v4.1.3 on CentOS {.title style="clear: both;"}
-----------------------------

Before upgrading to v4.1.3 from v4.0.0 or v4.1.2 on CentOS, you must
upgrade the kernel on any Controller nodes in your cluster. Log into the
Controller node and execute the following command:

~~~~ {.programlisting}
# rpm -Uvh http://repos.fedorapeople.org/repos/openstack/openstack-grizzly/epel-6/kernel-2.6.32-358.123.2.openstack.el6.x86_64.rpm \
  http://repos.fedorapeople.org/repos/openstack/openstack-grizzly/epel-6/kernel-firmware-2.6.32-358.123.2.openstack.el6.noarch.rpm \
  http://repos.fedorapeople.org/repos/openstack/openstack-grizzly/epel-6/kernel-headers-2.6.32-358.123.2.openstack.el6.x86_64.rpm     
                
~~~~

After the kernel upgrade is complete, reboot the Controller nodes and
upload the v4.1.3 cookbooks. You can then run chef-client on the
Controller nodes to complete the upgrade. You do not need to make any
changes to the environment attributes.

The following changes have been made to Rackspace Private Cloud on
CentOS and RHEL:

-   The chef-client native selinux handling is used, instead of
    restoring selinux contexts explicitly in cookbooks.
-   A patch has been added for amqplib to enable the SO\_KEEPALIVE
    option on sockets, which allows faster failover detection for
    RabbitMQ.

Rackspace Private Cloud Changes {.title style="clear: both;"}
-------------------------------

The following changes have been made to Rackspace Private Cloud:

-   Infrequently used informational messages in Chef runs have been
    converted to debug messages. This reduces the number of extraneous
    messages during a chef-client run.
-   The repository can be searched based on tag in addition to role and
    recipe.
-   Endpoint schema now allow for DNS-based endpoints.
-   Rackspace Private Cloud now uses RabbitMQ 3.x.
-   A new package repository houses the RPCDaemon packages, which
    improves certain HA features.

High Availability {.title style="clear: both;"}
-----------------

The following changes have been made to High Availability in Rackspace
Private Cloud:

-   Changes to Keepalived that enable increased reliability under a
    wider range of circumstances, such as manual failover for
    maintenance, power loss, and network isolation.
-   Issues with lost messages during RabbitMQ failover have been
    resolved.
-   A newer RabbitMQ version provides more robust replication behavior
    for improved active-active HA functionality.
-   OpenStack Networking availability in failure scenarios has been
    increased. The RPCDaemon tool improves OpenStack Networking
    scheduling of DHCP agents and L3 agents.

OpenStack Compute {.title style="clear: both;"}
-----------------

The following changes have been made to the support of OpenStack Compute
(Nova) in Rackspace Private Cloud:

-   Optional SSL support has been added for nova-novncproxy.
-   Template statements for the config files have been added.
-   The following attributes have been added:
    -   max\_age
    -   reserved\_host\_disk\_mb
    -   libvirt\_inject\_password
    -   libvirt\_inject\_partition

OpenStack Dashboard {.title style="clear: both;"}
-------------------

The following changes have been made to the support of OpenStack
Dashboard (Horizon) in Rackspace Private Cloud:

-   New override attributes give the user greater flexibility in
    customizing the Dashboard, including help\_url customization. The
    following example shows an environment override for a custom theme:

    ~~~~ {.programlisting}
        "horizon": {
          "theme": "default",
          "theme_css_update_style": "download_list",
          "theme_css_list": [ "custom_overlay.css" ],
          "theme_css_base": "http://web.example.org/theme_files",
          "theme_image_update_style": "download_list",
          "theme_image_list": [ "custom_logo.png", "custom_favicon.ico" ],
          "theme_image_base": "http://web.example.org/theme_files",
          "config": {
            "template_debug": true
          }
        }
                                
    ~~~~

-   Users can now override the Keystone endpoint that the Dashboard
    uses.
-   `CSRF_COOKIE_SECURE`{.filename} and
    `SESSION_COOKIE_SECURE`{.filename} are enabled when using SSL.
-   Users can turn off password auto-complete in web browsers.

OpenStack Identity {.title style="clear: both;"}
------------------

You can now enable SSL on internal, service, and admin endpoints
individually in a Rackspace Private Cloud environment.

OpenStack Image Storage {.title style="clear: both;"}
-----------------------

Unused Object Storage configurations have been removed from the Image
Storage configuration for when Object Storage is not in use.

OpenStack Metering {.title style="clear: both;"}
------------------

The following changes have been made to the support of OpenStack
Metering (Ceilometer) in Rackspace Private Cloud:

-   Logging defaults to verbose.
-   The verbose and debug configuration options can be overridden
    separately.
-   HA queue awareness improves failover consistency.

OpenStack Networking {.title style="clear: both;"}
--------------------

L3 agent support is now available, which enables floating IPs and
routers. For more information about L3 routing, refer to ["L3 Routing
and NAT" in the OpenStack Networking Administration
Guide](http://docs.openstack.org/network-admin/admin/content/l3_workflow.html).

Known and Resolved Issues {.title style="clear: both;"}
-------------------------

A known issue has been identified regarding upgrades from v4.1.2 to
v4.1.3. Due to race conditions in restarting keepalived, chef-client
failures are expected in the upgrade from v4.1.2 to v4.1.3. On Ubuntu,
you will need to run chef-client twice, and on CentOS you will need to
run chef-client twice and restart keepalived. The procedure for this has
been documented in [Upgrading to v4.1.3 from
v4.1.2](#upgrade-4.1.3 "Upgrading to v4.1.3 from v4.1.2 in HA Environments").

The following issues have been resolved in v4.1.3 of Rackspace Private
Cloud:

-   In some circumstances, the nova-novncproxy web service could provide
    a directory listing. This low-risk security concern has been
    removed.
-   Logging issues in SSL mod\_wsgi services have been fixed.
-   A memcache server sort order issue has been fixed. This issue could
    cause a spurious regeneration of the nova config template, which
    would trigger a service restart.
-   Numerous process matching issues with monit configurations on most
    services have been fixed. These issues could cause monit to fail to
    restart processes correctly.


