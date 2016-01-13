---
node_id: 1296
title: Adding Disk Space After Resizing a Windows 2003 Cloud Server
type: article
created_date: '2012-03-01 20:06:59'
created_by: RackKCAdmin
last_modified_date: '2012-03-01 20:4938'
last_modified_by: test_stakeholder
products: Cloud Servers
body_format: tinymce
---

### Note:  Rackspace no longer offers Cloud Servers with Windows 2003, but these instructions are here for legacy support purposes. {.p1}

  {style="border-style: initial; border-color: initial;"}
-

Contents {style="border-style: initial; border-color: initial;"}
--------

-   [1 Windows Server 2003](#Windows%20Server%202003)
    -   [1.1 Formatting the Disk and Adding an Additional
        Drive](#Format1)
    -   [1.2 Select Partition Type](#Select2)
    -   [1.3 Specify Partition Size](#Specify3)
    -   [1.4 Assign Drive Letter](#Assign4)
    -   [1.5 Format Partition](#Format5)
    -   [1.6 Complete the New Partition Wizard](#Complete6)

 

\
**** {style="border-style: initial; border-color: initial; color: #222222; font-family: Arial, Verdana, sans-serif;"}
----

**Windows Server 2003** {style="border-style: initial; border-color: initial; color: #222222; font-family: Arial, Verdana, sans-serif;"}
-----------------------

 

###  {style="border-style: initial; border-color: initial; color: #222222; font-family: Arial, Verdana, sans-serif;"}

### Formatting the Disk and Adding an Additional Drive {style="border-style: initial; border-color: initial; color: #222222; font-family: Arial, Verdana, sans-serif;"}

-   Log into your Windows Server 2003 Cloud Server using Remote Desktop
    and logging in as the user Administrator, or with an account that is
    part of the Administrator group.

![](http://c575672.r72.cf2.rackcdn.com/RDPConnectExample.png)

-   From the Desktop of your Windows Server 2003 Cloud Server, open
    the **Start Menu** and select **Administrative Tools** \> **Computer
    Management**.

![](http://c575672.r72.cf2.rackcdn.com/Win2003AdminTools.png)

 

-   Under the **Storage** folder in the left pane, select **Disk
    Management**.  In the left pane of Disk Management you will see the
    current formatted hard drive for your server, and you should also
    see an amount of unallocated space in the right pane.  Right-click
    on the Unallocated space and choose **New Partition** from the menu.
     

![](http://c575672.r72.cf2.rackcdn.com/Win2003NewPartition.png)

-   This will open the **New Partition Wizard** screen.
     Press **Next** to begin.

![](http://c575672.r72.cf2.rackcdn.com/Win2003NewPartitionWizard.png)

****

-   **Select Partition Type** - Check the radio button next
    to **Primary partition **and click **Next. **

![](http://c575672.r72.cf2.rackcdn.com/Win2003PrimaryPartition.png)

 

****

-   **Specify Partition Size** - Next you will be asked to specify the
    partition size.  If you want to add all of your available disk space
    to one new partition, go ahead and accept the default settings and
    press **Next**.  If you only want to use a portion of your available
    disk space for the new partition, you can specify the amount of
    space to use in the **Partition size in MB** field.

![](http://c575672.r72.cf2.rackcdn.com/Win2003SpecifyPartitionSize.png)

 

****

-   **Assign Drive Letter** - Choose the drive letter for your new
    volume and click **Next**.

![](http://c575672.r72.cf2.rackcdn.com/Win2003AssignDriveLetter.png)

 

****

-   **Format Partition** - Format the partition as an NTFS partition.
     Here you can also name the partition, such as "New Volume" in this
    example.  Keep the default settings on this screen, and
    press **Next**. 

![](http://c575672.r72.cf2.rackcdn.com/Win2003FormatPartition.png)

****

-   **Complete the New Partition Wizard** - You have now successfully
    created and formatted a new partition as the destination for the
    newly available hard drive space that has been added to your Windows
    Server 2003 Cloud Server.  Press the **Finish** button to complete
    the process.

![](http://c575672.r72.cf2.rackcdn.com/Win2003CompleteNewPartWiz3.png)

-   You will now see the additional disk drive volume that you created.
     Close Computer Management and begin using the additional space that
    you have just created.

![](http://c575672.r72.cf2.rackcdn.com/Win2003driveCandD.png)

 

 {style="border-style: initial; border-color: initial; color: #222222; font-family: Arial, Verdana, sans-serif;"}


