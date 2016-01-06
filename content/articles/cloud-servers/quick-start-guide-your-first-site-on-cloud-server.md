---
node_id: 3768
title: Quick start guide - Create your first website on Cloud Servers
permalink: article/quick-start-guide-your-first-site-on-cloud-server
type: article
created_date: '2013-11-11 19:59:20'
created_by: David Hendler
last_modified_date: '2015-01-13 20:1207'
last_modified_by: David Hendler
products: Cloud Servers
body_format: markdown_w_tinymce
---

<p>The Rackspace Cloud can save you both time and money. This guide shows you how to do both by explaining the basic process of turning your idea into a working site in three basic steps:</p>

<ol start="1" type="1">
	<li><a href="http://www.rackspace.com/knowledge_center/#Step1">Build the infrastructure</a></li>
	<li><a href="http://www.rackspace.com/knowledge_center/#Step2">Upload your code</a></li>
	<li><a href="http://www.rackspace.com/knowledge_center/#Step3">Test</a></li>
</ol>

<p>The project that you're bringing to the cloud is probably much more complicated than what this guide covers. However, the process that this guide uses applies to the successful deployment of any web site or application.</p>

<p>This guide is not a comprehensive tour of Cloud Servers. However, by following these instructions, you are establishing the fundamentals that you can build on by reading future articles and guides.</p>

<h2>What you need</h2>

<p>The information in this guide is practical. You should follow along step by step. To do so, you might need to install the following software:</p>

<p>Mac OS X</p>

<ul type="disc">
	<li>Mac OS X already has Terminal.app, but you can download <a href="http://iterm.sourceforge.net/">iTerm</a> if you prefer</li>
	<li><a href="http://cyberduck.ch/">Cyberduck</a> SFTP has built-in support for Rackspace <a href="http://www.rackspace.com/cloud/files/">Cloud Files</a></li>
</ul>

<p>Windows</p>

<ul type="disc">
	<li>If you don't already have an SSH client, download <a href="http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html/">PuTTY</a></li>
	<li>If you don't already have an SFTP client that supports SFTP, download <a href="https://filezilla-project.org/">FileZilla</a></li>
</ul>

<p>You also will need a website to upload to your cloud server. To save time you can use an HTML file created for this exercise. Download it <a href="http://90df0b8db988dcfbf5da-c1875553a16f2a6d80002cac1a22fc37.r75.cf1.rackcdn.com/index.html">here</a> (right-click to save the file).</p>

<h3><a name="Step1"></a>Build the infrastructure</h3>
<p>In this section, you create your server, connect to it, and install the Apache web server package to turn the server into a web server.</p>
<strong>Create a cloud server</strong>
<ol>
<li>Log in to the <a href="https://mycloud.rackspace.com">Cloud Control Panel</a>. To log in, use the user name and password that you entered when you created your account.</p>

<p><img alt="" border="2" height="384" src="/knowledge_center/sites/default/files/field/image/3768.1.png" width="668" /></p>

<p>The control panel supports many Rackspace products and services. Each component of this interface, and all of our products and services, are explained in other articles and videos (for example, <a href="http://www.rackspace.com/knowledge_center/article/introducing-the-new-cloud-control-panel">Introducing the Cloud Control Panel</a>). This guide focuses on deploying your first cloud server.</p></li>

<li>On the Cloud Servers page, which is displayed whenever you log in, click <strong>Create Server</strong>.

<p>In most cases, you can deploy the right infrastructure with just a few clicks.</p>

<p>You have a large amount of control when creating a new cloud server, but to keep things simple this guide focuses on the three required parts: name, image, and size</p>

<li>Name your Cloud Server

<p>The name of your cloud server should communicate its role (for example, web server or database) and what it's hosting.</p></li>

<li>Select an image. 

<p>The image that you select contains both the OS and preselected software.</p>
<p><img alt="" border="2" height="320" src="/knowledge_center/sites/default/files/field/image/3768.5.png" width="520" /></p>

<li>Select a flavor

<p>Flavor refers to the server's capacity for CPU, RAM, and hard drive. You can think of flavor as the "size" of the server. When you need more power, you want to select a "bigger" Cloud Server, so you select a higher capacity flavor. Because this is a test server, save some money and select the 1 GB General Purpose flavor.</p>

