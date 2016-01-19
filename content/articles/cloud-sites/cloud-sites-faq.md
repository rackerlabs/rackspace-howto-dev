---
node_id: 5012
title: Cloud Sites - FAQ
type: article
created_date: '2015-12-10'
created_by: Stephanie Fillmon
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Sites
body_format: markdown_w_tinymce
---

<h2>Getting Started</h2>

<h3>How do my sub-accounts access their control panel?</h3>

<p>The Rackspace Cloud sub-account log in page can be found at <a href="https://www.websitesettings.com">https://www.websitesettings.com</a>.</p>

<h3>What goes in to calculating a compute cycle?</h3>

<p>Mostly, CPU processing time. However, compute cycles also account for the disk I/O your application's operations consume. For example, a page with heavy database queries will consume more compute cycles in part due to the larger volume of disk I/O it requires.</p>

<h3>How do I track my compute cycle usage?</h3>

<p>The compute cycles you use are presented in your control panel in near real time.</p>

<h3>What are compute cycles?</h3>

<p>Compute cycles measure the amount of processing time your applications take to execute in order to serve content to users from the Cloud Sites environment.</p>

---------
<h2>Account Services</h2>

<h3>Where can I find your Acceptable Use Policy (AUP)?</h3>

<p>You can find a copy of our <a href="http://www.rackspace.com/information/legal/aup">AUP</a>, <a href="http://www.rackspace.com/information/legal/cloud/tos">Terms of Service</a> (TOS) and <a href="http://www.rackspace.com/information/legal/cloud/sla">Service Level Agreement</a> (SLA)&nbsp;on our website.</p>

<h3>Where can I view usage information for my Cloud sites account?</h3>

<p>Overall usuage for diskspace and bandwidth is availiable in the <strong>Home</strong> tab when first logging in.</p>

<p>Individual site usage is available on the&nbsp;<strong>General Settings</strong>&nbsp;tab after clicking&nbsp;<strong>Hosting</strong>&nbsp;on the left navigation menu and then click on&nbsp;<strong>Cloud Sites</strong>&nbsp;and then on the domain in question.</p>

<p>More detailed information on usage is available in <strong>Reports, </strong>which&nbsp;breaks down bandwidth, MySQL, and MSSQL usage.</p>

<h3>How many compute cycles will my applications use?</h3>

<p>Since web applications vary so greatly, it's hard to make a perfect guess. There are, however, some guidelines that can help. For example, 10,000 compute cycles would power approximately:</p>

<ul>
	<li>2.1 million page views using a database-driven content management system</li>
	<li>11 million page views of rackspacecloud.com</li>
	<li>25 million requests for a static 15KB image</li>
</ul>

<h3>How far can I really scale?</h3>

<p>We currently have users pushing hundreds of millions of requests on single domains. There are many factors that impact how easily a web application can scale, including the application's code and its architecture. Rackers are ready to review your web application/solution and provide guidance on how to optimize it for Cloud Sites. If an application is not properly built for scale, Cloud Sites will not be able to compensate for it.</p>

<p>Also, if you are expecting a massive surge in traffic (perhaps your site was featured on Oprah) please contact us via chat, phone, or ticket in advance and we will help you prepare for it. The information we will need can be found at the end of the article <a href="/how-to/optimize-your-website-on-cloud-sites">Optimize your website on Cloud Sites</a>.&nbsp;</p>

<h3>What happens if I exceed the included amount?</h3>

<p>While most customers will fall well below the included amount, we have created fair and simple pricing beyond the base amount that means you pay ONLY for what you use and nothing more. There are no onerous penalties for exceeding the included plan amounts. The prices for all scaling metrics can be found on the <a href="http://www.rackspace.com/cloud/sites">Cloud Sites pricing page</a>.</p>

<h3>What is included for $150?</h3>

<p>We have included enough resources in the Cloud Sites base package to power most business needs. You get 50 GB of high performance storage as well as 500 GB of bandwidth permonth. In addition, Cloud Sites uses compute cycles to monitor your computing usage. You get 10,000 compute cycles per month across all your sites and applications. Unlike many hosting companies, the Rackspace Cloud will never cut you off for using what we sell you.</p>

<p>The base package does not include the cost of MySQL/MSSQL database storage, SSL, or domain registration. More details can be found on our <a href="http://www.rackspace.com/cloud/sites">pricing page</a>.</p>

<h3>I've had shell access (SSH) in the past. Why isn't it offered on Cloud Sites?</h3>

<p>Shell access (also commonly known as SSH) is not offered on Cloud Sites, primarily for security reasons. Keep in mind, however, that many functions typically accessed via shell are available on the Rackspace Cloud, including cron jobs, file permissions, and unzip. You can also do many SSH type functions by mounting your FTP location locally using SSHFS. More information can be found <a href="/how-to/getting-started-with-cloud-sites-ftpsshfsftp-clients">here</a>.&nbsp;</p>

<h3>Will Rackspace ever suspend my site if it receives tons of visitors?</h3>

<p>Rackspace will never suspend a site as long as the traffic is legitimate and the hosted content doesn't violate our TOS or our AUP. As a company, we succeed when you succeed, so we will always encourage legitimate traffic to your sites. We have several domains on Cloud Sites that receive millions of hits each month. We have never limited or throttled their accounts, as that is one of the many benefits of going with a cloud offering like the Rackspace Cloud Sites service. On the other hand, we will stop illegitimate spikes in traffic, such as runaway scripts or DDOS attacks.</p>

