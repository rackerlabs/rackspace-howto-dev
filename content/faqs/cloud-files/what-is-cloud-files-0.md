---
node_id: 2185
title: What is Cloud Files?
type: frequently_asked_question
created_date: '2012-09-20 18:38:38'
created_by: tom.hopkins
last_modified_date: '2016-01-05 17:1525'
last_modified_by: rose.contreras
product: Cloud Files
body_format: full_html
---

#### Introduction

Cloud Files&trade; is an affordable, redundant, scalable, and dynamic storage
service offering. The core storage system is designed to provide a safe,
secure, automatically re-sizing and network accessible way to store
data.

You can store an unlimited quantity of files ranging in size from a few
bytes to extremely large. Users can store as much as they want and pay
only for storage space they actually use.

Cloud Files makes it easy to serve content through a CDN. This allows
users to take advantage of a proven world-class content distribution
network that is affordable and easy to use.

Cloud Files also allows users to store/retrieve files and CDN-enable
content with a simple Web Service (ReST: Representational State
Transfer) interface. There are also language-specific API&rsquo;s that utilize
the ReST API but make it much easier for developers to integrate into
their applications.

#### Ideal uses for Cloud Files {#idealusesforcloudfiles}

There are a number of uses for the Cloud Files service. Cloud Files is
an excellent storage solution for a number of scenarios and is well
suited for a number of applications such as:

-   Backing up or archiving data
-   Serving images/videos (streaming data to the user&rsquo;s browser)
-   Serving content with a world-class CDN (Akamai)
-   Storing secondary/tertiary, static web-accessible data
-   Developing new applications with data storage integration
-   Storing data when predicting storage capacity is difficult
-   Storing data for applications affordably

#### Key Concepts {#keyconcepts}

Cloud Files&trade; is not a &ldquo;file system&rdquo; in the traditional sense. You will
not be able to map or mount virtual disk drives like you can with other
forms of storage such as a SAN or NAS. Since Cloud Files is a different
way of thinking when it comes to storage, please take a few moments
to [review the
concepts](http://www.rackspace.com/knowledge_center/frequently-asked-question/cloud-files-key-concepts).

#### Using Cloud Files {#usingcloudfiles}

There are two ways to use Cloud Files:

1.  GUI interface such as the Rackspace Cloud Control Panel or
    Cyberduck.
2.  Programming interfaces via ReST, Python, PHP, Ruby, Java, or
    C\#/.NET.

#### Control Panel Interface

The Control Panel provides an browser based, intuitive, easy to use
graphical user interface. The interface allows you to manage your
Containers and Objects without any programming knowledge. From there,
users can CDN-enable the Container by marking it &ldquo;public&rdquo;. Any Objects
stored in a public, CDN-enabled Container are directly accessible over
the Akamai&rsquo;s CDN.

#### Programming Interfaces {#programminginterfaces}

There are several programming interfaces for Cloud Files that will allow
you to integrate the storage solution into your applications, or provide
automated ways of accessing the system. Currently, we support a ReST
web-services API and several programming language API&rsquo;s (Python, PHP,
Java, Ruby, and C\#/.NET).

Please refer to the Developer Guide for more details about using these
interfaces. You can access the Developer Guide on our [API documentation
site](http://docs.rackspace.com/api/).

