---
node_id: 361
title: Installing fwbuilder
type: article
created_date: '2011-03-16'
created_by: Rackspace Support
last_modified_date: '2015-12-30'
last_modified_by: Nate Archer
product: Cloud Servers
body_format: tinymce
---

**Note:** The commands and utilities in this article have been tested on
a Debian Cloud Server. They are not guaranteed to function correctly on
other distributions. However, the [General Package Installation
Guidelines](/howto/general-package-installation-guidelines "General Package Installation Guidelines")
article may assist in "porting" this article to another distro.

**Prerequisites:** [VNC
Install](/howto/vnc-install "VNC Install")

[](){#Introduction}

<span class="mw-headline">Introduction </span>
----------------------------------------------

Fwbuilder is an advanced graphical firewall configuration tool. It is
used to set up complex firewall policies in situations where
command-line scripting tools would simply be too slow or clunky. For
simpler configurations or for users who are newer to Linux, we recommend
our
[iptables](/howto/introduction-to-firewalls)
articles.

[](){#Installation}

<span class="mw-headline">Installation </span>
----------------------------------------------

Fwbuilder may either be downloaded from
[Sourceforge](http://sourceforge.net/project/showfiles.php?group_id=5314&package_id=125359 "http://sourceforge.net/project/showfiles.php?group_id=5314&package_id=125359"){.external
.text} or installed via your Cloud Server's built-in package manager:

    aptitude install fwbuilder

That's it! Connect to your Cloud Server using the instructions in the
VNC or X over SSH articles above, then simply type

    fwbuilder

to launch the application. [](){#Configuration}

-   [Firewall Builder 5 User's
    Guide](http://www.fwbuilder.org/4.0/docs/users_guide5/ "http://www.fwbuilder.org/4.0/docs/users_guide5/"){.external
    .text}


