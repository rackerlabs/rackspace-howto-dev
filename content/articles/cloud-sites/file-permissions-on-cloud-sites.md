---
node_id: 548
title: File permissions on Cloud Sites
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-11-11 13:1503'
last_modified_by: kyle.laffoon
products: Cloud Sites
body_format: tinymce
---

undefined&rsquo;. So, the number 777,
is not literally seven hundred-seventy-seven, it is actually 7, 7, and
7, where each octal digit indicates that all three bits have been set ON
(4+2+1 = 7), thus giving full permissions to User, Group and Other.

### File creation

When a file is created, it takes its owner as the person who created the
file, and its group is the default group of the user who created the
file. The permissions are set against a mask that might specify whether
certain bits, and thus permissions, should be turned OFF by default.
Most services, such as FTP or Bash, mask OFF the world writable bit,
making it impossible to create a file that is world writable. The
Rackspace Cloud Sites FTP and  SFTP all behave in this manner. The owner
can change the permissions after file creation to anything from 000 to
777. As a result, within the Rackspace Cloud Sites environment, there is
usually no reason to give Other write permissions to any file or any
directory.

### Cloud Sites scenarios

Cloud Sites is continually working to improve security. Following are a
few special cases that you need to know about to properly secure files.

-   If you are using Cloud Sites only as a PHP solution, you can
    completely remove all Other permissions from all files and
    directories. So files could be 600 and directories could be 700.
-   When you are using multiple FTP users to manage the content of the
    site, the Group permissions must be considered. FTP users are in the
    same group as the primary account owner. Their ability to access
    files is determined through the Group permissions, and in general
    they should be set the same as the User permissions. 770 is standard
    for directories, and 660 is standard for files.
-   When you are using CGI, the CGI files must be set to Executable. So
    700 or 770 is the standard for files in the **cgi-bin** directory.
-   If you are using Cloud Sites classic ASP/.Net solution, we recommend
    that you use impersonation. Contact our Support for assistance with
    this.

The following table provides a reference for each scenario.

**Most common and recommended ACLs**

Type

Permission

User

Group

Other

Description

Directory

700

RWX

---

---

Gives only the user (owner) full permission. This is a good option if
you are not using FTP users.

File

600

RW-

---

---

Gives only the user full permissions to the file that is not a script or
a binary.

Directory

770

RWX

RWX

---

Gives the group and user full permissions. This is a good option if you
are using FTP.

File

660

RW-

RW-

---

Gives the group and user full permissions.

File

700

RWX

---

---

Gives the user full permissions and marks the file as an executable.

File

770

RWX

RWX

---

Gives the user full permissions and marks the file as executable.

Directory

755

RWX

R-X

R-X

Gives the user full permissions and allows everyone else to traverse and
list directory contents. Required when using .NET w/o impersonation.

Directory

775

RWX

RWX

R-X

Gives full read write and execute permissions to both user and group,
but limits access to read-only to all others.

File

644

RW-

R--

R--

Gives the user read and write permissions, and give reader permissions
to group read and other.

 \</