<p>Use the slider to select the flavor.</p>

<p><img alt="" border="2" height="442" src="/knowledge_center/sites/default/files/field/image/3768.6.png" width="550" /></p>
<li>Click <strong>Create Server</strong>.

<p>A pop-up window is displayed with your server's Root Admin Password. You need this password to connect to the server later in this guide, so copy it before you click <strong>Dismiss Password</strong>.</p></li>

<li>Verify that the build is complete.

<p>The time it takes for your cloud server to build depends on the image and flavor that you selected. The server is finished building and is ready for a connection when the Server Status is <strong>Active</strong>.</p>

<p><img alt="" border="2" height="39" src="/knowledge_center/sites/default/files/field/image/3768.10.png" width="204" border="1" /></p></li>

<li>Copy the public IP address.

<p>Now that you have an active cloud server, you need to make it a web server. You do this by connecting to it and installing the Apache web server package. You use the server's IPv4 address (PublicNet), which you can find in the <strong>Networks</strong> section of the server's detail view. Copy the address for later use.</p>

<p><img alt="" border="2" height="176" src="/knowledge_center/sites/default/files/field/image/3768.11.png" width="770" /></p></li>
</ol>

<h2>Connect to your server</h2>

<p>You can connect to a server in several ways, but the standard and most secure method is called Secure Shell, or SSH. It allows you to send information to and from your server in a secure fashion.</p>
<ol>
<li>Connect from either a Mac OS X or Windows Computer.
<ul>
<li><strong>Connect from Mac OS X</strong>
	
<p>You can connect to your cloud server from a Mac OS X computer by running the SSH command in Terminal.app or iTerm (if you downloaded that at the beginning of the guide). You can find the command to use SSH in the right-side bar of the server detail page of the Cloud Control Panel.</p>

<p><img alt="" border="2" height="209" src="/knowledge_center/sites/default/files/field/image/3768.12.png" width="422" /></p>

<p>Copy this command and paste  it into your terminal, or click it and Terminal.app opens for you.</p>

<p><img alt="" border="2" height="143" src="/knowledge_center/sites/default/files/field/image/3768.13.png" width="760" /></p>
</li>
<li><strong>Connect from Windows</strong>

<p>You can use the PuTTY SSH client to connect to your server from a Windows computer. For instructions, see <a href="http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-3-going-from-windows-to-linux-using-putty">Connecting to Linux from Windows by using PuTTY</a>.</p>

<p>The first time that you connect to a cloud server, your computer verifies that this is something you want to do.</p></li></ul></li>
<li>Type <strong>yes</strong> and then press <strong>Enter</strong>.

<p><img alt="" border="2" height="172" src="/knowledge_center/sites/default/files/field/image/3768.14.png" width="732" /></p></li>

<li>Type or paste the password that you copied in step 6 when you created the server.

<p><img alt="" border="2" height="189" src="/knowledge_center/sites/default/files/field/image/3768.15.png" width="733" /></p>

<p>If the password is correct, you connect to your server. You will see a screen similar to the following one:</p>

<p><img alt="" border="2" height="456" src="/knowledge_center/sites/default/files/field/image/3768.16.png" width="716" /></p></li></ol>

<h2>Install Apache</h2>

<p>To install Apache, enter the following command in the terminal window:</p>

<pre>
apt-get install apache2 -y</pre>

<p><img alt="" border="2" height="126" src="/knowledge_center/sites/default/files/field/image/3768.17.png" width="671" /></p>

<p>Some information scrolls by in your terminal window. This is your server downloading and installing Apache and any software Apache might need to operate correctly.</p>

<h3>Test Apache with your web browser</h3>

<p>After the command is finished running, ensure that Apache is installed and turned on. Put the (PublicNet) IPv4 address of your cloud server into a web browser. If you see the message It works!, you now have a web server installed on your cloud server.</p>

<p><img alt="" border="2" height="157" src="/knowledge_center/sites/default/files/field/image/3768.18.png" width="694" /></p>

<h2>Upload your code</h2>

