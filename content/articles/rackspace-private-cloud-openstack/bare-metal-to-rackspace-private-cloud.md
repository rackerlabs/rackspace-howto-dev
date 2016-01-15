---
node_id: 3271
title: Bare Metal to Rackspace Private Cloud
type: article
created_date: '2013-01-24 17:59:56'
created_by: alyssah
last_modified_date: '2014-05-15 19:5523'
last_modified_by: rose.contreras
product: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

Overview
--------

Combining Razor and Chef provides a powerful, fully automated solution
for deploying Rackspace Private Cloud Software (RPCS) on bare metal.
Using this deployment system, the installation of a customized OpenStack
environment across multiple servers can start as fast as they come
online. 

![](/knowledge_center/sites/default/files/field/image/deploymentsystem-razor.png)

Razor and Chef
--------------

Razor is an automated provisioning tool that is very easy to use and is
geared towards installing and managing servers. Razor automatically
detects servers that need to be installed and based on policy will
install an OS. Finally, Razor hands the servers off to a DevOps tool
(Chef) for further configuration. Chef is a configuration management
system that allows you to treat infrastructure like code, thereby
enabling flexible management at cloud scale. Where Chef is great as a
configuration management tool, Razor fills in the gap that exists in
bringing systems from first boot into the configuration management
space.

For more information:

