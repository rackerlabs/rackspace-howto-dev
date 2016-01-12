---
node_id: 3649
title: Available checks for Rackspace Monitoring
permalink: article/control-panel-monitoring-what-do-the-options-do
type: article
created_date: '2013-08-19 19:40:45'
created_by: Jim Culbreath
last_modified_date: '2016-01-05 21:2255'
last_modified_by: Mike Asthalter
products: Cloud Monitoring
body_format: tinymce
---

In the Cloud Control Panel, you can choose to set monitoring checks on
your servers. This article explains each check and the options that you
can set for them. For information about setting up one of these
monitoring checks, see [Create a monitoring check using the Cloud
Control
Panel](https://www.rackspace.com/knowledge_center/article/creating-a-monitoring-check-using-the-cloud-control-panel).

For API check definitions, see the Rackspace Monitoring Developer's
guide [Available Check Types and
Fields.](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/#document-tech-ref-info/check-type-reference) 

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

+--------------------------+--------------------------+--------------------------+
| Check type               | Creation options         | Editing options          |
+==========================+==========================+==========================+
| HTTP                     | Set the URL and specific | -   **Target**: Specify  |
|                          | body context with        |     the server IP        |
|                          | regular expressions      |     address or a         |
|                          | allowed.                 |     specified host name. |
|                          |                          | -   **Details**: Specify |
|                          | Click **Advanced         |     the exact URL and    |
|                          | Options** to open a      |     body content to use. |
|                          | **Body Match** text box  |     Regular expressions  |
|                          | in which you can provide |     are allowed.         |
|                          | more syntax.             | -   **Parameters**: Set  |
|                          |                          |     how often the check  |
|                          |                          |     runs and when it     |
|                          |                          |     will time out, as    |
|                          |                          |     well as which        |
|                          |                          |     regions the check    |
|                          |                          |     uses.                |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Alarm** to add an    |
|                          |                          |     alarm                |
+--------------------------+--------------------------+--------------------------+
| TCP                      | Set the port that you    | -   **Target**: Specify  |
|                          | want to monitor for      |     the server IP        |
|                          | connectivity. Provide    |     address or a         |
|                          | the following            |     specified host name. |
|                          | information:             | -   **Details**: Specify |
|                          |                          |     the port to be       |
|                          | -   Port number          |     monitored.           |
|                          | -   Target IP address or | -   **Parameters**: Set  |
|                          |     target host name     |     ho often the check   |
|                          |                          |     will run and when it |
|                          |                          |     will time out.       |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Ala**rm to add an    |
|                          |                          |     alarm.               |
+--------------------------+--------------------------+--------------------------+
| Ping                     | Select a name and select | -   **Details**: Set the |
|                          | the target type as IP    |     packet count and the |
|                          | address or host name.    |     number of packets    |
|                          |                          |     that are sent at one |
|                          |                          |     time.                |
|                          |                          | -   **Parameters**: Set  |
|                          |                          |     how often the check  |
|                          |                          |     runs and when it     |
|                          |                          |     will time out, as    |
|                          |                          |     well as which        |
|                          |                          |     regions the check    |
|                          |                          |     will use.            |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Alarm** to add an    |
|                          |                          |     alarm.               |
+--------------------------+--------------------------+--------------------------+
| Memory                   | There are no special     | -   **Parameters**: Set  |
|                          | settings when creating a |     how often the check  |
|                          | memory check.            |     will run and whei it |
|                          |                          |     will time out.       |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Alarm** to add an    |
|                          |                          |     alarm.               |
+--------------------------+--------------------------+--------------------------+
| CPU                      | There are no special     | -   **Parameters**: Set  |
|                          | settings with creating a |     how often the check  |
|                          | CPU check.               |     runs and when it     |
|                          |                          |     will time out.       |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Alarm** to add an    |
|                          |                          |     alarm.               |
+--------------------------+--------------------------+--------------------------+
| Load Average             | There are no special     | -   **Parameters**: Set  |
|                          | settings when creating a |     how often the check  |
|                          | load balancer check.     |     runs and when it     |
|                          |                          |     will time out.       |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Alarm** to add an    |
|                          |                          |     alarm.               |
+--------------------------+--------------------------+--------------------------+
| Filesystem               | Specify the disk for     | -   **Parameters**: Set  |
|                          | which you want to        |     how often the check  |
|                          | monitor space.           |     runs and when it     |
|                          |                          |     will time out.       |
|                          |                          | -   **Alarms**: Edit     |
|                          |                          |     existing alarms or   |
|                          |                          |     click **Create       |
|                          |                          |     Alarm** to add an    |
|                          |                          |     alarm.               |
+--------------------------+--------------------------+--------------------------+
| Network                  | -   Select which network | -   **Parameters**: Set  |
|                          |     interface to use     |     how often the check  |
|                          |     (typically eth0 or   |     runs and when it     |
|                          |     eth1).               |     will time out.       |
|                          | -   Set the receive rate | -   **Alarms**: Edit     |
|                          |     alert for warning    |     existing alarms or   |
|                          |     and critical states. |     click **Create       |
|                          | -   Set the transmit     |     Alarm** to add an    |
|                          |     rate alert for       |     alarm.               |
|                          |     warning and critical |                          |
|                          |     states. (For more    |                          |
|                          |     information, see     |                          |
|                          |     [Rackspace           |                          |
|                          |     Monitoring Checks    |                          |
|                          |     and                  |                          |
|                          |     Alarms](https://www. |                          |
|                          | rackspace.com/knowledge_ |                          |
|                          | center/article/rackspace |                          |
|                          | -cloud-monitoring-checks |                          |
|                          | -and-alarms).)           |                          |
+--------------------------+--------------------------+--------------------------+

 

Data graphs for monitoring********
----------------------------------

 

You can view graphical information about resource use on the server
details page. In the **Monitoring Data** section of the page, you can
view historical check data. This viewing option is available for all
checks and does not require the monitoring agent to be installed. Use
the drop-down menu under **Monitoring Data** to select the monitoring
check you want to view.

![](/knowledge_center/sites/default/files/field/image/Monitoring-Data.png)

