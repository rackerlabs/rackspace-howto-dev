---
node_id: 268
title: Basic Cloud Server Security
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-30 20:2013'
last_modified_by: kyle.laffoon
products: Cloud Servers
body_format: tinymce
---

undefined&rsquo;ve created.  If not
saved before your server is rebooted, the iptables ruleset will revert
to the default ruleset blocking all traffic except on port 22!

        # sudo /sbin/service iptables save

#### Restarting iptables

Your changes to iptables will not take effect until you save your rules,
and then restart the iptables service.  Remember, if you restart
iptables before saving your rules, iptables will revert to the default
ruleset!

        # sudo /sbin/service iptables restart

Restarting ssh
--------------

Now we'll restart the ssh service.  **Make sure you stay logged in while
you restart ssh and test it with a new connection.**  That way if
something goes wrong you can troubleshoot it more easily.

On most distributions the service is "sshd", and you restart it with the
command:

        # sudo service sshd restart

On Ubuntu and some other distributions it's called "ssh", and is
restarted with a similar command:

        # sudo service ssh restart

If you have trouble making a new connection after restarting ssh, check
the symptoms to see what may be wrong.  If the connection times out,
there may be a problem with the iptables config.  If you get a warning
about a private key, your key may not be installed on the server
properly (check for extra linebreaks or characters that were missed in a
copy and paste operation).  If you've been rebuilding the server then
you may need to [remove the host key from your known hosts
file](http://www.rackspace.com/knowledge_center/checking-ssh-host-fingerprint-with-the-web-console)
before you can make a connection.

If you're locked out...
-----------------------

The incorrect configuration of SSH, sudo and/or iptables could cause you
to be locked out of your system.  If this occurs, please log into the
The Rackspace Cloud Control Panel and use the Web Console or Rescue Mode
to repair the configurations.

 

### Next section

[Creating an Inbound Predefined Allow Rule for Windows Firewall
2008](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-creating-an-inbound-predefined-allow-rule-for-windows-firewall)

