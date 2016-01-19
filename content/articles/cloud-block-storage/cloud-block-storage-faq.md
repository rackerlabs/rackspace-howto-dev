---
node_id: 5022
title: Cloud Block Storage - FAQ
type: article
created_date: '2015-12-10'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Block Storage
body_format: markdown_w_tinymce
---

<h2>Backups</h2>

<h3>What are the minimum / maximum limits for single Cloud Block Storage volumes?</h3>

<p>The minimum size for a Cloud Block Storage volume is 50 GB for an SSD volume or 75 GB for an SATA volume. The maximum volume size is 1 TB.</p>

<h3>What's the maximum number of Cloud Block Storage volumes I can attach to a single server instance?</h3>

<p>Depending on your Cloud Server’s operating system, you can have up to a maximum of 14 Cloud Block Storage volumes attached to a single server.</p>

<h3>What is the default maximum capacity of Cloud Block Storage that can be consumed by a single customer account?</h3>

<p>The limit for Volumes and storage is 10 TB total stored or 50 volumes per region (whichever is reached first).</p>

<h3>What if I need more storage than the default maximum capacity?</h3>

<p>No problem. We'll be happy to accommodate any size storage requests for Cloud Block Storage. Simply ask for an increase to your storage quota via a support request and include the desired storage amount (TBs or volume count), storage type (SATA or SSD), and region (DFW, ORD, IAD, LON, SYD, HKG). Please contact your account team for further details.</p>

<h3>Does Cloud Block Storage have a Service Level Agreement (or SLA)?</h3>

<p>Yes. Details regarding the Cloud Block Storage SLA can be found here: <a href="http://www.rackspace.com/cloud/legal/sla/">http://www.rackspace.com/cloud/legal/sla</a>.</p>

<h3>Is Cloud Block Storage right for me?</h3>

<p>Cloud Block Storage is an excellent option for you if you:</p>

<ul>
	<li>Want more control over your storage or application infrastructure</li>
	<li>Are looking for a high performance storage option (SSD)</li>
	<li>Would like to add additional storage to your servers without paying for additional compute resources</li>
</ul>

<p>You might not be a good fit for the Cloud Block Storage service if you:</p>

<ul>
	<li>Are leveraging First Generation Cloud Servers</li>
	<li>Are not comfortable with low-level system administration tasks, such as installing file systems, mounting and partitioning storage volumes, or installing your own applications on top of a raw storage device</li>
	<li>Are looking for a fully managed storage or database solution</li>
</ul>

<h3>Is Cloud Block Storage a replacement for existing Rackspace storage products?</h3>

<p>Cloud Block Storage (CBS) is not meant as a direct replacement of any existing Rackspace products (shared or dedicated). CBS allows Rackspace Cloud customers to add “a la carte” storage to their existing next generation Cloud Servers and should be considered a complementary cloud-based storage offering that rounds out our entire storage portfolio.</p>

<h3>What parts of the storage system are highly available (HA)?</h3>

<p>Cloud Block Storage back-end storage volumes employ a RAID (Redundant Array of Independent Disks) level 10 configuration. RAID 10 provides high availability by combining features of RAID level 0 and RAID level 1 in which data is stripped and mirrored to provide a very high level of reliability and performance.</p>

<h3>If the system employs RAID level 10 on the back end storage nodes, can I assume my volumes are fully protected from a failure scenario?</h3>

<p>The hardware RAID level 10 employed by Cloud Block Storage nodes provides protection against disk failures on the storage nodes themselves. However customers are strongly encouraged to implement a RAID level 1 (mirror) configuration across multiple volumes to protect against data loss in the event of a storage node failure.</p>

<h3>Can I attach a single volume to multiple Cloud Servers?</h3>

<p>Not concurrently. Cloud Block Storage is not a shared storage offering. You may attach multiple volumes to a single Cloud Server instance, but you may not attach multiple Cloud Servers to a single Cloud Block Storage volume.</p>

<h3>Once I have created a Cloud Block Storage volume, can it be resized (increased or decreased)?</h3>

<p>Once you have created a volume, you can increase its size using the API by either of two methods:</p>

<ul>
	<li>Cloning from a source volume to a new larger volume, or</li>
	<li>Creating a new larger volume from an existing volume snapshot.</li>
</ul>

<p>Alternatively, in order to move to a larger or smaller volume size, you might need to create a new volume of the desired size and then copy your data from the original volume to the new volume. Please note that you will be required to resize your file system when moving to a smaller volume (if supported by your operating system).</p>

<p>When you copy your data within the same data center via the internal ServiceNet network, there is no charge for bandwidth.</p>

<h3>Can a Cloud Block Storage volume be mounted to a first-generation Cloud Server or a Dedicated Server?</h3>

<p>No. Cloud Block Storage volumes are available to newer Cloud Servers platforms, but not first-generation Cloud Servers.</p>

<h3>When I am using a volume, how can I know how much space I have left?</h3>

<p>You can verify a volume’s capacity and available space using basic system commands available via their Cloud Server operating system:</p>

<ul>
	<li>In Linux CLI: From a terminal window, run the “df -h” command and note the Size, Used, Avail, and Capacity of the storage volume</li>
	<li>Windows Explorer: Right-click on drive icon and select "Properties," and note Capacity, Free space, and Used space</li>
</ul>

<h3>Is there a limit to the number, frequency or size of snapshots that can be taken on a volume?</h3>

<p>There is no limit. You may create an unlimited number of Snapshots.</p>

<h3>Can I utilize a software RAID to improve the I/O performance of my SATA Cloud Block Storage volumes?</h3>

