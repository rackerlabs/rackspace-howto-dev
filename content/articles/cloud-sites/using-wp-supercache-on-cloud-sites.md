---
node_id: 702
title: Using WP-SuperCache to optimize Wordpress on Cloud Sites
type: article
created_date: '2011-03-16 21:57:40'
created_by: thomas.hester
last_modified_date: '2014-10-15 21:2202'
last_modified_by: jered.heeschen
product: Cloud Sites
body_format: tinymce
---

undefined&rsquo;t cache pages for known users. (Recommended)
-   Cache rebuild. Serve a supercache file to anonymous users while a
    new file is being generated. (Recommended)
-   Mobile device support. (External plugin or theme required. See the
    FAQ for further details.)
-   Extra homepage checks. (Very occasionally stops homepage caching)
    (Recommended)

After making those changes, click **Update Status**.

#### Mod\_rewrite settings

After the screen refreshes scroll down to the Mod Rewrite Rules section
and click **Update Mod\_Rewrite Rules**.

![](/knowledge_center/sites/default/files/field/image/RewriteRules1.png)

#### Expiry time and garbage collection

Scroll down to **Expiry Time & Garbage Collection**.

![](/knowledge_center/sites/default/files/field/image/gc_1.png)

Change cache timeout to 0 seconds then click **Change Expiration**.

#### Preload settings

Click on the **Preload** tab next.

![](/knowledge_center/sites/default/files/field/image/Preload_0.png)

-   Select **Preload mode (garbage collection only on legacy cache
    files. Recommended.)**.
-   Set the refresh rate for preloaded supercache files by changing the
    number of minutes in the **Refresh preloaded cache files every
    \_\_\_ minutes**field (0 to disable, minimum 30 minutes) to a
    number appropriate for the traffic your site receives, like 1440 (24
    hours) or 10080 (1 week).
-   Click **Update Settings**, then after the page refreshes click
    **Preload Cache Now** and in around 10 or 15 seconds the cache will
    start building for the site. Depending on the size of the site and
    amount of content, the cache will take a few seconds to a minute to
    build. Once complete you will see a much improved response and load
    time.

Any time a layout change has been made (such as adding a widget or
changing the theme), it will be necessary to go to the admin panel and
click **Delete cache**, verify your page looks as you want, then go into
into the Supercache settings, go to the **Preload** tab and click
**Preload Cache Now** to regenerate the cache for the site.

### Updating the Supercache plugin

For security purposes and optimizations, it is important to keep the
plugin (and Wordpress itself) up-to-date. This can be done through the
Wordpress Dashboard.

1.  Login to your WordPress Dashboard.
2.  Click the **Plugins** tab on the left-hand column.
3.  Check the box next to **Plugin** to select all available plugin
    updates.
4.  Click the **Bulk Actions** drop down and select **Update**.
5.  Click **Apply**.
6.  The page will change once all of the plugins are updated.


