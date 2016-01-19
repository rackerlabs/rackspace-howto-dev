---
node_id: 3851
title: Cloud Images FAQ
type: article
created_date: '2014-01-14'
created_by: Cloud Images
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Images
body_format: markdown_w_tinymce
---

<h2>Cloud Images</h2>

<h3>Where is the documentation?</h3>

<p>There are several types of documentation available:</p>

<ul>
	<li>The <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/#document-getting-started">Rackspace Cloud Images Getting Started Guide</a> walks you through the basics of using the Images API for all your image-related needs</li>
	<li>The <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/">Rackspace Cloud Images Developer Guide</a> gives you details on the Cloud Images v2 API</li>
	<li>There are links to Rackspace Knowledge Center articles giving step-by-step instructions for various Cloud Images operations at appropriate places in this document.</li>
</ul>

<h3>What is Cloud Images and how does it relate to Glance?</h3>

<p>Glance is the OpenStack image registry and storage service. Cloud Images is the product name for the initiative where we expose the Glance image service endpoints in the Rackspace open cloud.</p>

<h3>What does Cloud Images expose?</h3>

<p>Cloud Images exposes the Rackspace open cloud deployment of the OpenStack Images v2 API powered by OpenStack Glance.</p>

<h3>Why are the Glance operations being exposed?</h3>

<p>Glance features that aren't available in the Compute API or Cloud Control Panel can be accessed directly via the Cloud Images API. You already use Glance behind the scenes whenever you boot a cloud server, make an image from a server, look at a list of images, or look at detailed information for a particular image. The Cloud Images API enables direct access to those operations.</p>

<p>Exposing the Glance functions in the API also lets us add new image functionality more quickly and transparently in the future.</p>

<h3>What kind of new functionality can be accessed with the Cloud Images API?</h3>

<ul>
	<li>Image sharing</li>
	<li>Image tags</li>
	<li>More flexible image list filtering</li>
	<li>RBAC</li>
	<li>Image import</li>
	<li>Image export</li>
</ul>

<h3>Can the API return responses in XML format?</h3>

<p>The Images API returns JSON exclusively. There is no option to receive responses in XML.</p>

---------
<h2>Image Sharing</h2>

<h3>Can I share or accept images in the Control Panel?</h3>

<p>Yes! Image sharing is now available in the Cloud Control Panel. Please see the following Knowledge Center article for details: <a href="/how-to/sharing-images-in-the-cloud-control-panel">Sharing images in the Cloud Control Panel</a>.</p>

<h3>Where can I read a quick summary of image sharing?</h3>

<p>The Cloud Images API documentation has a section on <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/#image-sharing">Image Sharing</a> that will give you an overview (along with links to details).</p>

<h3>Does it cost anything to share images?</h3>

<p>There will not be a charge for sharing images. Sharing an image merely makes the image accessible/viewable to the person to whom it is shared. For example, you will be able to see the image in an API response, a client <code>image-list</code> call, or in the Cloud Control Panel. As it is not a copy of the image, the cost of storage is handled by the image producer (who is charged at normal Cloud Files rates).</p>

<h3>Is there a limit to what kinds of images, or how many, I can share or have shared with me?</h3>

<p>There is no limit on the number of images that can be shared from, or shared to, a cloud user. You can act as an image producer and share as many images as you like to other users, and you can act as an image consumer and have as many images shared with you as other people are willing to offer you.</p>

<p>If you are acting as an image producer, it's your responsibility to ensure that any images you share contain properly licensed software for which the vendor allows sharing. As a consumer, you should only use images containing properly licensed software. You are expected to follow the Rackspace <a href="http://www.rackspace.com/information/legal/aup">Acceptable Use Policy</a> with regard to the type of software included on images.</p>

<h3>Will I be charged extra for images that are shared to me?</h3>

<p>No, image charges are the responsibility of the person sharing the image. However, if you create an image of a server built from an image shared to you, that image will then be stored in your account and charged at normal Cloud Files rates.</p>

<h3>What information is required to share an image from one account to another?</h3>

