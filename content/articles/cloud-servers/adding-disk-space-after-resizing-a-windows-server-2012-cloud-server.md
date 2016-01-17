---
node_id: 3397
title: Adding Disk Space After Resizing a Windows Server 2012 Cloud Server
type: article
created_date: '2013-04-10'
created_by: Rackspace Support
last_modified_date: '2013-04-30'
last_modified_by: Evan Nabors
product: Cloud Servers
body_format: tinymce
---

<span
style="color: #333333; font-family: arial; line-height: 18.19444465637207px;">After
successfully resizing a Windows Cloud Server, you will need to perform
some additional steps in order to utilize the new disk space that is
available for your server. In Windows Server 2012 you can merge the
newly available disk space into one drive by expanding your original
drive. </span>** **



Contents
--------

-   [Open Computer Management](#opencomputermanagement)

<!-- -->

-   [Open Disk Management](#opendiskmanagement)

<!-- -->

-   <span style="line-height: 1.538em;">[Extend the
    Volume](#extendthevolume)</span>

<!-- -->

-   [Extend Volume Wizard](#volumewizard)

<!-- -->

-   [Select the Volume to Extend](#volumeyouwishtoextend)

<!-- -->

-   <span style="line-height: 1.538em;">[Verify Disk
    Space](#verifydiskspace)</span>

### ** ** {#section style="color: #333333; font-family: arial; line-height: normal;"}

### **[]()Open Computer Management** {#open-computer-management style="color: #333333; font-family: arial; line-height: normal;"}

From the Desktop of your Windows Server 2012 Cloud Server, open
the **Server Manager** and select **Tools** &gt; **Computer
Management**.** **

### **![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/tools_computer_manager.png){width="846" height="634"} ** {#section-1 style="color: #333333; font-family: arial; line-height: normal;"}

### **[]()Open Disk Management** {#open-disk-management style="color: #333333; font-family: arial; line-height: normal;"}

Under the **Storage** folder in the left pane, select **Disk
Management**. In the left pane of Disk Management you will see the
current formatted hard drive for your server, generally (C:), and you
should also see an amount of unallocated space in the right pane. In
this example we have a server with 40 GB of hard disk space that we have
resized to 80 GB. That expanded storage space is the unallocated 40 GB.

<span
style="font-size: 1.231em; font-weight: bold; line-height: normal;">![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/disk_managment.png){width="848"
height="635"}</span>

### []()Extend the Volume {#extend-the-volume style="color: #333333; font-family: arial; line-height: normal;"}

Select the C:\\ drive and right-click on it.  Choose **Extend
Volume** from the drop down menu.

**![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/extend_volume.png){width="849"
height="636"}**

### **[]()Extend Volume Wizard**  {#extend-volume-wizard style="color: #333333; font-family: arial; line-height: normal;"}

This will open the Extend Volume Wizard. Click **Next** to begin the
process.

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/extend_1.png){width="641"
height="519"}

### []()Select the Volume you wish to Extend {#select-the-volume-you-wish-to-extend style="color: #333333; font-family: arial; line-height: normal;"}

To add all available space to your C:\\ drive (**Disk 0**) you can keep
the default selections and press **Next**.

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/extend_2.png){width="641"
height="520"}

You will now see the C:\\ drive expand to the maximum available space.
To finalize the modifications click **Finish**.

** ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/extend_3.png){width="640"
height="519"}**

### **[]()Verify Disk Space** {#verify-disk-space style="color: #333333; font-family: arial; line-height: normal;"}

You will now see the additional disk drive volume that you created.
 Close Computer Management and begin using the additional space that you
have just created.  You can verify that the Extend process worked
correctly by loading the **Computer** **Manager **fromthe Server
Manager and checking the disk size for the C:\\ drive in **Disk
Management**.

![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/verify.png){width="850"
height="637"}