<h3>Can I use Cloud Sites as an audio or video encoder?</h3>

<p>Audio and video encoding is a task that is better suited for a Cloud Server. Cloud Sites was built to be a highly specialized and optimized computer cluster for serving web content. That means that it is not really designed for audio processing, video processing, or streaming tasks. You can have some audio or video content on Cloud Sites, but the service was not designed to be a processing farm for audio conversion, video conversion, or a Shoutcast system to use for live audio streaming.&nbsp;</p>

<h3>Can I host adult content sites on Cloud Sites?</h3>

<p>Please refer to our Acceptable Use Policy for details on what content can be hosted with us. You can find a copy of our <a href="http://www.rackspace.com/information/legal/aup">AUP</a> on our website.</p>

<h3>Who is my domain registrar?</h3>

<p>The company who serves as your domain registrar is responsible for managing your domain registration records. Your domain registrar is often the company who sold you your domain name. Register.com, GoDaddy, and TuCows are examples of popular domain registrars. Typically, you'll contact your registrar (or log in to their website) in order to renew your domain name, change your name servers, or update your contact information. If you purchased your domain name through us, we serve as your domain registrar. We also serve as your domain registrar if you elected to transfer your domain name to us. If don't know where you bought your domain name or who serves as your registrar, you can find out by doing a WHOIS search.</p>

<h3>Why was my request to change registrars rejected?</h3>

<p>Your current registrar may reject a registrar change request if:</p>

<ul>
	<li>the request was made within 60 days of the initial registration.</li>
	<li>there is a legal dispute over the domain name.</li>
	<li>there is a pending bankruptcy of the domain name holder.</li>
	<li>there is a dispute over the identity of the domain name holder.</li>
	<li>the domain name is "on hold" or "locked."</li>
</ul>

<p>Please note that your current registrar may offer "transfer lock" or a similar service as a security measure to prevent unauthorized transfer of your domain name. If this feature is activated, you will need to log on to your account with your current registrar in order to unlock the domain.</p>

<p>In order to turn the transfer lock function off, you must have access to the administrative email address you used when first registering the domain. Your current registrar will send an email to this account that will require a reply from you, confirming that the transfer is authorized. If you do not have access to this email address, contact <a href="http://manage.rackspacecloud.com/SupportMain.do">customer support</a>for help.</p>

<p>You can do a WHOIS search to find the administrative email and the current registar for the domain.</p>

<h3>What happens if my Cloud Sites domain registration expires?</h3>

<p>For any domain that is registered with or transferred to The Rackspace Cloud, we will automatically notify you as the expiration date for your domain name nears. The notices will be sent to the email address listed under the administrative contact for that particular domain name.</p>

<p>A total of three email notices will be sent to you, beginning 90 days before your domain is set to expire, and a fourth notice will be sent out 10 days after the expiration date. If you do not renew before the stated expiration date, the domain name will be held in reserve for a redemption period of 45 days. During this redemption period, you may incur a registry-imposed redemption fee in order to reactivate your domain. To renew or redeem your domain name, please contact&nbsp;<a href="http://manage.rackspacecloud.com/SupportMain.do">customer support</a>.</p>

<h3>Is my domain name set to auto renew?</h3>

<p>Unfortunately Automatic Domain Renewal is not available for registered Cloud Sites domains; the domains must be manually renewed via the Control Panel. Please see the following article on how to manually renew your domain:</p>

<p><a href="/how-to/renew-a-cloud-sites-domain-name">How Do I Renew My Domain?</a></p>

<h3>What does it mean when my domain name is "locked"?</h3>

<p>A "locked" domain cannot be transferred to a new registrar. Your current registrar may offer "transfer lock" or a similar service as a security measure to prevent unauthorized transfer of your domain name. If this feature is activated, you will need to log on to your account with your current registrar and turn this feature off before you can transfer your domain name.</p>

<h3>What top level domain extensions (TLDs) can I purchase through the control panel?</h3>

<p>You can set up domains with any extension, but only the following ones can be purchased or transferred to Cloud Sites at this time:</p>

<ul>
	<li>.com</li>
	<li>.org</li>
	<li>.net</li>
	<li>.co.uk</li>
</ul>

<p>Though they can be registered in the control panel, all .uk address can only be registered for a 2 year minimum and maximum.</p>

<h3>What is the Cloud Sites' IPS tag for .uk domain transfers?</h3>

<p>When you transfer your .uk domain into a new registrar, you must ensure that the Internet Provider Security (IPS) tag points to the correct place before you begin the transfer process. If you are transferring your domain registration to Rackspace, the IPS tag must point to TUCOWS-CA.</p>

<p>To change the IPS tag, contact your current Domain Registrar and request the change (some providers might charge an administration fee).</p>

<h3>What is the administrative email account listed for my domain name?</h3>

<p>You can do a WHOIS search to find the administrative email and the current registrar for the domain. A WHOIS search reveals details about a domain name, including who owns it, where it was registered, when it expires, and which name servers are assigned to the domain. There are many software tools for performing a WHOIS search, and you can also search online. One good web site to try is <a href="http://whois.domaintools.com/">http://whois.domaintools.com/</a></p>

