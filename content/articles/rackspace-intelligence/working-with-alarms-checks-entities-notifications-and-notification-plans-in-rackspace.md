---
node_id: 4842
title: 'Working with alarms, checks, entities, notifications, and notification plans in Rackspace Intelligence for dedicated accounts'
type: article
created_date: '2015-10-14 18:32:09'
created_by: constanze.kratel
last_modified_date: '2015-12-17 18:4343'
last_modified_by: constanze.kratel
product: Rackspace Intelligence
body_format: tinymce
---

Rackspace Intelligence provides a user interface that displays
configuration information about the following items:

-   [Entities](#entities)
-   [Checks](#checks)
-   [Alarms](#alarms)
-   [Open alerts](#open_alerts)
-   [Notifications](#notifications)
-   [Notification plans](#notification_plans)

Entities
--------

To view the configuration information for a specific item, you typically
start off with a list of all the entities that have been set up and
configured for your system.

To obtain a list of entities, on the Rackspace Intelligence interface,
perform the following steps:

1.  Click **Monitor**, and then click the **Entities** tab.

    ![](/knowledge_center/sites/default/files/field/image/Entity%20List1_0.png)

2.  To view details about a specific entity, click the link for the
    entity.\
     The top of the details page shows information about the  entity.

    ![](/knowledge_center/sites/default/files/field/image/Entity%20Details1.png)

 

Checks
------

 
-

Rackspace Intelligence lets you view the configuration of checks that
were created for an entity. Customers with dedicated accounts can use
remote checks. Remote checks monitor an entity's Internet
connectivity. Remote checks are performed by attempting to contact the
entity from outside the entity. For more information, see [Remote check
types](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/#remote-check-type-ref).

Rackspace Intelligence for dedicated accounts supports the following
remote checks:

-   [ping](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/#remote-ping)

-   [tcp](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/#remote-tcp)

-   [http](https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/#remote-http)

To view a check on the Intelligence interface, perform the following
steps:

1.  Click **Monitor** and then click the **Entities** tab.
2.  Click the entity for which you want to view check details.
3.  On the entity details page, scroll to the Monitoring Checks section
    and click the link for the check that you want to view.\
     A page that lists the check details is displayed.

    ![](/knowledge_center/sites/default/files/field/image/Check%20Details1.png)

 

Alarms
------

Rackspace Intelligence supports alarms that analyze the data that is
collected by a check.

The alarm criteria contain the logic to process this data and convert
the alarm into one of the following states: OK, WARNING, CRITICAL.
Rackspace Intelligence lets you view the alarms that have been
configured for your entities.

To view an alarm, perform the following steps:

1.  Click on the details page for an entity, click the check for which
    you want to view the alarm
2.  Scroll to the **Monitoring Alarms******section and click the alarm
    for which you want to view details.\
     The alarm detail are displayed.

    ![](/knowledge_center/sites/default/files/field/image/Alarm%20Details1.png)

 

Open alerts
-----------

Open alerts report statuses that you have asked Rackspace Intelligence
to monitor.

You can view a list of all open alerts by clicking** Monitor** at the
top of the Rackspace Intelligence interface and then clicking **Open
Alerts**.

![](/knowledge_center/sites/default/files/field/image/Open%20Alerts.png)

 

Notifications
-------------

Rackspace Intelligence lets you view notifications that have been
created for your entities. Notifications must be defined before you can
set up a notification plan for an entity. For example, you can define a
method of contacting a support engineer by SMS and a method of
contacting a manager by email.

To view the notifications that have been configured for you, click
**Notify** at the top of the Rackspace Intelligence interface, and then
click the **Notifications** tab. This action displays the
**Notifications** page, which lists all the notifications that have been
configured for you.

![](/knowledge_center/sites/default/files/field/image/Notifications1.png)

Notification plans
------------------

You can have notification plans defined that work with your monitoring
checks and alarms. You can specify several ways to notify members of
your team (notifications) and then assemble those notifications into
notification plans.

To view the notification plans that have been configured for you, select
**Notify** at the top of the Rackspace Intelligence interface, and then
click the **Notification Plans** tab. This acction displays the
**Notification Plans** page.
![](/knowledge_center/sites/default/files/field/image/Notification%20Plans1.png)

