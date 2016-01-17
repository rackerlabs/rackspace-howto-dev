---
node_id: 3392
title: Permissions Matrix for Cloud Files
type: article
created_date: '2013-04-10'
created_by: Renee Rendon
last_modified_date: '2016-01-14'
last_modified_by: Rose Contreras
product: Cloud Files
body_format: markdown_w_tinymce
---

The following matrix displays specific permissions for the roles in Cloud Files. The matrix displays the method names, their corresponding RESTful API commands, and the roles that are supported.

- [API Documentation](http://docs.rackspace.com/)
- [Related Knowledge Center Articles](/howto/)
- [Cloud Files Terminology](/howto/cloud-files-faqs)

### As of September 26, 2013

CAPABILITY:<br />Method Name | CAPABILITY:<br />API Action | ROLE:<br />Observer | ROLE:<br />Creator | DESCRIPTION
--- | --- | :---: | :---: | ---
Read Account Metadata | HEAD /account | &#9989;| &#9989; | View quick metadata on an account.
Write Account Metadata | POST /account | &nbsp; | &#9989; | Write metadata on an account.
List Containers | GET /account | &#9989; | &#9989; | View a list of containers in an account.
Create Container | PUT /account/container | &nbsp; | &#9989; | Create containers, or storage compartments, for your data.
Delete Container | DELETE /account/container | &nbsp; | &#9989; | Permanently remove a container. (The container must be empty before it can be removed.)
Read Container Metadata | HEAD /account/container | &#9989; | &#9989; | View quick metadata on a container.
Write Container metadata | POST /account/container | &nbsp; | &#9989; | Write metadata on a container.
List Objects | GET /account/container | &#9989; | &#9989; | View names and details of objects within a container.
Read Object | GET /account/container/object | &#9989; | &#9989; | Retrieve the object's data.
Create/Update Object | PUT /account/container/object | &nbsp; | &#9989; | Write or overwrite an object's content and metadata.
Copy Object | PUT /account/container/destobject | &nbsp; | &#9989; | Copy an existing object to another object in Cloud Files. (The destination container must exist before attempting the copy.)
Delete Object | DELETE /account/container/object | &nbsp; | &#9989; | Permanently remove an object from the storage system (data and metadata).
Retrieve Object Metadata | HEAD /account/container/object | &#9989; | &#9989; | Retrieve object metadata and other standard HTTP headers.
Update Object Metadata |POST /account/container/object |  &nbsp; | &#9989; | Set your own custom object metadata.


### Next: [Permission Matrix for RBAC](/howto/permissions-matrix-for-role-based-access-control-rbac)