<h3>What if I don't have access to the administrative email account listed for my domain name?</h3>

<p>You must have access to the administrative email to approve transfer requests when you are changing registrars or updating your name servers. Your current registrar will send an email to this account that will require a reply from you, confirming that the transfer is authorized. If you do not have access to this email address, please contact <a href="http://manage.rackspacecloud.com/SupportMain.do">customer support</a>for help.</p>

---------
<h2>Compromised Sites</h2>

<h3>What is a domain compromise?</h3>

<p>A domain compromise is when a domain has been exploited for various reasons. That is, a domain using exploitable code becomes infected with a code injection and proceeds to send out email without the owner's knowledge, infect visitors with malware, or perform other malicious activity.</p>

<h3>What can I do to avoid a domain suspension resulting from a domain compromise?</h3>

<p>To avoid suspension, you may not use the Cloud Sites platform or services to knowingly or unknowingly store, execute, promote, or facilitate malicious content or action to include:</p>

<ul>
	<li>Mail spam</li>
	<li>Code or file injection</li>
	<li>Outbound DDOS attacks</li>
	<li>Personally identifiable information scraping</li>
	<li>Brute force attacks</li>
	<li>MySQL/MSSQL spam request</li>
</ul>

<h3>How can I get my domain unsuspended?</h3>

<p>Following suspension, domains cannot be activated until all listed files are removed from our systems and the domains pass a security scan performed by our team. Due to the security of other customers, domains will not be activated if they do not meet these criteria.</p>

<h3>What if a domain is compromised and it was not my fault? Will I get a credit from this issue?</h3>

<p>Domains and their content are the responsibility of their owner. If domains are compromised, the final responsibility will be with the owner. Accounts will not be eligible for credits due to interruptions of service resulting from any AUP violation.</p>

<h3>Why doesn't Cloud Sites keep my domains secure?</h3>

<p>Cloud Sites is a platform-as-a-service web hosting product. We manage the infrastructure and you manage your domains' data and content. While our systems will conduct scans for malicious activity, we do not enforce minimum requirements on content management systems or conduct code audits to ensure security. We do, however, recommend keeping the content up-to-date.</p>

<h3>How can I increase the security of my domains?</h3>

<p>We are committed to ensuring the security of our infrastructure and the reputation of our hosting environment. Additional resources you may utilize to improve your security posture are third party products. There are many resources out in the marketplace if you search for the security of your website. Many popular content management systems (CMS) also recommend specific security plugins.</p>

---------
<h2>Security</h2>

<h3>How do I deny certain IP addresses from accessing my site on Cloud Sites?</h3>

<p>Visitors to a Cloud Sites website come through our load balancers, which means the IP address reported to your site will be that of our load balancers. We store the visitor's IP address in the <strong>X-Cluster-Client-Ip</strong> variable to work around this behavior. The value of <strong>X-Cluster-Client-Ip</strong> can be used when configuring allow and deny rules.</p>

<p>For instructions, see <a href="/how-to/controlling-access-to-linux-cloud-sites-based-on-the-client-ip-address">Controlling access to Linux Cloud Sites based on the client IP address</a>.</p>

---------
<h2>Backups</h2>

<h3>How often do Cloud Sites backup information?</h3>

<p>The entire Cloud Sites FTP structure is backed up in an <a href="/how-to/ftp-snapshot">FTP Snapshot</a> at the top of every hour, going back 32 hours. Those backups are rolled into a nightly backup, which are retained for two days. However, these backups are for disaster recovery on the server side. If for any reason a storage node on our side were to crash, our backups will be there to replace any lost data.</p>

<p>That said, we recommend that you make periodic backups of your site and data to your local computer since we are unable to extract an individual site's data from the nightly backups. If you need a backup of your MySQL or MS SQL databases, they can be exported through our online utilities (MySQL or MS SQL) or by connecting directly to the servers using desktop software.</p>

<h3>What does Rackspace use for a storage system? Have you done anything there to make it redundant?</h3>

<p>Nothing as important as your website should be served from a single hard drive, but you'd be surprised by how many web hosts have little more redundancy than a pair of crossed fingers. We're different - and for good reason.</p>

<p>The advanced architecture powering our hosting solution uses groups of high-performance, network-attached storage devices to reliably serve every web page, image, and email. Inside each storage device, drives are mirrored to each other in a RAID configuration to create a first level of redundancy. And, as a final precautionary measure, all data on the system is automatically backed up on a repeating schedule.</p>

---------
<h2>Web Servers</h2>

<h3>How do I set up error pages for my PHP site?</h3>

<p>You can use a .htaccess file to create custom error pages for your sites defaulted to PHP.</p>

<pre>
ErrorDocument "code" "location of error document"</pre>

<p>For example, with a 404 error:</p>

<pre>
ErrorDocument 404 /404.html</pre>

<p>You can use this directive to create error pages for other error codes as well. You will need to specify the path to the error page relative to the location of the .htaccess file. For more information, see the <a href="http://www.javascriptkit.com/howto/htaccess2.shtml">Comprehensive guide to .htaccess</a>.</p>

