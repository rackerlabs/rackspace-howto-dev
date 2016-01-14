---
node_id: 3909
title: Introducing Rackspace Monitoring on Mobile Devices
type: article
created_date: '2014-02-18 22:41:01'
created_by: maria.abrahms
last_modified_date: '2016-01-04 17:5634'
last_modified_by: constanze.kratel
product: Cloud Monitoring
body_format: tinymce
---

The new Rackspace Cloud mobile application for iOS and Android devices
enables you to instantly monitor the health of your cloud
infrastructure.  The Rackspace Cloud mobile app, when used with
Rackspace Monitoring, provides you with timely and accurate information
about how your resources are performing. 

This article describes how to get started with the app and perform the
following Rackspace Monitoring actions on your mobile device:

-   View the status of any current alarm
-   View historical data and graphs that show trends over time
-   View monitoring check and alarm details
-   Understand error conditions

Get Started
-----------

First, you need to install Rackspace Monitoring on your cloud resources,
if it is not already installed.  For information about using the Cloud
Control Panel or the Rackspace Monitoring API to set up monitoring,
see [Getting Started With Rackspace
Monitoring](http://www.rackspace.com/knowledge_center/getting-started/cloud-monitoring). 

Download the Application
------------------------

To download the Rackspace cloud app for mobile devices, click the
following link for your device:

[![](/knowledge_center/sites/default/files/field/image/Download_on_the_App_Store_Badge_US-UK.png)](https://itunes.apple.com/us/app/rackspace-cloud-control/id672443103?mt=8) 
 
  [![](/knowledge_center/sites/default/files/field/image/en_app_rgb_wo_60.png)](https://play.google.com/store/apps/details?id=com.rackspace.cloudmobile)

For instructions on how to log in and add accounts to your device, see
[Getting Started with the Rackspace Mobile Application and Managing
Accounts](http://www.rackspace.com/knowledge_center/article/getting-started-with-the-rackspace-mobile-application-and-managing-accounts).

Open the Monitoring Screen
--------------------------

On the main menu of the app on your device, tap **Monitoring**.  A
number on the main menu, as shown in the following example, indicates
that you have one or more resources with an alarm in a critical or
warning state.

![](/knowledge_center/sites/default/files/field/image/newMonitoringScreen.png)

On the Monitoring home screen, you can view a list of monitored
resources and their current status.  By tapping the different status
icons, you can view resources with at least one alarm in Critical,
Warning, or OK state. 

-   Alarms in a Critical state are shown in red.
-   Alarms in a Warning state are shown in yellow.
-   Alarms in OK state are shown as green.
-   Alarms with an error or unknown state are shown in grey. 

In the following example, the account has one resource with an alarm in
a critical state, which is shown, and 10 resources with alarms in an OK
state.

In the following example, the account has one resource with an alarm in
a critical state.

![](/knowledge_center/sites/default/files/field/image/newResourceWithCriticalState.png)

If a resource has multiple alarms with different states (for example,
one critical alarm and one warning alarm), the resource appears by
default on the status tab of the *most critical state*.

View Monitoring Details
-----------------------

If you tap a resource, you can see the monitoring checks, the alarm
status of each check, and a graph showing data over time.

In the following example, the Remote Ping check has a problem.  Click on
the check to expand the view and see a graph of data over time. You can
swipe to view multiple graphs.

![](/knowledge_center/sites/default/files/field/image/newMonitoringDetails.png)

View Errors
-----------

Monitored resources that are highlighted in grey might have an error.
You can diagnose errors with checks by visiting the Cloud Control Panel
(for Cloud Servers), or by using the Rackspace Monitoring API (for all
other resources).

![](/knowledge_center/sites/default/files/field/image/newDetailsGray.png)

View Resources with No Status Available
---------------------------------------

If your monitored resource is grey, it might have no status.  A resource
can have no status for the following reasons:

-   You have disabled all alarms.
-   You have deleted all alarms.

When there are no alarms configured, there are no thresholds to trigger
a change in the state of the alarms and the app cannot deliver a status
for that resource.  You can configure alarms for Cloud Servers in the
Cloud Control Panel. To configure alarms for all other resources,
use the Monitoring API.  For information about how to use the API, see
the *[Rackspace Monitoring Developer
Guide](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/)*.

![](/knowledge_center/sites/default/files/field/image/newDetailsNoAlarm.png)

Monitor Cloud Databases
-----------------------

Cloud Databases are provisioned with six default checks and one alarm. 
Cloud Database users can view metrics and graphs for all checks *except*
the MySQL check. 

The preconfigured alarm provides warning and critical thresholds for low
disk space *only*.  For this reason, the status bar on any MySQL
instance shows a green status whenever the disk space is within
threshold.  There is no status change if other checks are high or low
because no alarms or thresholds have been set.  You can configure
additional alarms and notification plans by using the Cloud Databases
API.  For more information, see the [Monitoring Cloud
Databases](https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#document-general-api-info/monitoring-cloud-databases)
section in the *Cloud Databases Developer Guide*.  At this time, Cloud
Database users cannot configure additional checks.