<p>You need to know the DDI (customer number) of the customer with whom you want to share the image. When the customer is logged in to the Cloud Control Panel, their DDI is displayed under their account name in the upper-right of the Control Panel (it is the first item in the <strong>Account</strong> menu.</p>

<h3>Someone shared an image with me. Why don't I see it in my image list?</h3>

<p>The process of image sharing requires you to accept the share request before you will be able to see the image. To do this, you'll need to know the UUID of the image that was shared with you. Please consult the <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/#image-sharing">Cloud Images v2 API documention</a> for instructions on how to accept an image.</p>

<h3>Can I share or accept an image in the Chicago (ORD) region?</h3>

<p>If you are an image producer who wants to share an image in the ORD region of the Rackspace cloud, please be aware that the provisioning of cloud services in the ORD region has not been available to recent customers. If you share an image with such a customer, the sharing will occur without error from your perspective. If the consumer you are sharing with doesn't have cloud services in ORD, of course, they will not see the image and won't be able to boot from it. (If you don't have service in ORD, this question won't even come up, because you won't have any images in ORD to share!) A customer can tell if they don't have access to the ORD region by looking in the Control Panel — it won't show up as an option in the Region dropdown on either the Server List or Create Server pages. API users can look directly in their service catalog. To learn more about regions in the Rackspace cloud, please see the Knowledge Center article<a href="/how-to/rackspace-data-centers-and-regions"> Where are the Rackspace data centers located? </a>.</p>

<h3>What if someone shares an image to me that I don't want, or if I don't know the person?</h3>

<p>The process of image sharing requires you to accept the share request before you can see the image in your image list. This is so that other customers cannot spam you with images you're not interested in. If you don't know or trust the person sharing the image, we advise against using the image. Only create servers from images you trust.</p>

<h3>What if I accepted an image but have decided that I don't want it?</h3>

<p>You can reject the image and it will no longer be displayed in your image list. Please consult the <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/#image-sharing">Cloud Images v2 API documention</a> for instructions on how to reject an image.</p>

<h3>What happens if someone accidentally (or intentionally) shares an image with malware, root kits, backdoors, or other vulnerabilities? Who is liable?</h3>

<p>Customers are liable for any activities resulting from the use of Cloud Images. For your protection, only use images shared by people you know. If you encounter fraudulent activities, please contact Support.</p>

<h3>What happens if an image with malware, etc. is shared to me? How can I report it?</h3>

<p>You can report suspicious activities to Rackspace Support and to <a href="mailto:cloudimageshelp@rackspace.com">cloudimageshelp@rackspace.com</a>.</p>

<h3>What happens if I build a server from a shared image and then have to rebuild the server?</h3>

<p>Information necessary for a server rebuild is stored in the server record in our infrastructure. You should be able to rebuild a server even if the image has been un-shared with you or if the image owner has deleted the image. You can also create your own image from a server built using a shared image.</p>

<h3>What happens if an image is un-shared with me or if the image owner deletes the image?</h3>

<p>If an image is un-shared with you, or if the owner deletes the image, you will no longer have access to the image. If access to a particular image is important to you, create your own image of a server you've built from that image. You will be the owner of the image you created and can create new servers from that image.</p>

<h>Some images have disappeared from my Compute v2 API (nova) image list. Where did they go?</h3>

<p>Images that were manually shared by Support previous to this API release have been put in pending state. The nova client's <code>image-list</code> command originally displayed those images, but planned changes to the client will cause it to display only images in an accepted" state to match the API behavior.</p>

<p>To add those images back to your displayed images list, accept the images <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/#image-sharing">via the API</a>.</p>

<h3>Can I share an image across regions (for example, from ORD to SYD)?</h3>

<p>Image sharing can only occur within a single region of the Rackspace open cloud. For example, you cannot share an image in the ORD region in a way that allows it to be used in the SYD region. If your image is in IAD, and you share it with someone else, they will only be able to build servers from the image in the IAD region.</p>

---------
<h2>Image Tags</h2>

<h3>What are image tags?</h3>

<p>Image tags are a set of arbitrary strings you can associate with an image.</p>

<h3>What are the restrictions on image tag strings?</h3>

<p>Tag strings can include up to 255 unicode characters. In practice, however, since you might need to create, delete, or filter tags in a URL, it is best to use ASCII-range alphanumeric characters with an underscore ("_") replacing any spaces. With that approach you don't have to worry about URL-encoding tags correctly.</p>

<h3>Why would I use image tags?</h3>

<p>Image tags make it easy to group images into functional units. You can retrieve a particular group of images by using the <code>tag=&lt;tag_value&gt;</code> filter on an <code>image-list</code> call.</p>

---------
<h2>RBAC</h2>

<h3>What roles are available for Cloud Images?</h3>

<p>The standard <strong><a href="http://identityuser-admin/">identity:user-admin</a></strong>, cross-product <strong>admin</strong>, and cross-product <strong>observer</strong> are included. There are also three product-specific roles:</p>

<ul>
	<li><strong><a href="http://cloudimagesadmin/">cloudImages:admin</a></strong></li>
	<li><strong><a href="http://cloudimagescreator/">cloudImages:creator</a></strong></li>
	<li><strong><a href="http://cloudimagesobserver/">cloudImages:observer</a></strong></li>
</ul>

<h3>What are the capabilities of these roles?</h3>

<p>For details on the Cloud Image roles, see the Knowledge Center article <a href="/how-to/detailed-permissions-matrix-for-cloud-images">Detailed Permission Matrix for Cloud Images</a>.</p>

---------
<h2>Image Tasks</h2>

<h3>What are image tasks?</h3>

<p>The OpenStack Images v2 API introduces tasks as a way for users to request image operations. This provides a common task interface across all Glance installations. At the same time, since the infrastructures of OpenStack clouds can vary greatly, tasks can be customized for each particular cloud.</p>

<h3>What can I do with tasks?</h3>

<p>You can import and export images. See the Image Import and Export section in this FAQ.</p>

<h3>What RBAC roles can create tasks?</h3>

<p>You must have an <strong>Admin</strong> role to create tasks.</p>

<h3>Where can I find out more about tasks?</h3>

<p>See the <a href="https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/">Rackspace Cloud Images Developer Guide</a> for more details.</p>

---------
<h2>Image Import and Export</h2>

<h3>What is the import/export functionality?</h3>

<p>Import and export functionality lets you upload images to, and download images from your Cloud Servers account. The images can be saved server images or custom server images created by you or third parties.</p>

<h3>Is the import/export functionality something proprietary to Rackspace?</h3>

<p>No, the functionality to import and export is provided by the Glance OpenStack project API (Icehouse release). We're simply making it available to our customers.</p>

<h3>Does it cost extra to import or export images? What charges should I expect?</h3>

<p>The costs for importing, storing, and exporting images follow the same conventions as normal storage and bandwidth usage:</p>

<ul>
	<li>Uploading an image: There is no charge for inbound bandwidth. Standard rates for Cloud Files storage will apply.</li>
	<li>Downloading an image: Exported images are stored in your Cloud Files account and charged at normal Cloud Files rates. If you download the image from Cloud Files, you'll be charged for outgoing bandwidth at standard Cloud Files rates.</li>
</ul>

<h3>What formats are supported for image imports?</h3>

<p>Currently, an image must be in the <a href="http://en.wikipedia.org/wiki/VHD_(file_format)">VHD (Virtual Hard Disk) format</a> in order to be imported into the Rackspace open cloud. Being in the correct format, however, is not sufficient to guarantee a "bootable" image. The image must also follow Rackspace open cloud bootstrapping practices. For details on these practices, please see the Knowledge Center article <a href="/how-to/preparing-an-image-for-import-into-the-rackspace-opencloud">Preparing an Image for Import into the Rackspace Open Cloud</a>.</p>

<h3>Are there any limitations on the operating system installed on an image?</h3>

<p>Microsoft product use rights do not allow the use of License Mobility for Windows licenses. Given the limitations related to this software platform, image import is not available for Windows images. You may import other operating system as long as you do not violate any licensing restrictions. Please contact the vendor of any operating system you wish to import for details.</p>

<h3>Are there any limitations on the software I can import on an image?</h3>

<p>It is your responsibility to make sure that any software you place on an image to be imported is properly licensed for use in the cloud. Be aware that Microsoft licensing, in particular, is extremely restrictive. If you are in doubt, do not import any software until you have checked with the vendor.</p>

<h3>Is Rackspace responsible for the content of imported images?</h3>

<p>No, as covered in the <a href="#where-can-i-find-the-rackspace-cloud-terms-of-service">Cloud Servers Terms and Conditions</a> (and standard practice among hosting providers), Rackspace can take no responsibility for content or application licensing when it is uploaded by the customer.</p>

<h3>Are all images available for export?</h3>

<p>Certain images may not be available for export if they are using licenses or licensing schemes for which Rackspace is responsible, or has an agreement with the provider. The export task will go into an error state with a message indicating that the image cannot be exported.</p>

<p>It's important to note that when you export an image using Cloud Images, your image does not leave the Rackspace open cloud. It is deposited in your Cloud Files account so that you may have a personal copy of the image. Why is this important? This process lets you have a copy of your image without in any way distributing the image (or any software contained therein) outside of the Rackspace open cloud. This is an important distinction for some licensing agreements.</p>

<p>As described in the <a href="https://www.rackspace.com/information/legal/cloud/tos">Rackspace Cloud Terms of Service</a>, you are responsible for understanding licensing terms regarding all software contained in any image you export. Do not distribute your image outside the Rackspace open cloud unless you're certain that all relevant licenses allow you to do so. You may need to obtain and apply your own licenses in order to use an image outside the Rackspace open cloud, depending on the software licenses involved. Please contact the appropriate software vendor if you have questions.</p>

<h3>How can I tell if an image can be exported?</h3>

<p>First, only the image owner can export an image. You cannot export a Rackspace public image and you cannot export an image that has been shared with you. <strong>Note:</strong> If you have a use case where you really want to export one of these, you can create a server from that image then make an image of the new server to get your own copy of the original image.</p>

<p>Next, some images are not available for export due to licensing or billing issues. Currently, these include all Windows and Red Hat images. You can tell for sure by looking at the image you want to export. It will have a property named <code>com.rackspace__1__options</code>. If the value is zero, you may export the image.</p>

<h3>Can you give me step-by-step instructions for exporting an image?</h3>

<p>You can find a detailed example of exporting an image in the first half of the article&nbsp;<a href="/how-to/transferring-images-between-regions-of-the-rackspace-open-cloud">Transferring images between regions of the Rackspace Open Cloud</a>.</p>

<h3>Where is my exported image?</h3>

<p>Your image is exported into a container you specify in your cloud files account. It's stored as a "Dynamic Large Object" in Cloud Files. What this means is that your image is actually stored as a series of "segments" along with a "manifest object". In order to download the image, what you'll want to download is the "manifest object". Cloud Files will stream all the segments in the correct order. Here's a screenshot so you can see what this looks like in the Cloud Control Panel:</p>

<p><img alt="Screenshot of the contents of a Cloud Files container illustrating a Dynamic Large Object and its segments" border="1" height="337" src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/file-listing_0.png" width="632" /></p>

<p>In the screenshot, the "manifest objects" are contained in red boxes. Note that each one is zero bytes in size and has a filename of the form <code>{image_uuid}.vhd</code>. The other objects in the screenshot (the ones whose names end with <code>-00001</code>, <code>-00002</code>, etc. are the "segments". <em>It is extremely important that you do not delete any of the segments unless you also intend to delete the entire image</em>. If you delete a single segment and then download the "manifest object", the download will succeed, but your image will be corrupt (since part of it will be missing).</p>

<p>To summarize: to download your image, you want to download the Cloud Files object whose name follows the format <code>{image_uuid}.vhd</code>. (We do not, however, suggest that you attempt to download an object the size of a typical VM image through the Cloud Control Panel.)</p>

<h3>Can you recommend a way for me to download my exported image from Cloud Files?</h3>

<p>We recommend using the <strong>Swiftly</strong> Cloud Files client. Please read <a href="/how-to/use-swiftly-to-download-an-exported-image">Use Swiftly to Download an Exported Image</a>.</p>

<h3>If I have cloud servers in multiple regions, will an imported image be available in all regions?</h3>

<p>An imported image is only available in the region into which it has been imported. If you want the image in multiple regions, you'll have to transfer it from your Cloud Files account in region A to your Cloud Files account in region B, and then use the Cloud Images endpoint for region B to import the image into region B.</p>

<p>We're working on building an "image cloning" functionality that will allow you to move images directly from region to region without having to perform the intermediate Cloud Files transfer and image import in each region.</p>

<h3>How do I transfer an image to another region?</h3>

<p>See the Knowledge Center article <a href="/how-to/transferring-images-between-regions-of-the-rackspace-open-cloud">Transferring Images Between Regions of the Rackspace Open Cloud</a>.</p>

<h3>Can I use image export and import to move between Infrastructure and Managed accounts?</h3>

<p>Yes, it is possible to now move images between Infrastructure and Managed accounts by following the steps in the article <a href="/how-to/transferring-images-between-regions-of-the-rackspace-open-cloud">Transferring Images Between Regions of the Rackspace Open Cloud</a> to export the required image, then import it into whatever account the customer requires. Any images that are shared, imported, or exported are deemed to be non-standard, therefore the <em>Infrastructure</em> service level will be applied regardless of the type of account the image is being shared with or imported into. Back-up configurations and monitoring checks are applied uniquely to each Cloud instance and therefore will need to be recreated upon successful import or share.</p>

<h3>How do I prepare an image for import?</h3>

<p>See the Knowledge Center article <a href="/how-to/preparing-an-image-for-import-into-the-rackspace-opencloud">Preparing an Image for Import into the Rackspace Open Cloud</a>.</p>

<h3>Can you recommend a way to upload my image to Cloud Files so it can be imported?</h3>

<p>We recommend using the <strong>swiftly</strong> Cloud Files client. Please see this Knowledge Center article: <a href="/how-to/use-swiftly-to-upload-an-image">Using Swiftly to upload an image to be imported</a>.</p>

<h3>Can you give me step-by-step instructions for importing an image?</h3>

<p>You can find a detailed example of importing an image in the second half of the article&nbsp;<a href="/how-to/transferring-images-between-regions-of-the-rackspace-open-cloud">Transferring images between regions of the Rackspace Open Cloud</a>.</p>

<h3>What's the deal with the checksum on my imported (or exported) image?</h3>

<p>Customers who are really, really careful with their data may have this question: When I look at my image in the Images (or Compute) API, I see that its checksum is 12345. But when I export my image and download it from Cloud Files, its checksum is 98765. (Or: I've prepared my own image outside the Rackspace cloud. It's got checksum 98765, but when I look at the imported image in the API, it says that the image checksum is 12345.) What's up with that?</p>

<p>The difference is that images are stored internally in the public cloud in a different format from the way they're transferred.</p>

<p>On the input side, the VHD format image is packaged as a gzipped OVA so that it's in the format the hypervisor expects to see. Therefore, the checksum will be different.</p>

<p>On the export side, to keep server image creation fast, the hypervisor stores a server "snapshot" as an OVA containing multiple VHD files. When we export the image, we coalesce these multiple VHDs into a single VHD. So the checksums again will be completely different between what's in the cloud and what's exported.</p>

<p>One other thing: during the coalesce operation that happens on export, some information is updated in the headers and footers of the VHD. So even if you have a VHD with checksum 56789 and you import it and then immediately export the imported image, the checksum of the VHD that's exported will be different (although the "content" of the VHD, i.e., the non-header and non-footer part, will be identical).</p>

<h3>I want to boot a server from my imported image, but I can't find the image in the Cloud Control Panel. Where is it?</h3>

<p>On the Create Server page in the Control Panel, you see a list of images you can choose from. The Cloud Control Panel sorts your images according to what server they're a snapshot of, but because your image is an import, it's not a snapshot of any existing server in the Cloud. Thus, the Control Panel considers this is a snapshot of a deleted server. Your imported image is listed under the <strong>Deleted Servers</strong> category.</p>

---------
<h2>Image Metadata and Property Protection</h2>

<h3>What's the difference between "image metadata" and "image properties"?</h3>

<p>The Compute API talks about "image metadata", while the Images v2 API uses the terminology "image properties". These refer to the same thing.</p>

<h3>Why are some image properties protected?</h3>

<p>There are some image properties that Rackspace puts on images for the purposes of determining licensing, billing, and VM configuration. These are inherited by snapshots of servers booted from these images and may not be modified by customers.</p>

<h3>Does protection affect image metadata calls in the Compute v2 API?</h3>

<p>The Compute (nova) API acts as a proxy for Glance, so property protections apply to all image metadata operations performed via the Compute v2 API.</p>

<h3>What happens if I try to modify a protected property?</h3>

<p>You'll get a 403 (Forbidden) response to your API request. The response will contain an error message to the effect that you're trying to modify a property that you don't have permission to modify.</p>

<h3>How do I know what properties are protected?</h3>

<p>Most of the properties that appear on an image by default, before you have added any custom properties, are protected. An exception is "name", which you may change at any time. You aren't allowed to create any new properties with the prefix "com.rackspace" (we use that prefix to indicate Rackspace properties). The simplest way to determine this is to try to modify a property. If you aren't allowed to modify it, you'll get a 403 (Forbidden) response.</p>

<h3>I'm creating sub-users on my account and assigning them RBAC roles. Which roles can modify image properties?</h3>

<p>A user must have a customer-admin role (like identity:user-admin, admin, or cloudImages:admin) in order to modify image properties.</p>

<h3>Which roles can create image properties?</h3>

<p>A user must have a customer-admin role to create image properties. Because of the way the Images v2 API works, any user that can create image properties can also modify and delete image properties. Those privileges exceed the capabilities that should properly be assigned to a "creator" role, so we restrict image property creation to users with a customer-admin role.</p>

---------
<h2>Image Support</h2>

<h3>Where can I find the Rackspace Cloud Terms of Service?</h3>

<ul>
	<li>For the UK cloud: <a href="http://www.rackspace.co.uk/legal/cloud-terms-of-service">http://www.rackspace.co.uk/legal/cloud-terms-of-service</a></li>
	<li>For the US cloud: <a href="http://www.rackspace.com/information/legal/cloud/tos">http://www.rackspace.com/information/legal/cloud/tos</a></li>
</ul>

<p>The Terms of Service incorporate the Rackspace Acceptable Use Policy. You can find links to the appropriate AUP document for your region from the TOS pages at the above URLs.</p>

<h3>What kind of support can I expect for imported and shared images?</h3>

<p>Imported and shared images are considered to be non-standard images, read the&nbsp;article <a href="/how-to/rackspace-standard-and-non-standard-images">Standard and Non-Standard Images</a>. For servers booted from non-standard images, you may expect that we will ensure host servers are functioning properly and that the API availability meets the SLA. We will also provide advice on sharing, importing, and exporting images.</p>

<h3>I'm a managed cloud customer—do I still only get infrastructure level support for servers built from non-standard images?</h3>

<p>Our managed cloud support team wants to create amazing customer outcomes, so when you build a server from a non-standard image, your support representative will do what he or she can to troubleshoot and provide guidance. Because the technologies contained in a non-standard image are not always popular or well documented, technical support for those technologies is not guaranteed and may vary by support representative. Any assistance provided in response to a support request for a server built from a non-standard image is not an agreement of continuing support, and future requests will be handled on a case-by-case basis. When you consider deploying a server built from a non-standard image as part of your infrastructure, please keep in mind that if you incur downtime or a degraded state due to problems with the image or any technology contained therein, it will not be covered by the standard Cloud Servers SLA.</p>

<h3>I've got a question that's not listed here. How can I get an answer?</h3>

<p>For additional questions, either contact Support or send an email to <a href="mailto:cloudimageshelp@rackspace.com">cloudimageshelp@rackspace.com</a>.</p>