<h3>How do I stop PHP scripts from executing in a directory?</h3>

<p>Include the following line in an .htaccess file placed in the directory you want to stop scripts:</p>

<pre>
removehandler .php</pre>

<p>Then add the file extensions you wise to stop.</p>

<h3>How do I enable directory listing in PHP?</h3>

<p>In an .htaccess file, insert the following line:</p>

<pre>
Options +Indexes</pre>

<p>Directory listing is disabled by default on our system.</p>

<h3>How do I change the PHP memory limit value?</h3>

<p>Include this line in an .htaccess file in the same directory as the script:</p>

<pre>
php_value memory_limit ?M</pre>

<p>Replace "?" with the appropriate megabyte value. Our default size is set to 128 MB, and a successful modification of the memory limit will show in your PHP info file.</p>

<h3>How do I change the PHP maximum upload file size?</h3>

<p>In an .htaccess file in the same directory as the upload script, include this line:</p>

<pre>
php_value upload_max_filesize ?M</pre>

<p>Replace "?" with the applicable value. Our default size is set to 8 MB and a successful modification of the max upload size will show in your PHP info file.</p>

<p>If you're running WordPress and continue to have problems after increasing the upload_max_filesize value, you can try adding these settings as well:</p>

<pre>
php_value post_max_size ?M
php_value max_execution_time 200
php_value max_input_time 200
</pre>

<p>If you are continuing to encounter issues, please contact support.</p>

<h3>How can I view any PHP errors?</h3>

<p>On a PHP-based site, a blank white screen is usually indicative of a PHP error. By default, Cloud Sites will store PHP errors under the&nbsp;<strong>/log</strong>&nbsp;folder in FTP to a file named <strong>php_errors.log</strong>.</p>

<p>To view the error on the page itself, you can create or edit an .htaccess file in the same directory as the executing script or content, and include these lines:</p>

<pre>
php_flag display_errors 1
php_value error_reporting 8191
</pre>

<p>If you are continuing to encounter issues, please contact support.</p>

<h3>How do I change the PHP maximum execution time?</h3>

<p>In an .htaccess file in the same directory as the executing script, include this line:</p>

<pre>
php_value max_execution_time ?</pre>

<p>Replace "?" with the value you need to for the maximum execution time in seconds. Our default time is set to 30 seconds and a successful modification of the maximum execution will show in your PHP info file.</p>

<h3>How do I change the default character set for PHP?</h3>

<p>In an .htaccess file placed in the directory you want to have the character set changed on, include this line:</p>

<pre>
php_value default_charset ?</pre>

<p>Replace "?" with the character set required for your site, such as ISO-8859-1.</p>

<p><strong>Note</strong>: Cloud Sites has a default character set of UTF-8 if otherwise unspecified in your .htaccess file.</p>

<h3>How do I change the post max size value?</h3>

<p>In an .htaccess file in the same directory as the executing script, include this line:</p>

<pre>
php_value post_max_size ?M</pre>

<p>Replace "?" with the required value needed, such as 16. Our default post_max_size value is set to 8 MB.</p>

<h3>How do I prevent hotlinking on Cloud Sites?</h3>

<p>Using the .htaccess file, you can prevent hotlinking--presenting pictures, videos, or other media from one site on another by means for a link--by denying access to specific files based on the domain requesting the file. Hotlinking makes the person who hosts the media pay for the bandwidth to present it, while not getting any of the viewers on her own website. You can deny domains who would hotlink your media by using <strong>mod_rewrite</strong>, so don't forget to use RewriteBase.</p>

<p><strong>Fully denying</strong></p>

<p>Below is an example that will only allow <strong>.gif</strong>, <strong>.jpg</strong>, and <strong>.png</strong> files to be accessed from <strong>www.example.com</strong> and <strong>example.com</strong>:</p>

<pre>
RewriteEnging on
RewriteBase /
RewriteCond %{HTTP_REFERER} !^http://(www\.)?example.com/.*$ [NC]
RewriteRule \.(gif|jpg|png)$ - [F]
</pre>

<p>Using the above example, another website embedding one of your .gif, .jpg or .png images would see a broken image or the alt text specified in the img tag.</p>

<p><strong>Denying with another image</strong></p>

<p>If you want to be even more creative, you can even submit a different image to the other website, such as one that reads <em>Stop Hotlinking or Stop Stealing My Bandwidth!</em> Replacing the images with one like that will usually deliver the right message to the offenders and you could even advertise your own site if you make a custom image--though the above example will ultimately save you more bandwidth since it denies the image altogether. Below is an example that will only allow <strong>.gif</strong>, <strong>.jpg</strong> and <strong>.png</strong> files to be accessed from <strong>www.example.com</strong> and <strong>example.com</strong>, while serving <strong>hotlinking.png</strong> to any other websites requesting these files:</p>

<pre>
RewriteEngine on
RewriteBase /
RewriteCond %{HTTP_REFERER} !^http://(www\.)?example.com/.*$ [NC]
RewriteCond %{REQUEST_URI} !^/hotlinking.png$ [NC]
RewriteRule \.(gif|jpg|png)$ http://www.example.com/hotlinking.png [R,L]
</pre>

<p>Using the above example, another website embedding one of your images would see <strong>hotlinking.png</strong> instead.</p>

