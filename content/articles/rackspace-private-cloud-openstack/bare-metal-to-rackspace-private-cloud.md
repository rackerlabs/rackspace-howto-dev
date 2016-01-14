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

undefined&rdquo;. Each matcher is based on server specific metadata that
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

