---
node_id: 249
title: Sample Ruby Application for Cloud Files
permalink: article/sample-ruby-application-for-cloud-files
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-09-04 21:0424'
last_modified_by: kyle.laffoon
products: Cloud Files
body_format: tinymce
---

Sample Ruby Application
-----------------------

*From Connection to Objects*

In the sample command below, use your Rackspace Cloud account username
and API key, where indicated by \<username\> and \<API key\> in the
following command. For information about how to find your API key, see
[View and reset your API
key.](http://www.rackspace.com/knowledge_center/article/view-and-reset-your-api-key)

    #!/usr/bin/env ruby
    require 'rubygems'
    require 'cloudfiles'
    # Log into the Cloud Files system
    cf = CloudFiles::Connection.new('UsernameGoesHere','APIKeyGoesHere')                   
    #Create a Container
    container = cf.create_container('ContainerNameGoesHere')
    #Create an Object
    object = container.create_object('ObjectNameGoesHere')
    # Write Data to an Object
    object.write('DataGoesHere')

 

