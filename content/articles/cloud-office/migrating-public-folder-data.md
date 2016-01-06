---
node_id: 3791
title: Migrating Public Folder Data
permalink: article/migrating-public-folder-data
type: article
created_date: '2013-11-21 13:52:54'
created_by: milton.prado
last_modified_date: '2013-11-28 18:2121'
last_modified_by: jered.heeschen
products: Cloud Office
body_format: tinymce
---

This article will provide you with instructions on migrating Public
Foder data via Outlook 2010.  The process is grouped into two sections:
 

1) Export Public Folder items to .pst    

2) Importing .pst into Public Folder

Public Folder data from your previous Exchange mailbox should be
exported to .pst format.  In order to do this, Outlook must be connected
to your source environment with appropriate permissions for the Public
Folder that you will be migrating. 

**Outlook 2010**
----------------

### **Export Public Folder Data to .pst\
**

1.Open Outlook 2010 while connected to your previous email environment.

2.Click**File \> ****Open \> Import**

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_export_pic1.png)

 

3. The first dialog of the Import and Export wizard will appear.
 Select **Export to a file \> Next**.**\
**

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_export_pic2.png)

 

4. In the next wizard dialog, Select **Outlook Data File (pst) \>
Next.**

**![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_export_pic3.png)**

 

5. The Export Outlook Data File box will appear.  *Note: To export
Public Folders, scroll down to select the public folders from the list
(see the example below)*.  Select **Include Subfolders \> Next**. 

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_export_pic4png.jpg)

 

6. Browse to the location where you would like to save the file
**\>**Click **Finish**.

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_export_pic5png.png)

 

7. A password is not required and may be left blank.  Click **OK.**

**![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_export_pic6png.png)**

 

 

### Import .pst into Public Folder 

8. Open Outlook 2010 while connected to your previous email environment.

9. Click** File \> ****Open \> Open Outlook Data File**

 ![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic7png.png)

 

10. You will not see the file listed in the Outlook folder tree.
 Please expand it and select the folder in question.

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic8png.jpg)

 

*Note: If you don't see it make sure that Folder View is enabled.*

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic9.png)

 

12. Expand the current public folders **\> All Public Folders \> Root
\#\#\# \> Domain.com.**

 ![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic10_0.jpg)

 

13. Right-click on the domain.com public folder and select **New
Folder.**

 ![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic11.jpg)

 

14. Enter the name of the folder and select the**Folder Contains** drop
down to select the folder type.

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic13.jpg)

 

15. Select all items from the .pst file (simultaneously hold CTRL and
A), drag and drop them to the Public Folder. You may also copy and paste
them if you like.

![](/knowledge_center/sites/default/files/field/image/Outlook_2010_-_import_pic12.jpg)

 

16. Allow some time for the newly imported emails to upload to the
server.  At this point the migration is complete.  Note: Based on the
way Public Folders replicate across the environment, we recommend
waiting 15-20 minutes before verifying all other users can see the data.
 