<p>The next step is to upload your site. You might be familiar with File Transfer Protocol (FTP) as a way to upload files to and download files from another computer. Rackspace Cloud Servers uses SSH File Transfer Protocol (SFTP) for added security, so you need an FTP client that will support an SFTP connection. Fortunately, many of the popular and free FTP clients do this.</p>


<h3>Establish an SFTP connection with your server by using Cyberduck</h3>
<ol>
<li>In the Cyberduck interface, click <strong>Open Connection</strong>.

<p><img alt="" border="2" height="233" src="/knowledge_center/sites/default/files/field/image/3768.19.png" width="653" /></p></li>
<li>Select <strong>SFTP (SSH File Transfer Protocol)</strong>.</li>
<li>For <strong>Server</strong>, type the IP address of the cloud server.</li>
<li>For Username, enter <strong>root</strong>.</li>
<li>For <strong>Password</strong>, enter the root user's password.</li>
<li>Click <strong>Connect</strong>.
<p><img alt="" border="2" height="371" src="/knowledge_center/sites/default/files/field/image/3768.20.png" width="653" /></p></li>
</ol>

<h3>Upload your site</h3>

<p>If you haven't already downloaded the sample HTML file, download it from<a href="http://90df0b8db988dcfbf5da-c1875553a16f2a6d80002cac1a22fc37.r75.cf1.rackcdn.com/index.html">here</a>.</p>

<p>You cannot upload your HTML file just anywhere on the Cloud Server. Apache is configured to look in a specific directory for content to serve on the web. This special directory is referred to as the <em>DocumentRoot</em>.</p>

<p>On an Ubuntu server, the DocumentRoot is located at /var/www, so that's where you need to upload your file. Navigate to that directory in Cyberduck by using the following steps:</p>

<ol>
<li>Select the I directory by using the drop-down menu at the top of the window.

<p><img alt="" border="2" height="160" src="/knowledge_center/sites/default/files/field/image/3768.21.png" width="611" /></p></li>

<li>Double-click the <strong>var</strong> directory.

<p><img alt="" border="2" height="526" src="/knowledge_center/sites/default/files/field/image/3768.22.png" width="590" /></p></li>

<li>Double-click the <strong>www</strong> directory.</p>

<p><img alt="" border="2" height="457" src="/knowledge_center/sites/default/files/field/image/3768.23.png" width="668" /></p></li>

<p>You're now in the DocumentRoot directory.</p>

<p><img alt="" border="2" height="195" src="/knowledge_center/sites/default/files/field/image/3768.24.png" width="658" /></p>

<p>You should see an <strong>index.html</strong> file already in the directory. This is the "It works!" file that you saw when you tested Apache in your browser earlier.</p></li>

<li>Replace the <strong>index.html</strong> file with your own file by dragging the new <strong>index.html</strong> file into Cyberduck.</li>
<li>When Cyberduck asks if you want to overwrite the existing file, click <strong>Continue</strong>.

<p><img alt="" border="2" height="616" src="/knowledge_center/sites/default/files/field/image/3768.25.png" width="654" /></p></li></ol>

<h2><a name="Step3"></a> Test your site</h2>

<p>Now that the correct HTML file is uploaded to the correct directory, you should see your site when you refresh your browser.</p>

<p><img alt="" border="2" height="719" src="/knowledge_center/sites/default/files/field/image/3768.26.png" width="764" /></p>

<p>Congratulations! In a short period of time, you deployed a cloud server, connected to it via SSH, installed the Apache web server, uploaded a new HTML file to the server's DocumentRoot directory, and tested the site in a web browser.</p>

<h2>What's next?</h2>

<p>Several resources are available to help you progress:</p>

<ul type="disc">
	<li><a href="http://www.rackspace.com/knowledge_center/">Rackspace Knowledge Center</a> - Information about all Rackspace products</li>
	<li><a href="https://launch.rackspace.com/">Cloud Launch Guides</a> - Step-by-step guides on how to build and deploy cloud services</li>
	<li><a href="https://community.rackspace.com/">The Rackspace Community</a> - Discuss ideas with Rackers and other customers</li>
	<li><a href="http://www.rackspace.com/support">Fanatical Support</a></li>
</ul>

<p>&nbsp;</p>
