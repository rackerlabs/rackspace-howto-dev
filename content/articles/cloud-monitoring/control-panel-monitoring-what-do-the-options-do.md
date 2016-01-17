---
node_id: 3649
title: Available checks for Rackspace Monitoring
type: article
created_date: '2013-08-19'
created_by: Jim Culbreath
last_modified_date: '2016-01-05'
last_modified_by: Mike Asthalter
product: Cloud Monitoring
body_format: tinymce
---

In the Cloud Control Panel, you can choose to set monitoring checks on
your servers. This article explains each check and the options that you
can set for them. For information about setting up one of these
monitoring checks, see [Create a monitoring check using the Cloud
Control
Panel](/howto/creating-a-monitoring-check-using-the-cloud-control-panel).

<span>For API check definitions, see the Rackspace Monitoring
Developer's guide </span>[Available Check Types and
Fields.](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/#document-tech-ref-info/check-type-reference)<span> </span>

Monitoring checks and alarms are located in the Cloud Servers section of
the control panel.

-   You can create a check by clicking the gear icon next to your
    individual server name and selecting **Create Check**.
-   To edit a check, click on the server name and scroll to the
    **Monitoring Checks** section of the server details page. From
    there, you can click a check name and make changes to it.

Available monitoring checks
---------------------------

The following table lists each check that you can create for your
server, the options that you can set when you create the check, and the
options that you can edit for an existing check.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Check type</th>
<th align="left">Creation options</th>
<th align="left">Editing options</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">HTTP</td>
<td align="left"><p>Set the URL and specific body context with regular expressions allowed.</p>
Click <strong>Advanced Options</strong> to open a <strong>Body Match</strong> text box in which you can provide more syntax.</td>
<td align="left"><ul>
<li><strong>Target</strong>: Specify the server IP address or a specified host name.</li>
<li><strong>Details</strong>: Specify the exact URL and body content to use. Regular expressions are allowed.</li>
<li><strong>Parameters</strong>: Set how often the check runs and when it will time out, as well as which regions the check uses.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">TCP</td>
<td align="left"><p>Set the port that you want to monitor for connectivity. Provide the following information:</p>
<ul>
<li>Port number</li>
<li>Target IP address or target host name</li>
</ul></td>
<td align="left"><ul>
<li><strong>Target</strong>: Specify the server IP address or a specified host name.</li>
<li><strong>Details</strong>: Specify the port to be monitored.</li>
<li><strong>Parameters</strong>: Set ho often the check will run and when it will time out.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Ala</strong>rm to add an alarm.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left">Ping</td>
<td align="left">Select a name and select the target type as IP address or host name.</td>
<td align="left"><ul>
<li><strong>Details</strong>: Set the packet count and the number of packets that are sent at one time.</li>
<li><strong>Parameters</strong>: Set how often the check runs and when it will time out, as well as which regions the check will use.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">Memory</td>
<td align="left">There are no special settings when creating a memory check.</td>
<td align="left"><ul>
<li><strong>Parameters</strong>: Set how often the check will run and whei it will time out.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left">CPU</td>
<td align="left">There are no special settings with creating a CPU check.</td>
<td align="left"><ul>
<li><strong>Parameters</strong>: Set how often the check runs and when it will time out.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">Load Average</td>
<td align="left">There are no special settings when creating a load balancer check.</td>
<td align="left"><ul>
<li><strong>Parameters</strong>: Set how often the check runs and when it will time out.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left">Filesystem</td>
<td align="left">Specify the disk for which you want to monitor space.</td>
<td align="left"><ul>
<li><strong>Parameters</strong>: Set how often the check runs and when it will time out.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">Network</td>
<td align="left"><ul>
<li>Select which network interface to use (typically eth0 or eth1).</li>
<li>Set the receive rate alert for warning and critical states.</li>
<li>Set the transmit rate alert for warning and critical states. (For more information, see <a href="/howto/rackspace-monitoring-checks-and-alarms">Rackspace Monitoring Checks and Alarms</a>.)</li>
</ul></td>
<td align="left"><ul>
<li><strong>Parameters</strong>: Set how often the check runs and when it will time out.</li>
<li><strong>Alarms</strong>: Edit existing alarms or click <strong>Create Alarm</strong> to add an alarm.</li>
</ul></td>
</tr>
</tbody>
</table>



Data graphs for monitoring ********
-----------------------------------



You can view graphical information about resource use on the server
details page. In the **Monitoring Data** section of the page, you can
view historical check data. This viewing option is available for all
checks and does not require the monitoring agent to be installed. Use
the drop-down menu under **Monitoring Data** to select the monitoring
check you want to view.

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Monitoring-Data.png){width="742"
height="317"}