<h3>How can I password protect my Cloud Sites website?</h3>

<p>You can password protect your website, or any of its directories, through basic authentication using a .htaccess file. PHP must be set as the default technology for a site in order to utilize a .htaccess file. If used on a site where ASP is also an enabled technology, please be aware that this will not protect ASP pages.</p>

<p><strong>Create the .htaccess file</strong></p>

<p>This file sets up the requirement for basic authentication and also points to the file containing a list of authorized users.</p>

<ul>
	<li>Open a simple text editor, such as Notepad</li>
	<li>Insert the following code:</li>
</ul>

<pre>
# The name of the area
AuthName "Name of Password Protected Area"

# Type of authentication. Always basic
AuthType Basic

# Path to .htpasswd file for the site.
# It's preferable to not have this in any
# of the site's content directories.
AuthUserFile /mnt/Target01/[DDI_ID]/[CLIENT_ID]/[WEBSITE_NAME]/.htpasswd

# The requirements to view the site. This
# requires that the browser provide
# credentials matching on of the users in
# the .htpasswd file specified above.
Require valid-user
</pre>

<ul>
	<li>Replace the text inside of the quotation marks on the AuthName line to the name of your password protected area (Ex. AuthName "My Password Protected Directory").</li>
	<li>The text after AuthUserFile must be changed to match your site's server side path to a .htpasswd file we will create soon (Ex. /mnt/Target01/000000/www.mywebsite.com/web/content/.htpasswd).</li>
	<li>Save the file as "htaccess.txt" and upload it to the directory you want protected.</li>
	<li>Rename the file to ".htaccess".</li>
</ul>

<p><strong>Create the .htpasswd file</strong></p>

<p>This file will contain a list of usernames and password sets. Each line should contain one set and the username and password should be separated by a colon.</p>

<ol>
	<li>Open a simple text editor, such as Notepad</li>
	<li>Use a .htpasswd encryption tool, such as the one available <a href="http://www.htaccesstools.com/htpasswd-generator/">here</a>. This will automatically generate the content for the .htpasswd file</li>
	<li>Copy the output of the encryption tool to your text editor</li>
	<li>Save the file as "htpasswd.txt" and upload it to your site to the path you are pointing to in the .htaccess file</li>
	<li>Rename the file to ".htpasswd"</li>
</ol>

<p>Following these steps will setup basic authentication password protection to the directory indicated. If you are unable to view the .htaccess and .htpasswd files after you renamed them, you will need to configure your FTP client to view hidden files.</p>

<h3>How do I use a .htaccess file?</h3>

<p>For a comprehensive explanation on how to use a .htaccess file and how to create one, please see one or both of the following links: .htaccess-Guide.com's <a href="http://www.htaccess-guide.com/how-to-use-htaccess/">How to use .htaccess</a> and JavascriptKit.com's <a href="http://www.javascriptkit.com/howto/htaccess.shtml">Comprehensive guide to .htaccess</a>.</p>

<h3>Why is mod_rewrite not working on my site?</h3>

<p>On Cloud Sites, due to our unique hosting environment, we require a slight addition to the code used for mod_rewrite. You will also need to make sure that the site is using either PHP4 or PHP5 as the default technology.</p>

<p>In the .htaccess file containing your rewrite rules, add the following lines:</p>

<pre>
RewriteEngine on
RewriteBase /
</pre>

<p>Depending on the application, you may need to further specifiy the RewriteBase / to include the subdirectory the application is installed in. For example:</p>

<pre>
RewriteBase /subdirectory
</pre>

<p>You can find more information on mod_rewrite at <a href="http://httpd.apache.org/docs/2.0/mod/mod_rewrite.html">Apache's website</a>.</p>

<h3>How do I enable SSI?</h3>

<p>You can activate Server Side Includes (SSI) by using .htaccess with the following directives:</p>

<pre>
AddType text/html .shtml
AddHandler server-parsed .shtml
Options Indexes FollowSymLinks Includes
</pre>

<p><strong>Note</strong>: You cannot serve PHP content using SSI. For PHP content, we recommend using PHP's include or require statements or using an inline frame, such as shown in the following example:</p>

<pre>
&lt;html&gt;
&lt;head&gt;&lt;/head&gt;
&lt;body&gt;
&lt;iframe src="/test.php"&gt;&nbsp;&lt;/iframe&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<h3>How do I change the default character set for HTML?</h3>

<p>In an .htaccess file placed in the directory you want to have the character set changed on, include the following lines:</p>

<pre>
AddDefaultCharset ?
# Or AddType 'text/html; charset=?' html
DefaultLanguage en-US
</pre>

<p>Replace the "?" with the character set required for your site, such as UTF-8.</p>

<p><strong>Note</strong>: Cloud Sites has a default character set of UTF-8 if otherwise not specified in .htaccess</p>

<h3>How can I do a 301 redirect?</h3>

<p><strong>Note</strong>: The following examples are specific to PHP technology and will only work if the Cloud Site is configured to utilize this technology. This will not work for IIS (ASP / ASP.NET).</p>

<p>Please see this article for converting a site from Windows (IIS) to Linux (PHP) technology: <a href="/how-to/change-your-sites-default-technology">Change your site's default technology</a>.</p>

