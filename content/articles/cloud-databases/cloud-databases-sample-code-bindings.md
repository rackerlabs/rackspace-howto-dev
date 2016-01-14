---
node_id: 1722
title: 'Cloud Databases: Sample Code & Bindings'
type: article
created_date: '2012-07-24 22:22:22'
created_by: Jerry Schwartz
last_modified_date: '2015-09-03 20:3141'
last_modified_by: constanze.kratel
product: Cloud Databases
body_format: tinymce
---

**Cloud Databases Code Samples**

 

**[List of API Operations](#a1)**

 

**Bindings:**The Rackspace Cloud Databases API is a RESTful API, with
support for the binding listed below:

-   [Fog Binding](https://github.com/rackspace/fog) (replaces Ruby
    Binding, which is now deprecated)

**Code Samples - PHP**

-   [Test Connection from Rackspace Cloud Sites to Rackspace Cloud
    Databases](http://c1776742.r42.cf0.rackcdn.com/downloads/code/clouddatabases.php)

** **

**Code Samples &ndash; JSON**

-   [Create Database Instance Request](#a9)
-   [Create Database Instance Response](#a10)
-   [Create Database Request](#a11)
-   [Create Database Response](#a12)
-   [Create User Request](#a13)
-   [Create User Response](#a14)

 

**[Legal Disclaimer](#a15)**

** **

 

 

**Code Samples &ndash; SDKs**

-   [Rackspace Cloud SDKs Software Developement Kit
    Guide](http://docs.rackspace.com/sdks/guide/content/intro.html)
-   [Rackspace Cloud SDK for
    Python](http://docs.rackspace.com/sdks/guide/content/python.html)

 

**List of API Operations**

o    API Versions

&sect;  List Versions

&sect;  List Version Details

o   Database Instances

&sect;  Create Database Instance

&sect;  List All Database Instances

&sect;  List Database Instance Status and Details

&sect;  Delete Database Instance

&sect;  Enable Root User

&sect;  List Root-Enabled Status

o   Database Instance Actions

&sect;  Restart Instance

&sect;  Resize the Instance

&sect;  Resize the Instance Volume

o   Databases

&sect;  Create Database

&sect;  List Databases for Instance

&sect;  Delete Database

o   Users

&sect;  Create User

&sect;  List Users in Database Instance

&sect;  Delete User

o   Flavors

&sect;  List Flavors

&sect;  List Flavor By ID<br>
<br>

 

 

** **

**Code Sample: Create Database Instance Request (JSON)**

 

POST /v1.0/1234/instances HTTP/1.1

User-Agent: python-example-client

Host: ord.databases.api.rackspacecloud.com

X-Auth-Token: d6cafa5b-e0c7-4ab8-948e-7c95f2acd031

Accept: application/json

Content-Type: application/json

 

{

    "instance": {

        "databases": [

            {

                "character\_set": "utf8",

                "collate": "utf8\_general\_ci",

                "name": "sampledb"

            },

            {

                "name": "nextround"

            }

        ],

        "flavorRef":
"https://ord.databases.api.rackspacecloud.com/v1.0/1234/flavors/1",

        "name": "json\_rack\_instance",

        "users": [

            {

                "databases": [

                    {

                        "name": "sampledb"

                    }

                ],

                "name": "demouser",

                "password": "demopassword"

            }

        ],

        "volume": {

            "size": 2

        }

    }

}

 

 

 

**Code Sample:  Create Database Instance Response (JSON)**

 

HTTP/1.1 200 OK

Content-Type: application/json

Content-Length: 636

Date: Wed, 25 Jan 2012 21:53:10 GMT

 

{

    "instance": {

        "created": "2012-01-25T21:53:09Z",

        "flavor": {

            "id": "1",

            "links": [

                {

                    "href":
"https://ord.databases.api.rackspacecloud.com/v1.0/1234/flavors/1",

                    "rel": "self"

                },

                {

                    "href":
"https://ord.databases.api.rackspacecloud.com/flavors/1",

                    "rel": "bookmark"

                }

            ]

        },

        "hostname":
"e09ad9a3f73309469cf1f43d11e79549caf9acf2.rackspaceclouddb.com",

        "id": "dea5a2f7-3ec7-4496-adab-0abb5a42d635",

        "links": [

            {

                "href":
"https://ord.databases.api.rackspacecloud.com/v1.0/1234/instances/dea5a2f7-3ec7-4496-adab-0abb5a42d635",

                "rel": "self"

            },

            {

                "href":
"https://ord.databases.api.rackspacecloud.com/instances/dea5a2f7-3ec7-4496-adab-0abb5a42d635",

                "rel": "bookmark"

            }

        ],

        "name": "json\_rack\_instance",

        "status": "BUILD",

        "updated": "2012-01-25T21:53:10Z",

        "volume": {

            "size": 2

        }

    }

}

 

 

 

**Code Sample: Create Database Request (JSON)**

** **

POST /v1.0/1234/instances/692d8418-7a8f-47f1-8060-59846c6e024f/databases
HTTP/1.1

User-Agent: python-example-client

Host: ord.databases.api.rackspacecloud.com

X-Auth-Token: 87c6033c-9ff6-405f-943e-2deb73f278b7

Accept: application/json

Content-Type: application/json

 

{

    "databases": [

        {

            "character\_set": "utf8",

            "collate": "utf8\_general\_ci",

            "name": "testingdb"

        },

        {

            "name": "sampledb"

        }

    ]

}

 

 

 

**Code Sample: Create Database Response (JSON)**

 

HTTP/1.1 202 Accepted

Content-Type: application/json

Content-Length: 0

Date: Wed, 27 Jun 2012 23:11:18 GMT

 

 

 

**Code Sample: Create User Request (JSON)**

POST /v1.0/1234/instances/1c59bdb8-03b6-4079-a7db-ba92d23a98b3/users
HTTP/1.1

User-Agent: python-example-client

Host: ord.databases.api.rackspacecloud.com

X-Auth-Token: bb64d788-2dec-4a6b-a670-7151d108cacf

Accept: application/json

Content-Type: application/json

 

{

    "users": [

        {

            "databases": [

                {

                    "name": "databaseA"

                }

            ],

            "name": "dbuser3",

            "password": "password"

        },

        {

            "databases": [

                {

                    "name": "databaseB"

                },

                {

                    "name": "databaseC"

                }

            ],

            "name": "dbuser4",

            "password": "password"

        }

    ]

}

 

 

 

**Code Sample: Create User Response (JSON)**

** **

HTTP/1.1 202 Accepted

Content-Type: application/json

Content-Length: 0

Date: Wed, 27 Jun 2012 23:11:18 GMT

 

 

** **

**Legal Disclaimer**

This information is intended for software developers who want to develop
applications by using Rackspace Cloud Databases application programming
interface (API). The information is for informational purposes only and
is provided &ldquo;as is.&rdquo;

Rackspace makes no representations or warranties of any kind, express or
implied, as to the accuracy or completeness of the contents of this
information and reserves the right to make changes to specifications and
product/services description at any time without notice. Rackspace
services offerings are subject to change without notice. Users must take
full responsibility for application of any services mentioned herein.
Except as set forth in Rackspace general terms and conditions and/or
cloud terms of service, Rackspace assumes no liability whatsoever, and
disclaims any express or implied warranty, relating to its services
including, but not limited to, the implied warranty of merchantability,
fitness for a particular purpose, and noninfringement.

 