<p>Yes. However at some point the cost benefit of utilizing multiple less expensive SATA volumes in a RAID configuration will be outweighed by the benefit of utilizing a single higher I/O SSD volume. If you want to increase the I/O performance of your storage volumes, we encourage you to use higher performing SSD volumes for increased disk I/O.</p>

<h3>How much does Cloud Block Storage cost?</h3>

<p>Cloud Block Storage is charged by gigabytes of storage used per month, not the IOPs, which can be difficult to predict. The price differs for standard volumes, SSD volumes, and snapshots.</p>

<p>Prices vary by region and are detailed on the following pages:</p>

<ul>
	<li><a href="http://www.rackspace.com/cloud/block-storage/pricing/">USA Pricing for Cloud Block Storage (DFW, ORD, and IAD regions)</a></li>
	<li><a href="http://www.rackspace.co.uk/cloud/block-storage/pricing">UK Pricing for Cloud Block Storage (LON region)</a></li>
	<li><a href="http://www.rackspace.com.au/cloud/block-storage/pricing">Australia Pricing for Cloud Block Storage (SYD region)</a></li>
	<li><a href="http://www.rackspace.com.hk/cloud/block-storage/pricing">Hong Kong Pricing for Cloud Block Storage (HKG region)</a></li>
</ul>

<h3>How Is Volume Cloning Different from Volume Snapshotting?</h3>

<p>A volume <em>clone</em> is a usable copy of the source volume; it can be attached to a server and used immediately. A volume <em>snapshot</em> cannot be directly used as a volume; you must create a volume from the snapshot and then attach that volume to your server. Snapshots are stored redundantly in Cloud Files. However, creating a volume from a snapshot is a slower process than creating a volume from a clone. If your application is time sensitive, consider using volume cloning.</p>

<p>For instructions on volume cloning, see <a href="/how-to/create-a-clone-of-a-cloud-block-storage-volume"> How to Create a Clone of a Cloud Block Storage Volume</a>.</p>

<h3>What can I do if I need to change volume types (SATA vs. SSD)?</h3>

<p>Although you cannot change the type of a Cloud Block Storage volume after it has been provisioned, you can create a copy of that volume and switch volume types by using the cloning or snapshot method outlined in the following articles:</p>

<ul>
	<li><a href="/how-to/create-a-clone-of-a-cloud-block-storage-volume">How to Create a Clone of a Cloud Block Storage Volume </a> .</li>
	<li><a href="/how-to/create-and-use-cloud-block-storage-snapshots">Create and Use Cloud Block Storage Snapshots </a></li>
</ul>

<h3>How can I make a copy of a Cloud Block Storage volume?</h3>

<p>You can create a copy of a Cloud Block Storage volume using two methods:</p>

<ul>
	<li><strong>Cloning Method</strong> (Volume-to-volume)</li>
</ul>

<p>This is direct copy from your existing volume to a new blank volume on another storage node. Volume data is copied directly between CBS storage nodes over our high-speed local storage network. This method is recommended if you want to make quick copies of your volume data and use them immediately after creation.</p>

<ul>
	<li><strong>Snapshot Method</strong> (Volume-to-Snapshot-to-Volume)</li>
</ul>

<p>This method requires the intermediate step of creating a volume snapshot. You first create snapshot from your existing volume, which gets stored in Cloud Files. Second, you create a new volume using your snapshot as the source. This process requires writing snapshot data in and out of Cloud Files so it can take longer than the Cloning Method. This method is recommended if you don’t require quick access to your copied volumes and want the added durability, and lower price, of having your volume snapshot stored in Cloud Files.</p>

<h3>Can I rename my volumes once they are created?</h3>

<p>Yes. Using the API, you can rename an existing volume using the cinder rename command to update the display-name of the volume.</p>

<h3>My snapshot seems to be taking a long time. Is it possible to check the status of a snapshot?</h3>

<p>Yes. Using the API, you can query the progress of a snapshot creation using the snapshot-show command.<br />
The percentage complete value will show up under the os-extended-snapshot-attributes:progress property.</p>

<h3>Can I use Cloud Backup to backup my Cloud Block Storage Volumes?</h3>

<p>Yes, you can. After you have attached and mounted your Cloud Block Storage Volume, you can add it to your current Cloud Backup Schedule. Edit the Backup Schedule and browse to the drive letter of your Volume or to individual files on the drive. Save your Schedule as normal.</p>

<h3>What is Rackspace Cloud Block Storage?</h3>

<p>Rackspace Cloud Block Storage provides persistent block-level storage volumes for use with Rackspace next generation Cloud Servers. Volumes can be created and deleted independently of the Cloud Servers they are attached to. Rackspace Cloud Block Storage customers can create volumes ranging from 50 GB for an SSD volume or 75 GB for a SATA volume up to 1 TB in size.</p>

<h3>How does Cloud Block Storage differ from the local storage available through Cloud Servers?</h3>

<p>Cloud Block Storage provides persistent data storage for next generation Cloud Servers. Persistent storage can exist independent of your server, even after the server has been deleted. The local storage bundled with Cloud Servers is ephemeral and exists only as long as the Cloud Server exists. When the server is deleted, so is its local storage.</p>

<p>We recommend that you <a href="/how-to/detach-and-delete-cloud-block-storage-volumes">unmount and detach Cloud Block Storage</a> volumes before deleting the server.</p>

---------
<h2>Security</h2>

<h3>What happens to my data when I delete a Cloud Block Storage volume?</h3>

<p>For your security, the used portions of the physical disk are overwritten with zeroes before the deleted volume's disk space is reallocated to the shared pool of disk resources. At this point, your data cannot be recovered and is not visible to other customers.</p>