<p>You can also view this article for assistance with rewriting from ASP.NET: <a href="/how-to/rewrite-urls-from-aspnet-on-cloud-sites">How do I rewrite URLs from ASP.NET?</a></p>

<h3>How do I install my own PEAR module?</h3>

<p>You can deploy PEAR modules and other useful scripts locally on your site by modifying <a href="http://php.net/manual/en/ini.core.php">PHP's include_path</a>. The default include_path on a Cloud Site is:</p>

<pre>
.:/usr/share/pear:/usr/share/php</pre>

<p>To add another location for PHP to search for modules, just append a directory separator (colon) and the path to your PEAR modules. For example, you might add this to your .htaccess:</p>

<pre>
php_value include_path ".:/usr/share/pear:/usr/share/php:/mnt/stor1-wc1-dfw1/123456/www.domain.com/web/pear_modules"
</pre>

<p>You will want to change the path in the example above to use your website's absolute path. Please see <a href="/how-to/locate-the-linux-path-for-your-cloud-sites-website">this article</a> to locate your website's absolute path.</p>

<p>Your website's absolute path should resemble this: <strong>/mnt/stor1-wc1-dfw1/123456/www.domain.com/web/content</strong>.</p>

<p><strong>Install the modules</strong></p>

<p>Following the above example, you would login to your FTP and create a directory at the location: <strong>/www.domain.com/web/pear_modules</strong>.</p>

<p>Then you would place the PEAR modules into this directory.</p>

<p><strong>Use the modules</strong></p>

<p>Now when you reference your modules in your script using a PHP function like include() or require(), the server will know where to look for them.</p>

---------
<h2>Web Technologies</h2>

<h3>How can I implement an e-commerce site?</h3>

<p>While Cloud Sites is not designed for credit card storage and is not PCI compliant, it can be used as a flexible front-end to a payment gateway. For more information, see our article on <a href="/how-to/utilize-cloud-sites-in-an-e-commerce-solution">utilizing Cloud Sites in an e-commerce solution</a>.</p>

<h3>Why can't I see my site using a web browser?</h3>

<p>If you have uploaded new content and can't see the changes in your web site, check the following:</p>

<ul>
	<li>Has it been at least 48 hours since you completed your domain registration? If not, try uploading content to your website using the test FTP (ftp1.ftptoyoursite.com) and checking the changes on your test website.&nbsp;<a href="/how-to/using-a-staging-url">Click here</a>for instructions on how to use your test website.</li>
	<li>Have you put files in the correct folders on the server? See <a href="/how-to/getting-started-with-cloud-sites-uploading-your-content">Where should I put my web content files?</a>for more information.</li>
	<li>Did you upload the files in the <a href="/how-to/should-i-upload-files-as-ascii-or-binary">appropriate format?</a></li>
	<li>Did you <a href="/how-to/getting-started-with-cloud-sites-rackspace-nameservers-and-creating-custom-nameservers">check your nameservers</a> to make sure that they are pointing to Rackspace nameservers?</li>
</ul>

<p>If you have checked these points without success <a href="https://manage.rackspacecloud.com/">contact support</a> for more help.</p>

---------
<h2>Billing</h2>

<h3>How can I cancel my Cloud Sites account?</h3>

<p>To cancel your Cloud Sites account, you must complete the cancellation from the Cloud Sites Control Panel.</p>

<ol>
	<li>Log in to the <a href="https://manage.rackspacecloud.com/" target="_blank">Cloud Sites Control Panel</a>.</li>
	<li>Click <strong>Your Account</strong> and then click <strong>Cancel Account</strong>.</li>
	<li>Complete the cancellation form and then click <strong>Submit</strong>.</li>
</ol>

<p>If you want to cancel your Cloud Sites subscription but leave the account open for Cloud Servers or other products, open a support ticket for this request.</p>

<ol>
	<li>Log in to the <a href="https://manage.rackspacecloud.com/" target="_blank">Cloud Sites Control Panel</a>.</li>
	<li>At the top of the window, click <strong>Tickets</strong>.<br />
	You are redirected to the Support Tickets page in the Cloud Control Panel.</li>
	<li>Click <strong>Create Ticket</strong>.</li>
	<li>Complete the form and then click <strong>Submit Ticket</strong>.</li>
</ol>

<h3>Is there a referral bonus or any discounts available?</h3>

<p>Please visit <a href="http://www.rackspace.com/cloud/partners/">our website</a> for updates on the referral program.</p>

<h3>Will there be a discount if I prepay for a full year?</h3>

<p>We currently only offer month-to-month billing terms. It's our belief that we have to earn your business every month.</p>

<h3>How can I found out if a bill wasn't collected or a payment wasn't processed?</h3>

<p>You can access billing information for Cloud Sites by clicking <strong>Your Account</strong> &gt; <strong>Billing </strong>in the Cloud Sites Control Panel. This action opens the Billing &amp; Payments section of the Cloud Control Panel. This section displays important information like your total outstanding balance, the date of your most recent invoice, and which credit card is being used for payments on the account.</p>

<ul>
	<li>The Recent Activity section lists a summary of your most recent invoice. This summary includes the date and amount of your most recent invoice and your current balance.</li>
	<li>In the Payment Information section, you can update your billing information and change the credit card attached to the account.</li>
	<li>The Billing History section displays a summary of your invoice history. Click an ID number for an invoice to view additional information or download the invoice in your preferred format.</li>
