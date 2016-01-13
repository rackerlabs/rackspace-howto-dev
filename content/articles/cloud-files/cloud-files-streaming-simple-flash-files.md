---
node_id: 77
title: Cloud Files - Streaming Simple Flash Files
type: article
created_date: '2011-03-08 19:30:04'
created_by: RackKCAdmin
last_modified_date: '2014-09-30 15:5124'
last_modified_by: kyle.laffoon
products: Cloud Files
body_format: tinymce
---

***Note:** We've had some reports of problems getting the current
version of FlowPlayer (3.2.14) working with Cloud Files and are
investigating. We'll update this article when we have more information.*

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 Overview](#Overview)                                              |
| -   [2 What we need](#What_we_need)                                      |
| -   [3 FlowPlayer](#FlowPlayer)                                          |
| -   [4 The Cross Domain XML file](#The_Cross_Domain_XML_file)            |
| -   [5 The xhtml](#The_xhtml)                                            |
| -   [6 Lets test it out](#Lets_test_it_out)                              |
+--------------------------------------------------------------------------+

### Overview

In this tutorial we will cover how to stream media files from Cloud
Files to a Web Site. This tutorial assumes you have a Video file
uploaded to Cloud Files and the container it is in is public. We will be
using [FlowPlayer](http://flowplayer.org "http://flowplayer.org"); it is
an open source Flash Video Player registered under the GPL.

### Streaming

Cloud Files containers published and marked **public** are delivered
over [Akamai Technologies,
Inc](http://www.akamai.com/ "http://www.akamai.com/").'s global Content
Delivery Network (CDN). For streaming flash files from your Cloud Files,
Akamai provides pseudo streaming. You can find additionl information
online, but a great explanation (in Flash) is provided at:
[http://www.longtailvideo.com/support/jw-player/28855/pseudo-streaming-in-flash/](http://www.longtailvideo.com/support/jw-player/28855/pseudo-streaming-in-flash/).
\
*"Pseudo-streaming works as follows: When the video is initially loaded,
the player reads and stores a list of seek points as part of the video's
metadata.  These seek points are offsets in the video (both in seconds
and in bytes) at which a new keyframe starts)."*\
\
To accomplish this, Akamai's streaming supports the HTTP Range Header to
identify those seek points. More information on the Range header is
available: 
[http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html\#sec14.35](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.35).
RTMP (Real Time Messaging Protocol) Streaming is not supported. \
\
There is a difference in the pseudo streaming and what Akamai offers
with their iOS streaming. iOS Streaming is a form of adaptive streaming.
\
\
"The encoder (or a separate segmented process) will produce H.264/AAC
content in a sequent of small content segments, in MPEG-2 TS format
(.ts).  There is also a m3u8 index file that references these segments;
in the case of live content the M3U8 is continuously updated to reflect
the latest content. \
\
More information is available at:

-   [http://developer.apple.com/library/ios/\#technotes/tn2224/\_index.html](http://developer.apple.com/library/ios/#technotes/tn2224/_index.html)
-   [http://www.akamai.com/dl/akamai/iphone\_wp.pdf](http://www.akamai.com/dl/akamai/iphone_wp.pdf)

 

#### Supported Formats/Codecs

The following formats are supported by Akamai streaming.

+--------------------+--------------------+--------------------+--------------------+
| **Container**      | **Video Codec**    | **Audio Codec**    | **Comments**       |
+--------------------+--------------------+--------------------+--------------------+
| FLV                | H.263              | MP4                | Video only works   |
|                    |                    |                    | as well.           |
|                    | H.264              | AAC                |                    |
|                    |                    |                    | For Nellymoser,    |
|                    | VP6                | PCM                | only the           |
|                    |                    |                    |                    |
|                    |                    | Nellymoser         | 8khz and 16khz     |
|                    |                    |                    | mono               |
|                    |                    |                    |                    |
|                    |                    |                    | sound formats are  |
|                    |                    |                    | supported.         |
+--------------------+--------------------+--------------------+--------------------+
| F4V                | H.264              | AAC                |  N/A               |
+--------------------+--------------------+--------------------+--------------------+
| MP4                | H.264              | AAC                | Can be audio-only  |
|                    |                    |                    | (AAC) or           |
|                    |                    | MP3                | video-only.        |
+--------------------+--------------------+--------------------+--------------------+
| F4F/F4M            | H.264              | AAC                |  N/A               |
|                    |                    |                    |                    |
|                    | VP6                | MP3                |                    |
+--------------------+--------------------+--------------------+--------------------+

### What we need

-   FlowPlayer found at
    [http://mediapm.edgesuite.net/flow/](http://mediapm.edgesuite.net/flow/).
-   A .flv video.
-   A text editor.

### FlowPlayer

-   Head to the [Akamai
    FlowPlayer](http://mediapm.edgesuite.net/flow/ "http://flowplayer.org")
    website.
-   Download the Free Version of FlowPlayer
-   Save the File to your Desktop
-   Unpack the Zip File to your Desktop

The Files we need are as follows. (this was written using FlowPlayer
3.5)

-   flowplayer-(version).swf
-   flowplayer-(version).min.js
-   flowplayer.controls-(version).swf

Go Ahead and upload these to Cloud Files using the control panel.

### The Cross Domain XML file

The Cross domain XML file allows you to specify what domains are allowed
to Grab Data from the CDN. This is so people cannot hotlink your content
unless you let them. Here is an example of a simple cross domain XML
file that allows ALL domains to call these flash files

    <?xml version="1.0"?>
     <!DOCTYPE cross-domain-policy SYSTEM "http://www.adobe.com/xml/dtds/cross-domain-policy.dtd"> 
      <cross-domain-policy>
       <site-control permitted-cross-domain-policies="master-only"/>
       <allow-access-from domain="*"/>
       <allow-http-request-headers-from domain="*" headers="SOAPAction"/>
      </cross-domain-policy>

For more info on Cross domain XML files take a look at [Adobe's
Website](http://www.adobe.com/devnet/articles/crossdomain_policy_file_spec.html "http://www.adobe.com/devnet/articles/crossdomain_policy_file_spec.html")

Go ahead and save this file in your text editor as crossdomain.xml and
upload it to the same Cloud Files Container.

### The xhtml

Now we will make a simple xhtml file that will call this flash player
and embeds it onto the page here is the code.

    <html>
     <head>
      <script type="text/javascript" src="http://c022320192.cdn.cloudfiles.rackspacecloud.com/flowplayer-3.5.min.js"></script>
     </head>
     <body>
      <a
        href="http://c022320192.cdn.cloudfiles.rackspacecloud.com/video.flv"
        style="display:block;width:520px;height:330px"
        id="player">
      </a>
      <script>
       flowplayer("player","http://c022320192.cdn.cloudfiles.rackspacecloud.com/flowplayer-3.5.swf");
      </script>
     </body>
    </html>

-   On line 3 please replace
    http://c022320192.cdn.cloudfiles.rackspacecloud.com/flowplayer-3.5.min.js
    with your version of this file.
-   On line 7 please replace
    http://c022320192.cdn.cloudfiles.rackspacecloud.com/video.flv to the
    location of your video file.
-   Finally on line 12 replace
    http://c022320192.cdn.cloudfiles.rackspacecloud.com/flowplayer-3.5.swf
    with your version of this file.
-   Go grab a party hat its time to celebrate we are almost done =)

### Let's test it out

Go ahead and save this xhtml file and run it from your local machine. If
all is well you should see the flash video load up quickly and stream
away. If not double check your code. If you are still having problems
after that give our support a call or submit a ticket via the Cloud
Control Panel.  We would love to help!

