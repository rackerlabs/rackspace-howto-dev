---
node_id: 4528
title: Sharing images in the Cloud Control Panel
type: article
created_date: '2015-01-29 20:56:07'
created_by: cloud.images
last_modified_date: '2015-03-17 17:2137'
last_modified_by: kyle.laffoon
product: Cloud Images
body_format: tinymce
---

undefined&mdash; it won't show up as an option in the
Region dropdown on either the Server List or Create Server pages. API
users can look directly in their service catalog.

To learn more about regions in the Rackspace cloud, please see the
Knowledge Center article [Where are the Rackspace data centers
located?](/knowledge_center/article/where-are-the-rackspace-data-centers-located).

### Image sharing courtesy {#courtesy}

To keep the Rackspace cloud a friendly place, observe the following
suggestions:

-   Don't share images with random customers. Share only with customers
    with whom you have some kind of connection.
-   If a sharing request is in the Pending Acceptance status for a
    while, verify that you entered the correct account number before
    sending a reminder.
-   If a sharing request is rejected, don't take it personally.
-   If a potential image consumer rejects your image but then contacts
    you to request it again, remove the consumer from the image and then
    re-share the image with the consumer.  As an image producer, you
    cannot directly change their status.

Accept or reject a shared image {##accepting}
-------------------------------

As explained earlier, to prevent spam in your image list, you must
accept an image before it appears in your image list.  There are two
places in the Cloud Control Panel where you can find out whether someone
has shared an image with you:

-   **Your list of Saved Images:** When someone has shared an image with
    you, a notification appears at the top of your list of saved
    images.  Because an image exists in a particular region, this
    notification is visible only when the region selector at the top of
    the list is set to **All Regions (Global)** or to the region in
    which the image exists.
-   **On the Create Server page:** If you are creating a server in a
    region in which someone has shared an image with you, a notification
    appears at the top of the image selector.

If you accept an image, the notification disappears and the image
appears among your Saved Images.  On the Saved Images page, the
text **Shared Image** appears in the **Source** column.  In the image
selector on the Create Server page, select **Saved Images** and
then **Shared Images**.

If you reject the image, it does not appear your image list and the
notification disappears.

If you don't want to boot from the image now and want to postpone the
decision to accept or reject the image, simply close the dialog box and
the notification will remain.

### **Reject an image after accepting it**

If you accept an image and then decide later that you don't want it, you
can reject it. 

1.  Find the image in your list of Saved Images. ,
2.  Click the gear icon to the left of the image name, and
    select **Remove Image**. 

### **Accept an image after rejecting it**

If you reject an image and decide later that you want it after all, you
must notify the image producer and ask that the image be re-shared with
you.

Use a shared image {#using}
------------------

After you accept a shared image, you can use it to boot a server using
your normal workflow.  However, we encourage you to consider the
following information before booting a server from a shared image:

-   **Shared images are nonstandard images** (for more information, see
    [Standard and Non-Standard
    Images](https://admin.rackspace.com/knowledge_center/article/rackspace-standard-and-non-standard-images)).
    For servers booted from nonstandard images, you may expect that we
    will ensure host servers are functioning properly and that the API
    availability meets the SLA. *However, we cannot promise to support
    servers booted from shared images in the same way we support servers
    booted from Rackspace base images.*  We create the base images
    ourselves and know exactly what's on them, whereas the point of
    shared images is to empower our customers to use images we haven't
    even dreamed of.  So although you can expect support, you can't
    expect our support staff to know the intricacies of Exotic OS, for
    example, in the same way they know CentOS.
-   Verify that there are no strange users with login privileges in
    /**etc/passwd** and that there aren't any strange SSH keys
    preinstalled on the server. 
-   **Build critical infrastructure components only from images created
    by people you completely trust.**If you suspect that an image shared
    with you contains malware or is behaving strangely, you can report
    such suspicious activities to Rackspace Support and
    to [cloudimageshelp@rackspace.com](mailto:cloudimageshelp@rackspace.com).