</ul>

<h3>When am I billed for my account?</h3>

<p>When you sign up for products under the Managed Infrastructure, Managed Operations SysOPs, or Managed Operations DevOps Automation service levels, your credit card is charged a US $1.00 authorization charge to confirm it is an active card. The authorization charge returns to your card normally within 24-72 hours.</p>

<p>Thirty days after you sign up, your first invoice is processed. Your charges consist of service usage accrued within the first 30 days. <strong>Note</strong>: The exception is Cloud Sites, which charges for the first 30 days at sign up and continues to charge in advance of monthly usage.</p>

<p>After the first billing cycle, you are billed every month on the same date that you first signed up for service. If you have any questions about account billing, call us at 1-877-934-0410.</p>

<h3>What information will appear on my credit card invoice?</h3>

<p>Any payments made to Rackspace will be listed as <strong>Rackspace Cloud</strong> on your credit card statement.</p>

<h3>What forms of payment does Rackspace accept?</h3>

<p>At this time, Rackspace only accepts credit card payments. We allow payment by Visa, MasterCard, and American Express.</p>

<h3>Is there a discount if I purchase multiple hosting accounts with Rackspace?</h3>

<p>No, at this time we do not offer a discount if you purchase multiple accounts.</p>

<h3>I live outside the United States. Can I use my foreign credit card to pay for my account?</h3>

<p>Yes, international credit cards are accepted. We allow payment by Visa, MasterCard, and American Express.</p>

<h3>How do I update my billing information?</h3>

<p>Use the following instructions to change your credit card and billing information from the <strong>Cloud Sites Control Panel</strong>.</p>

<p><strong>To change credit card information</strong></p>

<ol>
	<li>Log in to your control panel at <a href="https://mycloud.rackspace.com/">https://mycloud.rackspace.com</a>.</li>
	<li>In the left navigation menu, click <strong>Your Account</strong> &gt; <strong>Billing</strong>.<br />
	You are redirected to the Billing &amp; Payments section of the Cloud Control Panel.</li>
	<li>To edit your credit card, click <strong>Edit Credit Card</strong> under Payment Information.</li>
	<li>When you are done making changes, click <strong>Save Credit Card.</strong></li>
</ol>

<p><strong>To edit billing information</strong></p>

<ol>
	<li>Log in to your control panel at <a href="https://manage.rackspacecloud.com/">https://manage.rackspacecloud.com</a>.</li>
	<li>In the left navigation menu, click <strong>Your Account</strong> &gt;<strong> Billing</strong>.<br />
	You are redirected to the Billing &amp; Payments section of the Cloud Control Panel.</li>
	<li>Click the pencil icon next to <strong>Billing Address.</strong></li>
	<li>When done making changes, click <strong>Save Contact</strong>.</li>
</ol>

<p>Use the following instructions to change your credit card and billing information from the <strong>Cloud Control Panel</strong>.</p>

<p><strong>To change credit card information</strong></p>

<ol>
	<li>Log in to your control panel at <a href="https://mycloud.rackspace.com/">https://mycloud.rackspace.com</a>.</li>
	<li>Open the <strong>Account: </strong>menu in the top right corner of the screen, and click <strong>Billing &amp; Payments</strong>.<br />
	The Billing &amp; Payments section is displayed.</li>
	<li>To edit your credit card, click <strong>Edit Credit Card</strong> under Payment Information</li>
	<li>When you are done making changes, click <strong>Save Credit Card.</strong></li>
</ol>

<p><strong>To edit billing information</strong></p>

<ol>
	<li>Log in to your control panel at <a href="https://mycloud.rackspace.com/">https://mycloud.rackspace.com</a>.</li>
	<li>Open the <strong>Account: </strong>menu in the top right corner of the screen, and click <strong>Billing &amp; Payments</strong>.<br />
	The Billing &amp; Payments section is displayed.</li>
	<li>Click the pencil icon next to <strong>Billing Address.</strong></li>
	<li>When done making changes, click <strong>Save Contact</strong>.</li>
</ol>

<h3>Am I charged bandwidth for FTPing data to or from my Cloud Sites?</h3>

<p>No, FTP bandwidth does not count against your monthly transfer.</p>

<h3>How can I contact the Cloud Sites billing team?</h3>

<p>A Cloud Billing Specialist can help you with account billing questions. The Billing Team may be reached directly by phone at 1-877-934-0410 between the hours of 8:00 am and 5:00 pm CT, Monday through Friday.</p>

---------
<h2>Linux and PHP</h2>

<h3>What are the PHP configuration limits for Cloud Sites?</h3>

<p>The maximum values for PHP configuration options via .htaccess are:</p>

<ul>
	<li>Memory (<strong>memory_limit</strong>): 512M</li>
	<li>Upload size (<strong>upload_max_filesize</strong>): 550M</li>
	<li>Execution time in seconds (<strong>max_execution_time</strong>): 30</li>
</ul>

<p><strong>Note</strong>: Under some circumstances, PHP may grant an additional 30 seconds to a process that is still executing at the 30 second mark.</p>

<h3>What version of Linux does Cloud Sites run? What about for Windows?</h3>

