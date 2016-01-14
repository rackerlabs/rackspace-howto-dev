---
node_id: 4633
title: Configure Cloud Feeds archiving in the Cloud Control Panel
type: article
created_date: '2015-04-03 17:42:06'
created_by: greg.sharek
last_modified_date: '2015-10-30 16:4357'
last_modified_by: constanze.kratel
product: Cloud Hosting
body_format: tinymce
---

Cloud Feeds archives your events, based on region, by storing the data
in a Cloud Files container in a particular region. Archiving enables you
to store your events for a longer time period in case you need to
support security or compliance auditing.

You can elect to have your events stored in one or more Cloud Files
containers. During the archiving process, events are written to files
and are organized by date, feed, and region. Files are formatted as a
static feed page for a single day for a single feed in a region. You can
walk through your archived feeds (similar to regular feeds) by using
next-archive and prev-archive links that point to the next and previous
days.

Cloud Feeds provides the following options for storing the archive data:

-   Store all data at a default location, which is specified as one
    default container URL. With this option, feeds from all worldwide
    regions are stored in a single Cloud Files container in a single
    region.<br>
      
-   Store the data dependent on a specified region. For example, an
    event originating from the LON region is stored in a Cloud Files
    container in LON, and an event originating from the SYD region is
    stored in a Cloud Files container in SYD. This option requires you
    to specify an archive container URL for each region. Events can also
    be configured to be stored in any arbitrary region.<br>
      
-   Store some of the data at the default location, and some of the data
    at a specific, region-based container URL.

To configure archiving for Cloud Feeds
--------------------------------------

1.  Log in to the Rackspace [Cloud Control
    Panel](https://mycloud.rackspace.com/).<br>
      
2.  On the top-right corner, click the **Account**menu, and then
    select **Account Settings**.<br>
      
3.  In the **Cloud Feeds Archiving **section, click **Enable
    Archiving**.<br>
      
4.  In the Cloud Feeds Archiving dialog box, select one or more check
    boxes for your preferred **Event Format**(XML, JSON, or both).<br>
      
5.  Under **Storage Configuration**, select **Basic**  if you want to
    store your Cloud Feeds events in a default Cloud Files container in
    a single region. If no container exists, it will be created
    automatically. Select the appropriate region from the list and
    specify a container name.<br>
     <br>
     **Note:**If you want to specify different Cloud Files containers or
    regions for archiving your Cloud Feeds events, you can
    select**Advanced**. If you select **Advanced**, you must work with
    Rackspace support to configure your advanced archiving settings or
    use the [Cloud Feeds Archiving Configuration
    API](http://docs.rackspace.com/cloud-feeds/api/v1.0/feeds-devguide/content/Preferences_API.html).<br>
      
6.  Click **Save Configuration**.<br>
     <br>

    ![](/knowledge_center/sites/default/files/field/image/Cloud%20Feeds%20archiving.png)

 

For more information about Cloud Feeds archiving, see [Archiving
overview](http://docs.rackspace.com/cloud-feeds/api/v1.0/feeds-devguide/content/Archiving_Overview.html) in
the [Rackspace Cloud Feeds Developer
Guide](http://docs.rackspace.com/cloud-feeds/api/v1.0/feeds-devguide/content/overview.html).

 

