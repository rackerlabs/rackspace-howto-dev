---
node_id: 77
title: Cloud Files - Streaming simple Flash files
type: article
created_date: '2011-03-08'
created_by: Rackspace Support
last_modified_date: '2016-01-21'
last_modified_by: Catherine Richardson
product: Cloud Files
---

This tutorial describes how to stream media files from Cloud Files to a
website. This tutorial assumes that you have a video file uploaded to
Cloud Files and that the container it is in is public. This tutorial
uses \[FlowPlayer\](http://flowplayer.org), which is an open source
Flash video player registered under the GPL. \*\*Note:\*\* We've had
some reports of problems getting the current version of FlowPlayer
(3.2.14) working with Cloud Files and are investigating. We'll update
this article when we have more information. \#\#\# Streaming Cloud
Files containers that are published and marked **public** are delivered
over the \[Akamai Technologies, Inc\](http://www.akamai.com/) global
content delivery network (CDN). For streaming flash files from your
Cloud Files, Akamai provides pseudo streaming. You can find additionl
information online, but a good explanation (in Flash) is provided at
\[http://www.longtailvideo.com/support/jw-player/28855/pseudo-streaming-in-flash/\](http://www.longtailvideo.com/support/jw-player/28855/pseudo-streaming-in-flash/).
&gt; Pseudo-streaming works as follows: When the video is initially
loaded, the player reads and stores a list of seek points as part of the
video's metadata. These seek points are offsets in the video (both in
seconds and in bytes) at which a new keyframe starts. To accomplish
this, Akamai's streaming supports the HTTP Range header to identify
those seek points. More information about the Range header is available
at http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html\#sec14.35.
Real Time Messaging Protocol (RTMP) Streaming is not supported. There is
a difference in the pseudo streaming and what Akamai offers with their
iOS streaming. iOS Streaming is a form of adaptive streaming. &gt; The
encoder (or a separate segmented process) will produce H.264/AAC content
in a sequent of small content segments, in MPEG-2 TS format (.ts). There
is also a m3u8 index file that references these segments; in the case of
live content the M3U8 is continuously updated to reflect the latest
content. More information is available at the following links: -
\[http://developer.apple.com/library/ios/\\\#technotes/tn2224/\\\_index.html\](http://developer.apple.com/library/ios/\#technotes/tn2224/\_index.html)
-
\[http://www.akamai.com/dl/akamai/iphone\\\_wp.pdf\](http://www.akamai.com/dl/akamai/iphone\_wp.pdf)
\#\#\#\# Supported formats/codecs The following formats are supported by
Akamai streaming. Container | Video Codec | Audio Codec | Comments --- |
--- | --- | --- FLV | H.263 H.264 VP6 | MP4 AAC PCM Nellymoser |
Video-only works as well. For Nellymoser, only the 8khz and 16khz mono
sound formats are supported. F4V | H.264 | AAC | None MP4 | H.264 | AAC
MP3 | Can be audio-only (AAC) or video-only. F4F/F4M | H.264 VP6 | AAC
MP3 | None \#\#\# Prerequisites - FlowPlayer found at
\[http://mediapm.edgesuite.net/flow/\](http://mediapm.edgesuite.net/flow/)
- A \*\*.flv\*\* video - A text editor \#\#\# FlowPlayer 1. Go to
the \[Akamai FlowPlayer\](http://mediapm.edgesuite.net/flow/
"http://flowplayer.org") website. 2. Download the free version of
FlowPlayer. 3. Save the file to your desktop. 4. Unpack the zip file to
your desktop. 5. Upload the following files to Cloud Files by using the
Cloud Control Panel: - \*\*flowplayer-\*version\*.swf\*\* -
\*\*flowplayer-\*version\*.min.js\*\* -
\*\*flowplayer.controls-\*version\*.swf\*\* \#\#\# The cross-domain
XML file The cross-domain XML file enables you to specify what domains
are allowed to get data from the CDN, so that people cannot hotlink your
content unless you let them. Following is an example of a simple
cross-domain XML file that allows all domains to call these Flash files:
For more information about cross-domain XML files, see \[Adobe's
website\](http://www.adobe.com/devnet/articles/crossdomain\_policy\_file\_spec.html
"http://www.adobe.com/devnet/articles/crossdomain\_policy\_file\_spec.html")
Save this file in your text editor as \*\*crossdomain.xml\*\* and upload
it to the same Cloud Files container as the previous files. \#\#\#
The XHTML Now you can create a simple XHTML file that calls this
Flash player and embeds it onto the page here. Following is the code:
<a href="http://c022320192.cdn.cloudfiles.rackspacecloud.com/video.flv" id="player"></a>
- On line 3, replace
\`http://c022320192.cdn.cloudfiles.rackspacecloud.com/flowplayer-3.5.min.js\`
with your version of this file. - On line 7, replace
\`http://c022320192.cdn.cloudfiles.rackspacecloud.com/video.flv\` with
the location of your video file. - On line 12, replace
\`http://c022320192.cdn.cloudfiles.rackspacecloud.com/flowplayer-3.5.swf\`
with your version of this file. \#\#\# Test it Save this XHTML file
and run it from your local machine. If it is working correctly, you
should see the Flash video load quickly and stream. If not, check your
code. If you are still having problems after that, call our Support team
or submit a ticket via the Cloud Control Panel.