<p>Cloud Sites removed the ability to host disparate technologies due to changes in our technology options. The hybrid technology option removal allows us to release new changes more quickly.</p>

---------
<h2>MySQL</h2>

<h3>How do I import a large MySQL database?</h3>

<p>You should be able to use the <em>Online Manager</em> (see <a href="/how-to/rackspace-cloud-sites-essentials-phpmyadmin-database-management-interface" title="Working with a MySQL database">PHPmyAdmin Database Management Interface</a>) to import databases that are less than 16 MB in size without issue.</p>

<p>However, if you need to import database data that exceeds 16 MB into your Cloud Sites environment, you can use a script which you can schedule via a cron job.</p>

<p>Following is an example to help you set up this script:</p>

<pre>
#!/bin/sh
mysql -h DB_HOST -u DB_USER -p'DB_PASSWORD' DB_NAME &lt; /path/to/file/db_import.sql
</pre>

<ol>
	<li>Create a new text file, add the preceding code to it, and save it as restore.sh. In the preceding script, replace the placeholders with your actual information, as follows:
	<ul>
		<li><em>pathToFile</em>—This is the absolute path to your files. You can find this path by clicking on Hosting &gt; Cloud Sites &gt; Features in the Cloud Sites Control Panel and scrolling down the page. This path is the Linux Path listed there. An example is /mnt/target02/123456/www.domain.com. (Note that the file name is not included in this path.)</li>
	</ul>

	<ul>
		<li><em>databaseHost</em> - The name of the database host. An example is mysql5-9.wc1.</li>
	</ul>

	<ul>
		<li><em>database</em>User - The name of the database user.</li>
	</ul>

	<ul>
		<li>databae_Password - The password of the target database.</li>
	</ul>

	<ul>
		<li><em>databaseName</em> - The name of the database to which you are restoring.</li>
	</ul>
	</li>
	<li>Upload this file to your Cloud Site (for security purposes, we recommend keep this file outside your webroot) and create a "perl" cron job to schedule the task (the perl option runs shell scripts as well)..<br />
	<strong>Note</strong>: For security purposes, we recommend that you keep this file outside your webroot directory.</li>
	<li>Put the name of the file, which in this example is import.sh, in the "Command To Run" field.</li>
	<li>Select <strong>Perl</strong> as the Command Language and then select the minimum interval at which you want to run that script (5 minutes is recommended).<br />
	Logs are available in your <code>/logs/</code> folder each time a cron job is performed and you receive an email confirmation informing you if the job was successful or not.</li>
</ol>

<p><strong>Note</strong>: The cron job has 15 minutes to complete. If the script takes longer than 15 minutes to complete, it will time out. If this is a problem for you please break up the import into smaller pieces (several .sql files) and reschedule the job as necessary.</p>

<p>For more information about cron and related tasks, please see the following articles:</p>

<p><strong>Cron FAQ's:</strong></p>

<ul>
	<li><strong><a href="https://www.rackspace.com/knowledge_center/article/what-is-a-cloud-sites-cron-job">What is a cron job?</a></strong></li>
	<li><strong><a href="https://www.rackspace.com/knowledge_center/article/enable-or-disable-a-cloud-sites-scheduled-task-cron-job">Enable or disable a Cloud Sites scheduled task (cron job)</a></strong></li>
	<li><strong><a href="https://www.rackspace.com/knowledge_center/article/how-do-i-schedule-a-cron-job-for-cloud-sites">How do I schedule a cron job?</a></strong></li>
	<li><strong><a href="https://www.rackspace.com/knowledge_center/article/create-a-cron-job-to-back-up-a-cloud-sites-sql-server-database">Create a cron job to back up a Cloud Sites SQL Server database</a></strong></li>
</ul>

<h3>What is the shortest scheduled interval I can set for a Cloud Sites cron job?</h3>

<p>The minimum scheduled interval for a cron job is set to 5 minutes.</p>

---------
<h2>IIS, Windows, and .NET</h2>

<h3>How do I rectify an invalid view state error with an ASP.NET application?</h3>

<p>To correct this error, modify the machineKey in web.config. Use the information at the following sites to generate a key and usage in web.config.</p>

<ul>
	<li><a href="http://www.orcsweb.com/articles/generate-aspnet-machine-key/">http://www.orcsweb.com/articles/generate-aspnet-machine-key/ </a></li>
	<li><a href="http://support.orcsweb.com/KB/a248/why-am-i-am-getting-following-viewstate-error-view.aspx">http://support.orcsweb.com/KB/a248/why-am-i-am-getting-following-viewstate-error-view.aspx</a></li>
</ul>

<h3>What is an ASP.NET application pool?</h3>

<p>An application pool is a form of encapsulation to prevent the effects of bad code being executing from impacting other processes. Each application pool has its own worker process associated with it. By default, each site's /content directory is an application pool. In some situations, you may have installed a separate application into a sub-directory, such as /content/gallery. In this case, you may need to have the /gallery sub-directory turned into an application pool. By contacting support, this can be processed for you.</p>

<p>For in-depth information concerning application pools, please see the following article:</p>

<p><a href="http://www.developer.com/net/asp/article.php/2245511">http://www.developer.com/net/asp/article.php/2245511</a></p>
