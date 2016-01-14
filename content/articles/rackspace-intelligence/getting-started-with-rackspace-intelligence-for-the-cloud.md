---
node_id: 4878
title: Getting started with Rackspace Intelligence for the cloud
type: article
created_date: '2015-10-20 13:29:13'
created_by: constanze.kratel
last_modified_date: '2016-01-11 20:1545'
last_modified_by: constanze.kratel
product: Rackspace Intelligence
body_format: tinymce
---

**Note**: This guide is for Rackspace Intelligence on a standard cloud
account. If you have a dedicated account, click
[here](https://www.rackspace.com/knowledge_center/article/getting-started-with-rackspace-intelligence-for-dedicated-accounts)
for the applicable getting started guide.

Rackspace Intelligence provides a data panel, called a *dashboard*, that
shows actionable insights into infrastructure health. You can use these
insights to improve system performance and availability.

The Rackspace Intelligence dashboard performs different functions than
control panels such as the Cloud Control Panel. You use a control panel
to create the actual entities, such as cloud servers and cloud
databases. For entities that already exist and are known to Rackspace
Intelligence, you use the Rackspace Intelligence dashboard to monitor
and visualize the status of the entities.

You can use Rackspace Intelligence to help you understand the following
kinds of entities:

-   Rackspace cloud servers
-   Rackspace cloud databases
-   Other entities, which need not be hosted at Rackspace and need not
    be servers or databases

Only data available to Rackspace Intelligence can be gathered and acted
on. For example, if you define a website that is hosted outside
Rackspace as an entity, then you might be able to usefully place a check
on its ping time, but you probably wo&rsquo;t to be able to check the space
available in its file system.

**Note:**Early publications about Rackspace Intelligence referred to it
as*Cloud*Intelligence. Because the service is meant to be useful for
both cloud and dedicated devices, it is now
named*Rackspace*Intelligence. The Rackspace Intelligence team is working
to add support for dedicated accounts.

* * * * *

**Contents:**

*Before you begin using Rackspace Intelligence*

-   [Learn Rackspace Intelligence vocabulary](#concepts)
-   [Explore the Rackspace Intelligence dashboard](#ui-intro)

*Every time you use Rackspace Intelligence*

-   [Log in](#login)

*When you begin working with a new entity*

-   [Prepare entities to be monitored by Rackspace
    Intelligence](#preparing)

*When you change how Rackspace Intelligence monitors your
infrastructure*

-   [Monitor entities](#monitor-entities)
-   [Monitor open alerts](#monitor-open-alerts)

*When you change how Rackspace Intelligence communicates its findings*

-   [Report infrastructure status](#report-status)
-   [Schedule suppression of status
    notifications](#schedule-suppressions)
-   [E](#examine-log-suppressed)[xamine the suppression
    log](/knowledge_center/article/examining-the-log-of-alerts-suppressed-by-rackspace-intelligence).

*When you want to see what Rackspace Intelligence sees*

-   [Visualize infrastructure status](#visualize)

*When you want to create checks and alarms for your entities*

-   [Create and manage checks and alarms](#manage-checks-and-alarms)

See also [Learning about Rackspace
Intelligence](/knowledge_center/article/learning-about-rackspace-intelligence) for
a list of the articles that this getting started article links to, plus
other resources.

* * * * *

Before you begin using Rackspace Intelligence
---------------------------------------------

You can use Rackspace Intelligence most effectively if you prepare
yourself by learning its terminology and exploring its user interface.

### Learn Rackspace Intelligence vocabulary

To be able to fully use the features Rackspace Intelligence offers, you
need to familiarize yourself with the basic concepts about entity
monitoring and metrics. See [Learning the Rackspace Intelligence
vocabulary](/knowledge_center/article/learning-intelligence-vocabulary) for
more details.

### Explore the Rackspace Intelligence user interface

Actions that you can perform in the user interface are grouped into four
sections:  **Monitor**, **Suppress**, **Notify**, **Visualize**. Within
each section, you can drill down to get details. See [Understanding the
Rackspace Intelligence user
interface](https://admin.rackspace.com/knowledge_center/article/understanding-the-rackspace-intelligence-dashboard-user-interface) for
more details.

* * * * *

Log in
------

If you have a Rackspace cloud account, you are authorized to use
Rackspace Intelligence.

Before you can use [Rackspace
Intelligence](https://intelligence.rackspace.com/), you must be logged
in to your [Cloud Control Panel](https://mycloud.rackspace.com/)
account. [Log in to Rackspace
Intelligence](/knowledge_center/article/logging-into-the-rackspace-intelligence-dashboard)
explains how that works.

* * * * *

Prepare entities to be monitored by Rackspace Intelligence
----------------------------------------------------------

As soon as it becomes aware of an entity, Rackspace Intelligence can
discover and display basic status information about it. Rackspace
Intelligence can give you deeper insights about an entity if you
configure that entity to provide more information. See [Preparing to use
Rackspace
Intelligence](https://admin.rackspace.com/knowledge_center/article/preparing-to-use-rackspace-intelligence) for
suggestions on steps that you can take to maximize the information
available to Rackspace Intelligence.

* * * * *

Using the Rackspace Intelligence dashboard
------------------------------------------

You can use the Rackspace Intelligence dashboard to examine and manage
how Rackspace Intelligence interacts with your infrastructure. The
Rackspace Intelligence dashboard provides information about the
following items:

-   Entities monitored by Rackspace Intelligence
-   Open alerts
-   Notifications
-   Notification plans
-   Current suppressed notifications
-   Notifications that were suppressed in the past

You can also use the Rackspace Intelligence dashboard to [generate
graphs](/knowledge_center/article/getting-started-with-rackspace-intelligence#visualize) to
visualize infrastructure status.

### Identify infrastructure to be monitored

You can use the **Monitor**, **Suppress**, **Notify**,
and **Visualize** sections of the interface to examine events in your
configuration.

#### Monitor entities

The [list of
entities](/knowledge_center/article/monitoring-entities-with-rackspace-intelligence) identifies
all entities known to Rackspace Intelligence. While displaying the list
of known entities, you can perform management functions such
as [defining new
entities](/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#create-entities).

#### Create and manage checks and alarms

Rackspace Intelligence provides a wizard that lets you [create
monitoring
checks](/knowledge_center/article/working-with-checks#createcheck) to
collect metric data for your infrastructure. You can [set up
alarms](/knowledge_center/article/working-with-alarms#create-alarm) for
your checks to get notified when certain metric data meet criteria. You
can also perform management functions, such as [editing your
checks](/knowledge_center/article/working-with-checks#editcheck) and
[editing your
alarms](/knowledge_center/article/working-with-alarms#editalarm).

#### Monitor open alerts

The [list of open
alerts](/knowledge_center/article/monitoring-open-alerts-with-rackspace-intelligence) identifies
all entities that are currently in a status for which you have asked
Rackspace Intelligence to trigger alarms. Depending on the [notification
plans](/knowledge_center/article/managing-rackspace-intelligence-notification-plans) that
you have defined, appropriate communications and actions might have
already occurred in response to these alerts. Examining the list
directly means that, whether or not you were
automatically [notified](/knowledge_center/article/managing-rackspace-intelligence-notifications) of
a status change, you can investigate infrastructure status in context.

### Report infrastructure status

When Rackspace Intelligence detects a status change, it can report its
findings by sending email or a text message. Rackspace Intelligence can
also respond to a status change by executing a policy that was defined
by
a [webhook](http://docs.rackspace.com/cas/api/v1.0/autoscale-gettingstarted/content/Authenticated_Webhooks_and_Anonymous_Webhooks.html).

To customize how Rackspace Intelligence responds when it detects a
status change, perform the following actions:

-   Define [notifications](/knowledge_center/article/managing-rackspace-intelligence-notifications),
    providing contact details
-   Define [notification
    plans](/knowledge_center/article/managing-rackspace-intelligence-notification-plans),
    defining which notifications to perform under which circumstances

### Suppress reporting of infrastructure status

Rackspace Intelligence enables you to [suppress
notifications](/knowledge_center/article/scheduling-suppression-of-rackspace-intelligence-notifications) for
cases when notifications are temporarily inappropriate, such as during
scheduled maintenance activity.

To investigate status changes while notifications were suppressed, you
can [examine the suppression
log](/knowledge_center/article/examining-the-log-of-alerts-suppressed-by-rackspace-intelligence).

### Visualize infrastructure status

Rackspace Intelligence can report its findings visually with predefined
or custom graphs:

-   With [basic
    graphs](/knowledge_center/article/visualizing-with-rackspace-intelligence-default-graphs),
    you can observe changes in the status of an entity during a time
    range.
-   With [custom
    graphs](/knowledge_center/article/visualizing-with-rackspace-intelligence-custom-graphs),
    you can compare multiple entities and multiple metrics.


