---
node_id: 508
title: Windows Patches for Cloud Servers with a Managed Operations Service Level
permalink: article/windows-patching-for-managed-cloud-servers
type: article
created_date: '2011-04-04 16:57:40'
created_by: RackKCAdmin
last_modified_date: '2014-11-19 19:5721'
last_modified_by: rose.contreras
products: 'Cloud Servers,Managed Operations'
body_format: markdown_w_tinymce
---

All Windows patches for cloud servers within the Rackspace Managed Operations service level are released by Microsoft to the public on the second Tuesday of every month (known as Patch Tuesday). Rackspace tests these patches against our server builds before including them for updates to our customers' production servers. The patches are deployed to customers’ servers three weeks after Microsoft releases them. Our Windows server images are configured to check our Windows Server Update Services (WSUS) server daily for updates by default, but we release approved patches via our WSUS servers only once a month.

If you opted in to the Rackspace Managed Windows Patching service, you can manually install any software or updates released by Microsoft but not yet available on our WSUS servers. Use the **Windows Update** command located in the **Start** menu on your server to check for these patches directly from Microsoft. You can download most of these patches manually by visiting the page for the specific KB article related to the patch. You can also contact Rackspace support to assist you with the manual installation of any non-Rackspace approved patches onto your server. However, we cannot be held responsible for any issues that might arise from the manual installation of these patches before they are approved and released for update from our WSUS servers.

## WSUS endpoints

WSUS servers are located in each region where you can connect Windows Servers to pull approved Windows updates. We recommend that you get updates from the closest WSUS server.

The WSUS endpoints are as follows:

<table>
	<tr>
		<th>Region</th>
		<th>Data center</th>
		<th>WSUS endpoint</th>
	</tr>
	<tr>
		<td>Dallas</td>
		<td>DFW</td>
		<td>http://microsoftupdate.dfw1.rackspace.com</td>
	</tr>
	<tr>
		<td>Chicago</td>
		<td>ORD</td>
		<td>http://microsoftupdate.ord1.rackspace.com</td>
	</tr>
	<tr>
		<td>North Virginia</td>
		<td>IAD</td>
		<td>http://microsoftupdate.iad1.rackspace.com</td>
	</tr>
	<tr>
		<td>Hong Kong</td>
		<td>HKG</td>
		<td>http://microsoftupdate.hkg1.rackspace.com</td>
	</tr>
	<tr>
		<td>Sydney</td>
		<td>SYD</td>
		<td>http://microsoftupdate.syd1.rackspace.com</td>
	</tr>
	<tr>
		<td>London</td>
		<td>LON</td>
		<td>http://microsoftupdate.lon1.rackspace.com</td>
	</tr>
</table>
<p>&nbsp;</p>
<table>
	<tr>
		<th>Distribution</th>
		<th>Patching</th>
		<th>Mechanism</th>
		<th>Patching servers</th>
		<th>Frequency</th>
	</tr>
	<tr>
		<td>Windows Server 2008 R2</td>
		<td>WSUS</td>
		<td>microsoftupdate.[dc].rackspace.com</td>
		<td>Nightly between 1 a.m. and 5 a.m. in your server region's time zone:
			
			* IAD – EST
			* DFW – CST
			* SYD – AET
			* HKG – HKT
			* ORD – CST</td>
		<td>Windows Patching Portal</td>
	</tr>
	<tr>
		<td>Windows Server 2012	WSUS</td>
		<td>microsoftupdate.[dc].rackspace.com</td>
		<td>Nightly between 1 a.m. and 5 a.m. in your server region's time zone:
			
			* IAD – EST
			* DFW – CST
			* SYD – AET
			* HKG – HKT
			* ORD – CST</td>
		<td>Windows Patching Portal</td>
	</tr>
	<tr>
		<td>Windows Server 2012 R2</td>
		<td>WSUS</td>
		<td>microsoftupdate.[dc].rackspace.com</td>
		<td>Nightly between 1 a.m. and 5 a.m. in your server region's time zone:
			
			•	IAD – EST
			•	DFW – CST
			•	SYD – AET
			•	HKG – HKT
			•	ORD – CST</td>
		<td>Windows Patching Portal</td>
	</tr>
</table>

<p>&nbsp;</p>

## WSUS settings

While you are opted in to the Rackspace Managed Windows Patching service, the following registry setting are configured on the Managed Windows Server:

     [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\windows\WindowsUpdate]
	 "AcceptTrustedPublisherCerts"=dword:00000001
	 "WUServer"="http://microsoftupdate.dfw1.rackspace.com"
	 "WUStatusServer"="http://microsoftupdate.dfw1.rackspace.com"
	 
     [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\windows\WindowsUpdate\AU]
	 "AUOptions"=dword:00000004 "AutoInstallMinorUpdates"=dword:00000000
	 "DetectionFrequency"=dword:00000016 "DetectionFrequencyEnabled"=dword:00000001
	 "NoAutoRebootWithLoggedOnUsers"=dword:00000000 "NoAutoUpdate"=dword:00000000
	 "RackSpaceDefaults"=dword:00000001
	 "ScheduledInstallDay"=dword:00000000
	 "ScheduledInstallTime"=dword:00000002 "UseWUServer"=dword:00000001


You must set the Windows Updates service to automatically start. To do so, perform the following steps:

1.	Open a PowerShell command prompt and run the following commands: 
		
		Setting wuauserv Service to Auto
		
		Set-Service -Name wuauserv -StartupType Automatic

2.	Ensure that the wuauserv service is running:

		Restart-Service -Name wuauserv

3.	Apply all the changes:

		gpupdate.exe /force


You can find additional information on the [Rackspace Support site](http://support.rackspace.com) and the Windows Patching Portal. The following links provide complete information about how to configure your server registry settings for Windows updates.

 - [http://technet.microsoft.com/en-us/library/dd939844%28v=ws.10%29.aspx](http://technet.microsoft.com/en-us/library/dd939844%28v=ws.10%29.aspx)
 - [http://technet.microsoft.com/en-us/library/cc708449%28WS.10%29.aspx](http://technet.microsoft.com/en-us/library/cc708449%28WS.10%29.aspx)

## Opt out of Rackspace Managed Windows Patching

If you have valid reasons to take full control of and be responsible for managing your patching, you can opt out of Rackspace Managed Patching by following the instructions at [https://community.rackspace.com/general/f/34/t/689](https://community.rackspace.com/general/f/34/t/689).
