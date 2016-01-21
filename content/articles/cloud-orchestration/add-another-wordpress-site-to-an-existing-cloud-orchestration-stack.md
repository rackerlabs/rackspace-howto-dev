---
node_id: 3810
title: Add another WordPress site to an existing Cloud Orchestration stack
type: article
created_date: '2013-12-13'
created_by: Jered Heeschen
last_modified_date: '2016-01-12'
last_modified_by: Stephanie Fillmon
product: Cloud Orchestration
---

This tutorial walks through the process of manually adding another
WordPress site to an existing WordPress Cloud Orchestration stack on
Cloud Servers. Note that in most situations, it's better to create a new
WordPress stack for each site. This allows for better performance,
security, and scalability, and is much easier to manage. Furthermore,
creating a new WordPress stack is a simple process involving just a few
clicks through the Cloud Control Panel. Adding a site to an existing
stack requires changes to the configurations for multiple services. The
effort may be acceptable when the existing stack runs well under
capacity or when you're trying to minimize the number of server
instances you maintain. \#\#\# Connect to the backend (database) server
1. Log in to the \[Cloud Control Panel\](http://mycloud.rackspace.com).
2. In the top navigation bar, click \*\*Orchestration &gt; Stacks\*\* to
view the list of existing stacks.
<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/orchestration-nav.png" width="479" height="131" />
3. From the Stacks list, click on the name of the stack to which you
want to add a WordPress site. 4. From the list of servers, click the
name of the "backend" server to view its details page. On the backend
server's detail page, you will find the PublicNet IP address in the
Networks section. \*\*Note:\*\* If "backend" does not appear on your
server list, find details for "database". "Database" acts as your
backend server. 5. Use the public IP address from the server details
page and the private key provided when the stack was created to connect
to the backend server with SSH. ssh user@ -i /path/to/key If you do not
have the private key, you can reset the backend server's root password.
For help connecting to your server via SSH, see the articles on using
SSH with a private key in our Knowledge Center for \[Mac and
Linux\](http://www.rackspace.com/knowledge\_center/article/logging-in-with-an-ssh-private-key-on-linuxmac)
or
\[Windows\](http://www.rackspace.com/knowledge\_center/article/logging-in-with-an-ssh-private-key-on-windows).
\#\#\# Database Setup 1. After logging in, run the \`\`\`mysql\`\`\`
command to connect to MySQL. mysql 2. Create a database for the new
WordPress site with the \`\`\`create database\`\`\` command in the MySQL
shell. For this example we'll call the site "blogsrock.rackspace.com".
create database blogsrock\_rackspace\_com; 3. Create a user and password
for this site. Please use a strong password (not like the one in this
tutorial). grant all on \`blogsrock\_rackspace\_com\`.\* to
'blogsrock'@'localhost' identified by 'mystrongpassword'; 4. Grant
access for this user when connecting from our web servers. For this
tutorial we are going to grant access to all \`10.x.x.x\` IP addresses;
however, for additional security, you can replace this with the specific
ServiceNet IP addresses of your web servers. grant all on
\`blogsrock\_rackspace\_com\`.\* to 'blogsrock'@'10.%' identified by
'mystrongpassword'; 5. When you are finished, type \`exit\` to leave
MySQL and type \`exit\` again to disconnect from the backend server.
\#\#\# WordPress Setup Now that the database is ready, we can begin
installing WordPress on the master node. 1. From the stack's detail
page, click the link for the "master" server.
<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/cpdeploymentsmasterlist.png" alt="List of stacks with the backend node highlighted" width="600" />
On the master server's detail page, you will find the PublicNet IP
address in the Networks section. 2. Use the IP address and private key
to connect to the server via \`ssh\`. ssh user@ -i /path/to/key 5. Use
\`wget\` to download the latest WordPress tarball. wget
http://wordpress.org/latest.tar.gz 12. Download a script called
\[wordpress-cli-installer\](https://github.com/nexcess/wordpress-cli-installer)
that we will use later to simplify the final steps of the WordPress
setup. wget
https://raw.github.com/nexcess/wordpress-cli-installer/master/wordpress-cli-installer.sh
3. Navigate to the web server's data directory. cd /var/www/vhosts The
directory should contain subdirectories for any WordPress sites that are
already configured on the server. 4. Make a new directory for the new
site, with WordPress subdirectories. sudo mkdir -p
blogsrock.rackspace.com/{conf,http\_docs,.ssh} The new directory should
contain subdirectories named \`conf\`, \`http\_docs\`, and \`.ssh\`. \$
ls -l blogsrock.rackspace.com total 20 drwxr-xr-x 5 root root 4096 Dec 3
16:23 ./ drwxr-xr-x 4 root root 4096 Dec 3 16:23 ../ drwxr-xr-x 2 root
root 4096 Dec 3 16:23 conf/ drwxr-xr-x 2 root root 4096 Dec 3 16:23
http\_docs/ drwxr-xr-x 2 root root 4096 Dec 3 16:23 .ssh/ 5. Extract the
WordPress tarball you downloaded earlier to the \`http\_docs\`
directory. sudo tar --strip-components 1 -xvzf \~/latest.tar.gz -C
http\_docs/ 6. Change to the http\_docs directory. cd http\_docs/ The
extracted WordPress files should be present, including the
wp-config-sample.php file. 7. Copy the wp-config-sample.php file to make
a new WordPress config file. sudo cp wp-config-sample.php wp-config.php
8. Edit the new configuration file and add some extras to help with file
permissions and load balancing. For HTTP-only sites, you can easily make
the necessary changes by running, all on one line: sudo bash -c "echo -e
"define('FS\_METHOD', \\"direct\\");\\ndefine('FS\_CHMOD\_DIR', (02775 &
\~umask()));\\ndefine('FS\_CHMOD\_FILE', (0664 & \~
umask()));\\ndefine('FORCE\_SSL\_ADMIN', false);\\nif (
isset(\\\$\_SERVER\['HTTP\_X\_PROXY\_PROTO'\]) &&
\\\$\_SERVER\['HTTP\_X\_PROXY\_PROTO'\] == 'HTTPS' ) {
\\\$\_SERVER\['HTTPS'\] = 1; }" &gt;&gt; wp-config.php" If you are
running an HTTPS site, run this command instead: sudo bash -c "echo -e
"define('FS\_METHOD', \\"direct\\");\\ndefine('FS\_CHMOD\_DIR', (02775 &
\~umask()));\\ndefine('FS\_CHMOD\_FILE', (0664 & \~
umask()));\\ndefine('FORCE\_SSL\_ADMIN', true);\\nif (
isset(\$\_SERVER\['HTTP\_X\_PROXY\_PROTO'\]) &&
\\\$\_SERVER\['HTTP\_X\_PROXY\_PROTO'\] == 'HTTPS' ) {
\\\$\_SERVER\['HTTPS'\] = 1; }" &gt;&gt; wp-config.php" 9. Generate new
secure keys using the WordPress API. curl -q
https://api.wordpress.org/secret-key/1.1/salt/ You should get some
output like this: define('AUTH\_KEY',
'V}zrS|PsyH3\]!p!AEufS{7:Jjy);(ooKx/aG-S6VWcpd3D47zc3Xr\~2=.W3|Yfw:');
define('SECURE\_AUTH\_KEY',
'w1|o-0:5i};kj&V1SY}2O\[2MGTwo8NhoI2+Gmj!qDgG&lt;\~1A+\*,DAQ?\^0xO\_&g%se');
define('LOGGED\_IN\_KEY',
'Ce6g&gt;+OA\$u+-H5\`/ZU|f\#\`=J,rb!.-\^ayr20jG.BF\$Q7q&gt;\]G&lPG
nTS\^Ox\*mMET'); define('NONCE\_KEY',
'G\$Or)@Rp%Im\#eezD{P.P\[/eMv9q\_wNe+.GVt|
y,rN\~sA;\`y@UY76S|J\[p7-n\*s&'); define('AUTH\_SALT',
'\$iPgS\$t\^,h!=YSW0ju\*jqmk!@eLAno4u'); define('SECURE\_AUTH\_SALT',
'ciy\$1-c\^X-mkb&lt;2ULD7+ua;\_kjd9ku&:bZX&gt;}B-GnI5ITu\`(q)\]3{p\#TQ)-:\`w@c');
define('LOGGED\_IN\_SALT',
'VE\]+84A?6Qen-p\`iuthBw;Cqh:z2-9)Rdcw2AY\_7?W;D\`W5T7ATmJHrK\~}-1\`e2E');
define('NONCE\_SALT',
'XV}nFzYqXJ}jr)tD2vZ\`-|!w\]f&gt;3;\*\`?\#U8\*l(C:/\*)w.cf}6i{Adw@,Yj7p(F?d');
10. Edit the wp-config.php file to replace the default keys with the
keys generated in the previous step. sudo nano wp-config.php Replace
\`nano\` in that command with your text editor of choice. 11. Edit the
wp-config.php file to replace the default database values with the
database name, username, and password created in the previous section.
The relevant section of the configuration file looks like this: // \*\*
MySQL settings - You can get this info from your web host \*\* // /\*\*
The name of the database for WordPress \*/ define('DB\_NAME',
'database\_name\_here'); /\*\* MySQL database username \*/
define('DB\_USER', 'username\_here'); /\*\* MySQL database password \*/
define('DB\_PASSWORD', 'password\_here'); /\*\* MySQL hostname \*/
define('DB\_HOST', 'localhost'); For the \`DB\_HOST\` value, replace
\`localhost\` with the ServiceNet IP address of the backend server. 13.
Run \`wordpress-cli-installer\`, passing it arguments for the site's
base URL, title, admin email address, and WordPress location. sudo sh
\~/wordpress-cli-installer.sh -b 'http://blogsrock.rackspace.com' -T
'BLOGS ROCK' -e 'admin@example.com'
/var/www/vhosts/blogsrock.rackspace.com/http\_docs/ \#\#\# System Setup
Now we'll make some changes to the system to accommodate the new
WordPress site. 1. Create a new user for the site, setting the user's
home directory to the new site's directory. For example: sudo useradd -M
-d /var/www/vhosts/blogsrock.rackspace.com -p 'mystrongpassword' -s
'/bin/bash' -U -G www-data wp\_user2 2. Set up a new SSH key-pair for
\`lsyncd\` connections between the master and backend nodes in the new
user's \`.ssh\` directory. cd .ssh sudo ssh-keygen -f id\_rsa.lsyncd
sudo mv id\_rsa.lsyncd.pub authorized\_keys 3. Change to the conf
subdirectory of the new site. cd
/var/www/vhosts/blogsrock.rackspace.com/conf/ 4. Copy any configuration
files for the existing WordPress site to the new directory. sudo cp
/var/www/vhosts/iloveblog.rackspace.com/conf/\*
/var/www/vhosts/blogsrock.rackspace.com/conf/ 5. Change the name of the
new config file to match the new site. sudo mv
iloveblog.rackspace.com\_\_http.conf
blogsrock.rackspace.com\_\_http.conf If your site supports HTTPS you'll
also need to rename the copied HTTPS configuration file. sudo mv
iloveblog.rackspace.com\_\_https.conf
blogsrock.rackspace.com\_\_https.conf 6. Edit the configuration file to
use the domain name of the new site in place of the existing site. sudo
sed -i 's/iloveblog.rackspace.com/blogsrock.rackspace.com/g'
blogsrock.rackspace.com\_\_http.conf If your site supports HTTPS you'll
need to make the same change to the HTTPS file. sudo sed -i
's/iloveblog.rackspace.com/blogsrock.rackspace.com/g'
blogsrock.rackspace.com\_\_https.conf 7. If your site supports HTTPS,
you will need to change the SSL certificate being used in the new
"https" file to point to the SSL certificate for the new site. Specific
instructions for this step are beyond the scope of this tutorial. 8. Set
appropriate permissions for all the new site's directories and files.
Replace \`wp\_user2\` with the name of the user you created for the site
in the System Setup section of this tutorial. cd
/var/www/vhosts/blogsrock.rackspace.com/ sudo chown -R
wp\_user2:www-data http\_docs sudo chown -R wp\_user2:wp\_user2 conf
.ssh sudo chmod -R ug=rwX,o=rX http\_docs sudo chmod u+s http\_docs sudo
find http\_docs/ -type d -exec chmod u+s {} \\; sudo chmod -R u=rwX,go=
.ssh \#\#\# Apache Setup Next we need to create an Apache virtual host
configuration file for the new site. 1. Change to Apache's
sites-available directory. cd /etc/apache2/sites-available 2. Copy the
existing site's configuration file for the new site. sudo cp
iloveblog.rackspace.com.conf blogsrock.rackspace.com.conf 3. Edit the
new virtual host configuration file to change any domain references for
the new site. sudo sed -i
's/iloveblog.rackspace.com/blogsrock.rackspace.com/g'
blogsrock.rackspace.com.conf \#\#\# Varnish Setup Just like Apache, we
need to copy the existing site's varnish configuration to a new file and
change the domain name it looks for as well. 1. Change to the Varnish
include directory. cd /etc/varnish/include/ 2. Copy the existing site's
configuration file for the new site. sudo cp
iloveblog.rackspace.com\_.vcl blogsrock.rackspace.com\_.vcl 3. Edit the
new virtual host configuration file to change any domain references for
the new site. sudo sed -i
's/iloveblog.rackspace.com/blogsrock.rackspace.com/g'
blogsrock.rackspace.com\_.vcl \#\#\# Lsyncd setup Now we need to add the
new site to our lsyncd configuration so that the master server knows to
push content for the new site to the slave servers. 1. Change to the
lsyncd configuration directory. cd /etc/lsyncd/ 2. Open the
lsync.conf.lua file for editing to add a node for the new site. sudo
nano lsync.conf.lua Replace \`nano\` in that command with your text
editor of choice. 3. For each slave server in the WordPress stack, make
a new \`sync\` section, changing the \`source\` value to match the new
site, the \`target\` value to match the new system user, and changing
the directory reference in the \`excludeFrom\` value. The
\`lsync.conf.lua\` file consists of a \`settings\` section followed by
one or more \`sync\` sections, one for each slave site. Since our
example stack only has one slave, we only have to add one new \`sync\`
section. You can copy the existing \`sync\` section then modify the
directory references and username in the new section to match the new
site. For our example site, the edited file looks like this: settings =
{ logfile = "/var/log/lsyncd/lsyncd.log", statusFile =
"/var/log/lsyncd/lsyncd-status.log", statusInterval = 5, pidfile =
"/var/run/lsyncd.pid" } sync{ default.rsync,
source="/var/www/vhosts/iloveblog.rackspace.com/http\_docs",
target="wp\_user@:/var/www/vhosts/iloveblog.rackspace.com/http\_docs",
excludeFrom="/etc/lsyncd/lsyncd.exclude", rsyncOps={"-rlpgoDvz", "-e",
"/usr/bin/ssh -i
/var/www/vhosts/iloveblog.rackspace.com/.ssh/id\_rsa.lsyncd -o
StrictHostKeyChecking=no"} } sync{ default.rsync,
source="/var/www/vhosts/blogsrock.rackspace.com/http\_docs",
target="wp\_user2@:/var/www/vhosts/blogsrock.rackspace.com/http\_docs",
excludeFrom="/etc/lsyncd/lsyncd.exclude", rsyncOps={"-rlpgoDvz", "-e",
"/usr/bin/ssh -i
/var/www/vhosts/blogsrock.rackspace.com/.ssh/id\_rsa.lsyncd -o
StrictHostKeyChecking=no"} } \#\#\# Slave Setup Next, we need to create
the new user on each slave node in order to prepare for the new site. To
do this, we are going to setup the stack's SSH key (the one we used to
log in to each node) on the master server and use \`pssh\` to make the
process faster. 1. If you aren't already on the root account, switch to
a root shell to execute privileged commands and use root's SSH keys.
sudo su - root 1. Edit root's private key file to add the stack's SSH
private key. nano \~/.ssh/id\_rsa Replace \`nano\` in that command with
your text editor of choice. 2. Add the stack's SSH private key to the
file and save the change. If the file isn't empty, add the key on a new
line at the end of the file. 3. Change permissions on the key file so
only root can access it. chmod 600 \~/.ssh/id\_rsa 4. Install \`pssh\`
on the master server. apt-get update apt-get install pssh 4. Run pssh to
add the new user to each slave server. Note that the \`-H\` flag here is
only used once, but you should repeat it for each additional slave node
you have. parallel-ssh -P -H -x "-o StrictHostKeyChecking=no -o
UserKnownHostsFile=/dev/null -o GlobalKnownHostsFile=/dev/null" useradd
-M -d /var/www/vhosts/blogsrock.rackspace.com -p 'mystrongpassword' -s
'/bin/bash' -U -G www-data wp\_user2 You should see \`pssh\` report
\`SUCCESS\` for each slave node. 5. Run an \`id\` command through
\`pssh\` to verify the user creation on each slave node, again adding
\`-H\` flags for each additional slave node. parallel-ssh -P -H -x "-o
StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -o
GlobalKnownHostsFile=/dev/null" id wp\_user2 You should see something
similar to the following from each slave node: uid=1001(wp\_user2)
gid=1001(wp\_user2) groups=1001(wp\_user2),33(www-data) 6. Copy the new
site's content from the master server to each slave server using
\`rsync\`. rsync -avz -e ssh /var/www/vhosts/blogsrock.rackspace.com
root@:/var/www/vhosts Repeat the \`rsync\` for each slave node in your
stack. 7. Copy the Apache and Varnish configuration files to the slave
nodes. To make things easier we'll use a loop with the \`parallel-scp\`
command (part of the \`pssh\` package). Add extra \`-H\` flags for each
additional slave node. for file in
/etc/apache2/sites-available/blogsrock.rackspace.com.conf
/etc/varnish/include/blogsrock.rackspace.com\_.vcl; do parallel-scp -H
-x "-o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -o
GlobalKnownHostsFile=/dev/null" \$file \$file; done \#\#\# This is the
Final Countdown Now we can finally start putting everything together and
run the new site. 1. Restart \`lsyncd\` on the master node in order to
start syncing content for the new site to the slaves. service lsyncd
restart 2. Enable the new site's Apache configuration on the master
server and slave nodes. parallel-ssh -i -H -x "-o
StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -o
GlobalKnownHostsFile=/dev/null" /usr/sbin/a2ensite
blogsrock.rackspace.com.conf; /usr/sbin/a2ensite
blogsrock.rackspace.com.conf 3. Reload Apache's configuration on the
master server and slave nodes. parallel-ssh -i -H -x "-o
StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -o
GlobalKnownHostsFile=/dev/null" service apache2 reload; service apache2
reload 3. Reload Varnish's configuration on the master server and slave
nodes. parallel-ssh -i -H -x "-o StrictHostKeyChecking=no -o
UserKnownHostsFile=/dev/null -o GlobalKnownHostsFile=/dev/null" service
varnish reload; service varnish reload Congratulations, your new site is
online!

