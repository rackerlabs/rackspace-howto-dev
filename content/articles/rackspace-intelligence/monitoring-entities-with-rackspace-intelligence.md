---
node_id: 4751
title: Monitoring entities with Rackspace Intelligence
permalink: article/monitoring-entities-with-rackspace-intelligence
type: article
created_date: '2015-07-17 10:27:17'
created_by: rose.coste
last_modified_date: '2015-08-17 21:4306'
last_modified_by: kyle.laffoon
products: Rackspace Intelligence
body_format: tinymce
---

Rackspace Intelligence lets you create, edit, and view entities.

Like Cloud Monitoring, Rackspace Intelligence uses *entities* to
represent any object or resource that you want to monitor. An entity can
be a set of servers or non-server objects, but most often an entity
refers to an individual server.

You can define an entity in Rackspace Intelligence that is something
other than a Rackspace cloud server or a Rackspace cloud database. You
can create an entity to represent any server or website that you want to
monitor, even if it is not hosted at Rackspace.

As you create new Rackspace cloud servers or cloud databases, Rackspace
Intelligence entities representing them are created automatically.

To see a list of the entities known to Rackspace Intelligence,
select **Monitor** at the top of the Rackspace Intelligence interface,
and then click **Entities**.

![](/knowledge_center/sites/default/files/field/image/intelligence-monitoring-create-entity-top-bar.png)

From the Monitor Entities section, you can perform the following actions
on the list of entities:

-   [Sort
    entities](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#sort-entities)
-   [View the details of an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#see-details-entities)
-   [Create an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#create-entities)
-   [Update an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#update-entities)
-   [Visualize an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#visualize-entity)

Sort entities
-------------

You can sort the list of monitored entities by entity name, by the
number of alarms reported for each entity in the Critical, Warning, and
OK categories, and by the number of monitoring checks reported for each
entity.

View the details of an entity
-----------------------------

All the entity labels in Rackspace Intelligence are linked to an entity
details page. To view the details page for an entity, click on the
entity's name. The following information about the entity is displayed:

-   Monitoring details, such as IP addresses and RAM configured for the
    entity
-   Monitoring checks, listing numbers of critical, warning, and OK
    alarms fired for each check activated for the entity
-   Suppressions, showing any alarms currently muted for this entity

If the entity is a cloud server, the details page provides the same
information that you can get about the server by using the Cloud Control
Panel or by logging in to the server itself.

Create an entity
----------------

1.  To create a new entity, on the Monitoring page, click **Create
    Entity**.

![](/knowledge_center/sites/default/files/field/image/intelligence-monitoring-create-entity-button.png)

2.  Type a name for your entity and click **Create Entity.**

Rackspace Intelligence creates the entity and displays the information
on the entity details page. You can now update the entity by adding an
IP address or a check. See the next section for instructions.

Update an entity
----------------

You can update an existing entity by clicking the **Actions** menu at
the top of the entity details page.

You can perform the following updates on an entity:

-   [Rename an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#rename-entities)
-   [Add an IP address to an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#adding-ip-address)
-   [Delete an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#deleting-entity)
-   [Create a check for an
    entity](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#creating-check)
-   [Create a
    suppression](https://admin.rackspace.com/knowledge_center/article/monitoring-entities-with-rackspace-intelligence#create-suppression)

### Rename an entity

1.  To rename an entity, select **Rename Entity**from the **Actions**
    menu.
2.  Type a new name in the **Rename Entity**box, and then
    click **Rename**.

The new name appears on the entity details page.

### Add an IP address to an entity

You can add one or more IP addresses to an entity. You can reference
these IP addresses by the checks on the entity.

1.  To add one or more IP addresses, select **Add IP**from the
    **Actions** menu..
2.  On the **IP Addresses** page, specify a label for the IP address,
    type the numbers for the IP address, and then click **Add**.
3.  To add another IP address, repeat the preceding step.
4.  After you have added all your IP addresses, click **Save**.

The IP addresses that you added appear on the entity details page.

### Delete an entity

1.  To delete an entity, select **Delete Entity**from the **Actions**
    menu.
2.  To confirm that you want to permanently delete the entity,
    click **Delete**.

The entity is permanently deleted from the database and is no longer
monitored by Rackspace.

### Create a check for an entity

1.  To create a check for an entity, select **Create Check**from the
    **Actions** menu.
2.  Select a check from the **Check Type** list, and then enter all the
    required information.

**Note:** Different check types require different values of input. For
more information, see [Working with
checks.](/knowledge_center/article/working-with-checks)

1.  Click **Create Check**.

Rackspace Intelligence creates the check and displays the details on the
check details page. If your check requires a monitoring agent to be
installed to collect metrics, a message is displayed in the **Check
Details**section.

### Create a suppression

1.  To create a suppression, select **Create Suppression**from the
    **Actions** menu.

On the **Create a Suppression** page, your entity is displayed in
the **Suppression Targets** section.

1.  Type a name for your suppression, and specify the start and end
    dates.
2.  To add an additional entity to this supression, click **Add
    Entities **and select one or more entities.
3.  Click **Create Suppression**.

![](/knowledge_center/sites/default/files/field/image/intelligence-entities-create-suppression.png)

5.  When asked to confirm that you want to create a suppression,
    click **Create Suppression Now**.

For more information about suppressions, see [Working with notification
suppressions](/knowledge_center/article/working-with-notification-suppressions).

Visualize an entity
-------------------

In the list of entities, click in the **Visualize** column of the row
for an entity to launch a **Default Graphs** presentation for the
entity. The page shows any graphs that are available for checks
configured for the entity.

![](/knowledge_center/sites/default/files/field/image/intelligence-visualize-defaultgraphs-1on1off.png)

For checks that are defined but not configured, a link to begin the
process of configuring the check is provided.

