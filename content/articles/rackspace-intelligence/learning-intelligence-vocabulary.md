---
node_id: 4764
title: Learning the Rackspace Intelligence vocabulary
type: article
created_date: '2015-07-28 16:23:22'
created_by: constanze.kratel
last_modified_date: '2015-08-18 16:2554'
last_modified_by: kyle.laffoon
product: Rackspace Intelligence
body_format: tinymce
---

To tell Rackspace Intelligence which aspects of your configuration to
monitor for you, you define your objectives in the following terms:

-   *Entities* to be monitored<br>
     For example, you can define a cloud server as an entity.<br>
      
-   *Checks* that focus on a particular aspect of an entity's behavior<br>
     For example, a check can monitor a cloud server's RAM usage.<br>
      
-   *Alarms* that define the limits of the entity's behavior<br>
     For example, alarm criteria identify whether RAM usage is in one of
    the following states: OK, WARNING, or CRITICAL.<br>
      
-   *Alerts* that announce when a monitored entity has triggered an
    alarm<br>
     For example, an alert reports that RAM usage has reached the
    CRITICAL level.<br>
      
-   *Notification plans* that define how to communicate alerts<br>
     For example, a notification plan requests notification of the help
    desk and the on-call system administrator. <br>
      
-   *Notifications* that define the contact information used in
    notification plans<br>
     For example, notifications to the on-call system administrator are
    sent as text messages to a specific telephone number. <br>
      
-   *Visualizations* that present data meaningfully<br>
     For example, a RAM usage graph shows growth leading up to the
    triggered alarm.

[&ldquo;Single Pane of Glass&rdquo; for Your IT
Ops](http://www.rackspace.com/blog/cloud-monitoring/) discusses these
concepts in the context of Cloud Monitoring. Rackspace Intelligence acts
as a dashboard to help you interact with data collected by Cloud
Monitoring.