**Razor:**
[https://github.com/puppetlabs/puppetlabs-razor](https://github.com/puppetlabs/puppetlabs-razor)

**Chef:** [http://www.opscode.com/chef/](http://www.opscode.com/chef/)

 

Getting Started
---------------

To install Razor, follow the installation guide at Razor project wiki
(https://github.com/puppetlabs/Razor/wiki/Installation). Note that your
Razor installation will require a DHCP server as part of the setup. Once
Razor is installed and running, you may proceed with configuring Razor
to deploy RPCS.

After installing Razor, set it up to install your preferred OS on
servers that come online. To help with the installation process itself,
Razor uses a Microkernel, or the MK, that boots from the network and
lives in memory until a real target operating system can be installed.
The MK is a Tiny-Core Linux based, and is used on first boot and as the
default boot image for any nodes. Doing this allows Razor to collect
data on the node (similar to Chef&rsquo;s ohai) which is then used in tagging
and policies.

Add an MK as your first image to Razor so that it knows how to boot a
server (refer to MK documentation for more information on how it works:
[https://github.com/puppetlabs/Razor-Microkernel/wiki](https://github.com/puppetlabs/Razor-Microkernel/wiki)

    $ razor image add -t mk p ~/images/rz_mk_prod-image.0.9.3.0.iso

*Note: 0.9.3.0 is the current version of the Microkernel at the time of
this writing. You will want to ensure your MK is current when deploying
Razor.*

Once the MK image is added, you will need to add an actual OS that is
going to be installed on the nodes. We are using Ubuntu Precise Pangolin
image for our example:

    $ razor image add -t os p ~/images/ubuntu-12.04.1-server-amd64.iso -n ubuntu_12.04 -v 12.04

*Note: You can provide multiple images, versions, and different
distributions of Linux (and soon Windows) to Razor. These in turn can be
applied to nodes using different policies.*

Each OS requires its own model setup in Razor. Models manage OS related
data, we are going to create &ldquo;ubuntu\_precise&rdquo; model. While creating the
model, use the UUID from previous command here:

    $ razor model add -t ubuntu_precise -l install_precise -i  

Create a policy for servers with two CPUs and 8 GB of memory:

    $ razor policy add &ndash;t linux_deploy -l precise -m  -t cpus_2,memsize_8GiB -e true 

*Note: You can find additional tags for your nodes that razor has
discovered by using the &lsquo;razor node&rsquo; command.*

At this point, you are ready to do automated installs, but not yet ready
for the automated hand off to Chef. To fix this, create a Chef broker
and then add it to the policy we created. 

 

Razor Chef Broker
-----------------

The Razor broker manages handoffs between Razor and a DevOps system,
like Chef or Puppet. Since we are using Chef, we need a Chef broker. In
Razor, the broker takes over at the end of the OS installation, and
executes predefined additional steps. The Chef broker will do the
following:

1. Install chef-client on the node.

2. Create /etc/chef/validation.pem file.

3. Create basic /etc/chef/client.rb file with client settings.

4. Inject custom Razor metadata into the new node.

5. Execute initial run list.

The following command displays available brokers in Razor:

    $ razor broker get plugins

Create a new broker to use for private cloud deployments:

    $ razor broker add -p chef -n Chef -d PrivateCloud

Here, you will be prompted to answer a few questions about your Chef
setup. When in doubt about the different options that need to be set,
refer to this step-by-step guide on how to set up Chef broker:
[http://anystacker.com/2012/12/razor-chef-broker-updated/](http://anystacker.com/2012/12/razor-chef-broker-updated/)

After setting up a new broker, add it to the policy:

    $ razor policy update  -b

This is what newly created broker will look like:

    [Policy] [update_policy]
     Line Number => 3
     Label => precise
     Enabled => true
     Template => linux_deploy
     Description => Policy for deploying a Linux-based operating system.
     Tags => [cpus_2, memsize_8GiB]
     Model Label => install_precise
     Broker Target => Chef
     Currently Bound => 1
     Maximum Bound => 0
     Bound Counter => 1

Now, any new node that matches this policy will go trough a hand off to
Chef server.

** **

Setting up Chef Server
----------------------

In order to make large Rackspace Private Cloud deployments possible, you
will need to have Chef server set up with search functionality enabled.
Use your server to host cookbooks and make it accessible to all new
nodes that try to register with it. Roles and cookbooks for RPCS were
designed in such a way that they can be used to deploy anything from
single all-in-one server to multi-node installations. Get them here:
[https://github.com/rcbops/chef-cookbooks/](https://github.com/rcbops/chef-cookbooks/)

Once you have them available, you are ready to start deploying! 

 
-

Private Cloud Roles
-------------------

After OS is installed on your new node, you have several different
options to install RPCS on it. If you need just one node, do it by hand,
and execute the following:

    $ knife node run_list add node1 role[allinone]

This will install an all-in-one OpenStack. Individual nodes can be
installed the same way, by using different roles. For example:

Install a controller node by adding &ldquo;single-controller&rdquo; role to its
run\_list:

    $ knife node run_list add <controller_node_name> &lsquo;role[single-controller]&rsquo;

Install a compute node by adding &ldquo;single-compute&rdquo; role to its run\_list:

    $ knife node run_list add <compute_node_name> &lsquo;role[single-compute]&rsquo;
    $ chef-client

As soon as we run the chef-client on compute node, cookbooks use Chef
search feature to locate the node with the rabbit role or mysql role for
instance and set the appropriate IP in its nova.conf file. Therefore, it
is important to make sure that the controller node is finished prior to
adding the single-compute role to compute nodes. Likewise multiple nodes
can be added to compute nodes to a controller and form a Private Cloud
Cluster.

Some of the important roles and recipes:

Role[single-controller] &ndash; executes the below mentioned roles one by one:

    run_list(
      "role[base]",
      "role[mysql-master]",
      "role[rabbitmq-server]",
      "role[keystone]",
      "role[glance-registry]",
      "role[glance-api]",
      "role[nova-setup]",
      "role[nova-scheduler]",
      "role[nova-api-ec2]",
      "role[nova-api-os-compute]",
      "role[cinder-all]",
      "role[nova-cert]",
      "role[nova-vncproxy]",
      "role[horizon-server]"
    ) 

Role[single-compute] &ndash; executes the below listed roles one by one:

    run_list(
      "role[base]",
      "recipe[nova::compute]"
      &ldquo;recipe[nova::nova-network]&rdquo;
    )

Users can update the run\_list and design the private cloud cluster in
the order they want it to be. 

 
-

Fully Automating the Deployment
-------------------------------

While running knife commands on each individual server is easy enough,
it would be even easier if this task was automated. Razor is capable of
passing a list of roles to the server at the time of hand off. Lets say
you needed to automatically provision a lot of servers with all-in-one
OpenStack installations for your test systems. You may achieve this by
running the knife command on all servers for all-in-one role:

    $ knife node run_list add node1 role[allinone]

In order for the Razor to do this for you, create a new Chef broker to
include the run list:

    Name =>  Chef
    Description =>  allInOne
    Plugin =>  chef
    UUID =>  23PjqYKm915c19EPTNRrKF
    Chef Server URL =>  https://chef.example.com:4000
    Chef Version =>  10.16.2
    Validation Key MD5 Hash =>  186f28af3fa82b2760f7e028dbbdbe0c
    Validation Client Name =>  chef-validator
    Bootstrap Environment =>  _default
    Install Sh Url =>  http://opscode.com/chef/install.sh
    Chef Client Path =>  chef-client
    Base Run List =>  role[allinone]

Associate this broker with the Razor policy used to deploy your test
environments, and the all-in-one Chef roles will be installed on the new
node after it connects to the system. 

Similarly, servers dedicated to a different type of node, can have a
different broker set up. For example, dedicated Volume nodes can be set
up with the appropriate Cinder specific run list. After checking what
roles are used to deploy Cinder node on Rackspace Cloud Builders github,
[https://github.com/rcbops/chef-cookbooks/blob/master/roles/cinder-all.rb](https://github.com/rcbops/chef-cookbooks/blob/master/roles/cinder-all.rb),
add the list of roles to a new broker:

    Name =>  Chef
    Description =>  cinderAll
    Plugin =>  chef
    UUID =>  4kJh3byJFKavzyhzXOuCMF
    Chef Server URL =>  https://chef.example.com:4000
    Chef Version =>  10.16.2
    Validation Key MD5 Hash =>  c8c76aa7967f727be89445681536d71f
    Validation Client Name =>  chef-validator
    Bootstrap Environment =>  _default
    Install Sh Url =>  http://opscode.com/chef/install.sh
    Chef Client Path =>  chef-client
    Base Run List =>  role[base], role[cinder-setup], role[cinder-api], role[cinder-scheduler], role[cinder-volume]

Once the new broker is setup, repeat the process of setting up model and
policy that would define cinder-specific storage. You can differentiate
Cinder servers from Compute servers using tags based on hardware
attributes. Razor tags are labels that can be applied to one or more
node. If you create a Cinder policy for a server that has 16 GB ram and
2 hard disks, new servers matching the specifications will be installed
as Cinder nodes anytime they come online.

Create Cinder specific tags for this example. Add the tag, followed by
tag &ldquo;matchers&rdquo;. Each matcher is based on server specific metadata that
Razor Microkernel collects. 

    $ razor tag add -n cinderTags -t cinderName =>  cinderTagsTags =>  cinderUUID =>  2u7LG7s8JFBNl3cVdTsjwpMatcher =>  

If disk one is equal to 2048 GB:

    $ razor tag 2u7LG7s8JFBNl3cVdTsjwp matcher add -k mk_hw_disk0_size -c equal -v 2048

If disk two is equal to 4096 GB:

    $ razor tag 2u7LG7s8JFBNl3cVdTsjwp matcher add -k mk_hw_disk1_size -c equal -v 4096

If memory is 16 GB:

    $ razor tag 2u7LG7s8JFBNl3cVdTsjwp matcher add -k mk_hw_mem -c equal -v 16

After adding matchers, your new tag should be similar to this:

    $ razor tag 2u7LG7s8JFBNl3cVdTsjwp Name =>  cinderTagsTags =>  cinderUUID =>  2u7LG7s8JFBNl3cVdTsjwpMatcher =>  53EDDNpiGbAANeVmutpnSF - 'mk_hw_disk0_size' (equal) '2048'5cHU5UUfN6iGzJRCZIghUJ - 'mk_hw_disk1_size' (equal) '4096'1pRkngGTTUa8Hu91WinQZP - 'mk_hw_mem' (equal) '16'

With tags created, create a new policy:

    $ razor policy add -p linux_deploy -l Cinder -m 2dz79YGAQkgn6iqOHBGNtr -b 4kJh3byJFKavzyhzXOuCMF -t 2u7LG7s8JFBNl3cVdTsjwp -e true Policy createdUUID =>  3qMLRURZwfWECBvD1aHQ0pLine Number =>  1Label =>  CinderEnabled =>  trueTemplate =>  linux_deployDescription =>  Policy for deploying a Linux-based operating system.Tags =>  [2u7LG7s8JFBNl3cVdTsjwp]Model Label =>  install_preciseBroker Target =>  ChefCurrently Bound =>  0Maximum Bound =>  0Bound Counter =>  0

After all this setup, our new policy is ready to install Cinder on all
servers that have 2 disks, sized 2 and 4 TB, and 16 GB of memory. While
this is just an example, you can see where and how to build upon it to
deploy your own Private Cloud.

 

Automating the Automated Deployment
-----------------------------------

Razor makes full automation simple by providing full RESTful APIs. If
you have a Chef recipe that takes in different configurations, you can
create models, policies, and tags through Razor API. With all the steps
automated, it takes the same amount of time to deploy 20 individual
clusters as it would take one. Deployment model similar to this is used
at Rackspace. Quality engineering teams use a combination of Razor,
Chef, and Jenkins to run a full suite of automated tests on RPCS. Tests
include integration, functional, and capacity testing on bare metal as
well as virtualized environment. 

Other business systems can track assets and their assignment to business
units. Utilizing the flexible provisioning engine from Razor and Chef,
you can repurpose gear from one deployment to another. In this way, IT
departments can gain greater flexibility with changing requirements and
agility to keep up with the speed of business demands.

 

Conclusion
----------

There are many ways to provision hardware and software, but larger
installations require more automated solutions. Razor and Chef make a
perfect combination for deploying RPCS onto bare metal, while requiring
very little setup.
