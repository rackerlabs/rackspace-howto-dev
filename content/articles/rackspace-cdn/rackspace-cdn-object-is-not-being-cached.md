---
node_id: 5159
title: Rackspace CDN - Object is not being cached
type: article
created_date: '2016-01-19'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Catherine Richardson
product: Rackspace CDN
body_format: tinymce
---

When an object that is defined in the origin and in the appropriate path
is not cached by Akamai, you should contact Rackspace Support for
assistance.

However, the following information, which is extracted from several
articles from Akamai, provide some insight into why this situation might
occur.



<div id="expander-1443396478" class="expand-container">

Why is my cacheable content not being cached on Akamai?
-------------------------------------------------------

<div class="expand-control">

The most common cause for cacheable content not being cached is a
**Vary** header served by the origin server.

The **Vary** header instructs Akamai servers that content might differ
based on some characteristic, and hence, it is uncacheable. This
behavior is valid per RFC HTTP/1.1. Specifically, Akamai will not cache
content if the origin server response includes a **Vary** header with a
value other than **<span>Vary: Accept-Encoding</span>**. Akamai will
cache responses with **<span>Vary: Accept-Encoding</span>** only if they
are accompanied by **<span>Content-Encoding: gzip</span>**.



Will Akamai cache objects with a **Vary** response header containing multiple values, including **Accept Encoding**?
--------------------------------------------------------------------------------------------------------------------

Akamai will not cache any response with a **Vary** header set to
something  other than **Accept-Encoding**.

For example, when **Vary: Accept-Encoding** is specified, the object is
cached at Akamai.

However, when **Vary: Accept-Encoding,User-Agent** is specified, Akamai
will not cache the object because it contains a value other than
**Accept-Encoding**.



</div>

</div>

<div id="expander-822237047" class="expand-container">

If the origin server's **Vary** header contains anything other than **Accept-Encoding**, why do Akamai servers not cache objects?
---------------------------------------------------------------------------------------------------------------------------------

This requirement is necessary to prevent different versions of content
from being cached and then later served to end users for which they are
not intended. For instance, this prevents pages in one language from
being cached and served to users of another language, or pages designed
specifically for a certain browser from being cached and then served to
users on another browser.

The HTTP Vary header is used by servers to indicate that the object
being served will vary (the content will be different) based on some
attribute of the incoming request, such as the requesting client's
specified user-agent or language. The Akamai servers cannot cache
different versions of the content based on the values of the Vary
header. As a result, objects received with a Vary header that contains
any value(s) other than "Accept-Encoding" will not be cached. To do so
might result in some users receiving the incorrect version of the
content (wrong language, etc.)

An **Accept-Encoding** value to the **Vary** header is the exception to
this rule only when it relates to serving the object compressed. Because
compression does not change the content of the object (only its size for
transfer), an object that varies only by its compression can be safely
cached.

To summarize, Akamai servers will cache the object, based on the
configuration settings, in either of the following cases:

-   If **Vary: Accept-Encoding** is received and the content is served
    compressed (**Content-Encoding: gzip**).
-   If no **Vary** header at all is received.



If I have specified in the configuration file that an object should be cached by Akamai, why do I see every hit coming back to my origin server?
------------------------------------------------------------------------------------------------------------------------------------------------

<div class="expand-control">

Here are the most prevalent reasons why content that is specified to be
cached does not get cached on an edge server:

-   Another configuration setting overrides the cache setting.
-   The origin server sends a **Vary** header.
-   Query strings are making your objects unique.
-   The request is a **POST** request.
-   The origin server returns a 302 redirect.
-   The origin server sends no-store **Cache-Control** and **Expires**
    headers and the configuration is setup to honor **Cache-Control**
    and **Expires** headers.
-   The origin server is sending an **Edge-Control** header
    specifying no-store.
-   The **Content Length** header from the origin does not match the
    actual content length.
-   The **Date** header from the origin does not represent meaningful
    time because the origin clock is not synched up.
-   The **Age** header from the origin is inconsistent.
-   Authentication or revalidations settings require all objects to
    check freshness with origin every time.
-   The object is Edge Side Includeds(ESI)-processed or is a fragment
    from an ESI include.
-   The ETag is mismatched from the origin.
-   ESSL is used, and even though a request goes to the same VIP, it
    resolves to a different physical IP behind the VIP. So, it appears
    that the VIP doesn't have it in cache.

</div>

</div>

<div id="expander-1442541803" class="expand-container">

<div id="expander-control-1442541803" class="expand-control">

<span class="expand-control-icon icon"> </span>

</div>

</div>

