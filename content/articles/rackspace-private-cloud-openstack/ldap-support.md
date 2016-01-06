---
node_id: 3313
title: Rackspace Private Cloud Active Directory and LDAP Integration
permalink: article/ldap-support
type: article
created_date: '2013-03-04 17:28:32'
created_by: Karin Levenstein
last_modified_date: '2014-10-30 18:3113'
last_modified_by: jered.heeschen
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

**NOTE**: These instructions apply only to Rackspace Private Cloud v4,
deployed with Chef.

* * * * *

 

This article describes the processes for enabling [Active
Directory](#active-directory) and [LDAP](#rackspace-private-cloud-ldap)
in your Rackspace Private Cloud environment.

**Table of Contents**

[Overview](#overview)

[Intended audience](#overview-audience)

[Document change history](#overview-dochistory)

[Additional resources](#overview-resources)

[Contact Rackspace](#contact-rackspace)

[Prerequisites](#ad-ldapprereqs)

[Active Directory prerequisites](#prereqs-activedirectory)

[LDAP prerequisites](#prereqs-ldap)

[Required information](#ad-ldap-requiredinfo)

[Active Directory required information](#active-directory-requiredinfo)

[LDAP required information](#ldap-required-info)

[Adding Active Directory/LDAP integration for OpenStack
Havana](#ad-ldap-howto-havana)

[Prerequisites for Active Directory/LDAP in OpenStack
Havana](#ad-ldap-prereqs-havana)

[Adding Active Directory/LDAP](#ad-ldap-howto-havana-new)

[Using replicated Active Directory/LDAP controllers across multiple
environments](#ad-ldap-howto-multiple-rpcs-havana)

[Adding Active Directory/LDAP integration for OpenStack
Grizzly](#ad-ldap-howto-grizzly)

Overview {.title}
--------

Rackspace has developed a fast, no-charge, and easy way to deploy a
Rackspace Private Cloud powered by OpenStack in any data center. This
method is suitable for anyone who wants to install a stable, tested, and
supportable OpenStack private cloud, and can be used for all scenarios
from initial evaluations to production deployments. Two versions are
available:

-   Rackspace Private Cloud v4.2.2 is based on the [OpenStack
    Havana](http://www.openstack.org/software/havana/) code base,

-   Rackspace Private Cloud v4.1.3 is based on the [OpenStack
    Grizzly](http://www.openstack.org/software/grizzly/) code base.

### Intended audience {.title style="clear: both;"}

This document provides an overview of how to use the Rackspace Private
Cloud cookbooks to connect OpenStack Identity to an existing Active
Directory/LDAP authentication system for single sign on. It also
provides an example of Chef environments that have been tested to
achieve integration for each authentication service.

The scope of this document does **not** include the administration or
configuration of an Active Directory service, except insofar as is
required to achieve integration. It is also important to point out that
this is only currently applicable to authentication. Authorization is
not discussed in this document.

To use the product and this document, you should have prior knowledge of
OpenStack and cloud computing, and basic Linux administration skills.

### Document change history {.title style="clear: both;"}

This version of Rackspace Private Cloud Active Directory Integration
replaces and obsoletes all previous versions. The most recent changes
are described in the table below:

Revision Date

Summary of Changes

March 17, 2014

-   Rackspace Private Cloud v4.2.2 General Availability release.

February 2014

-   Updates for v4.2.2/OpenStack Havana

June 25, 2013

-   Release of Rackspace Private Cloud v. 4.0

### Additional resources {.title style="clear: both;"}

-   [Rackspace Private Cloud Knowledge
    Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud)

-   [OpenStack Manuals](http://docs.openstack.org)

-   [OpenStack API Reference](http://api.openstack.org)

-   [OpenStack - Keystone Developer
    Documentation](http://docs.openstack.org/developer/keystone)

### Contact Rackspace {.title style="clear: both;"}

For more information about sales and support, send an email to
[`<`{.email}](mailto:opencloudinfo@rackspace.com)[opencloudinfo@rackspace.com](mailto:opencloudinfo@rackspace.com)[`>`{.email}](mailto:opencloudinfo@rackspace.com).

If you have feedback about the product and the documentation, send and
email to
[`<`{.email}](mailto:RPCFeedback@rackspace.com)[RPCFeedback@rackspace.com](mailto:RPCFeedback@rackspace.com)[`>`{.email}](mailto:RPCFeedback@rackspace.com).
For the documentation, you can also leave a comment at [the Knowledge
Center](http://www.rackspace.com/knowledge_center/product-page/rackspace-private-cloud).

For more troubleshooting information and user discussion, you can also
inquire at the Rackspace Private Cloud Support Forum at
[`https://community.rackspace.com/products/f/45`{.uri}](https://community.rackspace.com/products/f/45)

Prerequisites {.title}
-------------

To use these instructions, you should have an understanding of OpenStack
Identity (Keystone) core concepts, including users, roles, tenants, and
tokens, and a working knowledge of Active Directory and LDAP.

### Active Directory prerequisites {.title style="clear: both;"}

Your environment must have the following features already configured:

-   A working Active Directory server.

-   The address, hostname, or URL of the Active Directory server, such
    as `activeserver.example.com`{.uri}.

-   A configured user with enough privileges to search all of the
    organizational units that are defined within the environment, such
    as `Administrator`{.filename}.

You may have existing users and groups already defined, but this is not
required.

### LDAP prerequisites {.title style="clear: both;"}

Your LDAP environment must have the following features already
configured:

-   A working LDAP server with OpenLDAP or 389 Directory Server
    installed. The top level organization should already be created, as
    in the following example:

    ~~~~ {.screen}
     dn: cn=example,cn=com
     dc: example
     objectClass: dcObject
     objectClass: organizationalUnit
     o: example.com
                                
    ~~~~

-   The address, hostname, or URL of the LDAP server, such as
    `ldapserver.example.com`{.uri}.

-   A configured user with enough privileges to search all of the
    organization units that are defined within the environment, as in
    the following example:

    ~~~~ {.screen}
    cn=admin,dc=example,dc=com 
                                
    ~~~~

You may have existing users and groups already defined, but this is not
required.

Required information {.title}
--------------------

The Chef cookbooks for the Keystone service have been made intentionally
flexible for this type of deployment, and does not enforce any defaults
except the most basic default Keystone configuration. This design
ensures that a user can integrate Keystone without modifying any
existing LDAP schema. You must understand Active Directory and your
underlying LDAP schema to correctly integrate the Keystone service.

### Active Directory required information {.title style="clear: both;"}

The example in this section is based on a clean Active Directory
installation.

Before you begin, you must make `groupOfNames`{.filename} a superior for
`organizationalRole`{.filename}. This enables Keystone roles to work
correctly with Active Directory.

**Procedure 3.1. To configure groupOfNames**

1.  In the Active Directory schema master, use ASDI Edit and select
    `schema`{.filename}.

2.  Open `CN=Organizational-Role`{.filename}.

3.  In the attribute editor, select `possSuperiors`{.filename}.

4.  Add `groupOfNames`{.filename} to the list of values and click OK to
    save the change.

After completing this task, you can proceed with collecting the required
information about your Active Directory configuration with Active
Directory Users and Computers.

**Procedure 3.2. To identify Active Directory configuration
information**

1.  Locate the Organizational Unit (OU) that contains Users. You will
    use this information to configure the lookup point for users in
    Keystone. Because Active Directory identifies the Users OU
    differently than LDAP does, you will search for the Common Name
    (CN).

    In the following example, the OU is called `Users`{.filename}.

    ~~~~ {.screen}
    CN=Users,dc=example,dc=com
                                    
    ~~~~

2.  Locate the OU that contains Groups. You will use this information to
    configure the lookup point for tenants in Keystone.

    In the following example, the OU is called `Tenants`{.filename}.

    ~~~~ {.screen}
    OU=Tenants,dc=example,dc=com
                                    
    ~~~~

3.  Locate the OU that contains Roles. If one does not already exist,
    the AD administrator should create a Roles OU. You will use this
    information in Keystone to set up roles and manage user/tenant
    interaction within the OpenStack cluster.

    In the following example, the OU is called `Roles`{.filename}.

    ~~~~ {.screen}
    OU=Roles,dc=example,dc=com
                                
    ~~~~

4.  **Note**: If you are using Keystone 2013.1.1, you may skip this
    step.

    The LDAP administrator will need to create an OU called
    `Domains`{.filename} and a single object named `Default`{.filename}
    that has the objectClass `groupOfNames`{.filename}.

5.  Identify the objectClass that will be used by objects in the User,
    Group, Role, and Domain OUs. The objectClass will depend on your own
    LDAP schema.

    In this example, the following objectClass definitions are used:

    ~~~~ {.screen}
    User: person
    Group: groupOfNames
    Role: organizationalRole
    Domain: Group
                                
    ~~~~

### LDAP required information {.title style="clear: both;"}

The example in this section is based on a default deployment of OpenLDAP
that contains the following enabled OpenLDAP `.ldif`{.filename} files:

-   `core.ldif`{.filename}

-   `cosine.ldif`{.filename}

-   `nis.ldif`{.filename}

-   `inetorgperson.ldif`{.filename}

Follow this process to gather the information required to add LDAP to
your Chef environment.

**Procedure 3.3. To identify LDAP configuration information**

1.  Identify the Organizational Unit (OU) that contains Users. You will
    use this information to configure the lookup point for users in
    Keystone.

    In the following example, the OU is called `users`{.filename}.

    ~~~~ {.screen}
    ldapsearch -x -LLL -H ldapi:/// -b dc=example,dc=com "(objectClass=organizationalUnit)"
    dn: ou=Users,dc=example,dc=com
    objectClass: organizationalUnit
    ou: users
                                    
    ~~~~

2.  Identify the OU that contains Groups. You will use this information
    to configure the lookup point for tenants in Keystone.

    In the following example, the OU is called `groups`{.filename}.

    ~~~~ {.screen}
    ldapsearch -x -LLL -H ldapi:/// -b dc=example,dc=com "(objectClass=organizationalUnit)"
    dn: ou=Groups,dc=example,dc=com
    objectClass: organizationalUnit
    ou: groups
                                    
    ~~~~

3.  Identify the OU that contains Roles. If one does not already exist,
    the LDAP administrator should create a Roles OU. You will use this
    information in Keystone to set up roles and manage user/tenant
    interaction within the OpenStack cluster.

    In the following example, the OU is called `roles`{.filename}.

    ~~~~ {.screen}
    ldapsearch -x -LLL -H ldapi:/// -b dc=example,dc=com "(objectClass=organizationalUnit)
    dn: ou=Roles,dc=example,dc=com
    objectClass: organizationalUnit
    ou: roles   
                                
    ~~~~

4.  **Note**: If you are using Keystone 2013.1.1, you may skip this
    step.

    The LDAP administrator will need to create an OU called
    `domains`{.filename} and a single object named `Default`{.filename}
    that has the objectClass `groupOfNames`{.filename}.

5.  Identify the objectClass that will be used by objects in the User,
    Group, Role, and Domain OUs. The objectClass will depend on your own
    LDAP schema.

    In this example, the following objectClass definitions are used:

    ~~~~ {.screen}
    User: inetOrgPerson
    Group: groupOfNames
    Role: organizationalRole
    Domain: groupOfNames
                                
    ~~~~

Adding Active Directory/LDAP integration for OpenStack Havana {.title}
-------------------------------------------------------------

The instructions in this section apply to Active Directory
implementations in Private Clouds that are running OpenStack Havana
(Rackspace Private Cloud v4.2.2).

If you are running OpenStack Grizzly (Rackspace Private Cloud v4.1.n),
refer to Adding Active Directory integration to the Chef environment
(OpenStack Grizzly).

### Prerequisites for Active Directory/LDAP in OpenStack Havana {.title style="clear: both;"}

In Rackspace Private Cloud v4.2.2, you **must** have an Active
Directory/LDAP user for every service, and the Chef environment must
have an override containing the password for that user.

If you are adding Active Directory/LDAP to an existing environment, you
will need to ensure that the service user passwords in Active
Directory/LDAP match the existing MySQL passwords.

Note

The MySQL service user passwords must match the Active Directory/LDAP
server's password policy.

**Procedure 4.1. To retrieve existing MySQL passwords**

1.  Log on to the Chef server.

2.  Run the following command, using the hostname of the primary
    Controller node:

    ~~~~ {.screen}
    $ for i in monitoring glance ceilometer neutron cinder nova; do echo $i; \
      if [ "$i" == "monitoring" ]; \
      then knife node show <primaryControllerNodeHostname> \
      -a keystone | grep -A2 monitoring | \
      awk '/password:/';else knife node show <primaryControllerNodeHostname> \
      -a $i| grep service_pass;fi;done
                            
    ~~~~

    You will receive output listing the MySQL passwords for the
    OpenStack service users.

You can now make changes to the environment that will enable Active
Directory/LDAP in your private cloud.

### Adding Active Directory/LDAP {.title style="clear: both;"}

You will now add your Active Directory environment information to the
Chef environment, which executes the configuration changes in your
OpenStack environment. The procedure is the same for Active Directory
and LDAP.

In this example, you will integrate Keystone and Active Directory in an
environment called `default`{.filename}. This example uses the Knife
command line tool to edit the environment's `.json`{.filename} file.

**Procedure 4.2. To add Active Directory/LDAP to an environment
(Havana)**

1.  In Active Directory/LDAP, create users for the following OpenStack
    services and assign passwords to them:

    -   `ceilometer`{.filename}

    -   `cinder`{.filename}

    -   `glance`{.filename}

    -   `neutron`{.filename}

    -   `nova`{.filename}

    -   `monitoring`{.filename}

    -   `admin`{.filename}

    The `admin`{.filename} user will use the OpenStack admin user
    password.

    If you are adding Active Directory/LDAP to an existing environment,
    be sure to assign to these users the MySQL passwords that you
    retrieved in [Prerequisites for Active Directory/LDAP in OpenStack
    Havana](#ad-ldap-prereqs-havana "Prerequisites for Active Directory/LDAP in OpenStack Havana").

2.  When logged into the Chef server or on a device that has knife
    access to your Chef environment, define your text editor with
    **EXPORT**. In this example, the editor is `vim`{.filename}.

    ~~~~ {.screen}
    $ export EDITOR=vim 
                                    
    ~~~~

3.  Use the **knife** command to enter the environment editing mode.

    ~~~~ {.screen}
    $ knife environment edit default 
                                
    ~~~~

    You will now be able to edit the environment `.json`{.filename} file
    directly.

4.  Locate the `override_attributes`{.filename} setting inside the file.

5.  Locate the `ceilometer`{.filename}, `cinder`{.filename},
    `glance`{.filename}, `neutron`{.filename}, and `nova`{.filename}
    override attributes. If these sections to not exist, you will need
    to add them.

    Add the service passwords that you created in Step 1 to each
    section. Note that in this example and the following examples, only
    overrides relevant to Active Directory are shown. You may have other
    attributes in your environment.

    ~~~~ {.screen}
        "ceilometer": {
          "service_pass": <servicePassword>"
        },
        "cinder": {
          "service_pass": <servicePassword>"
        },
        "glance": {
          "service_pass": <servicePassword>"
        },
        "neutron": {
          "service_pass": <servicePassword>"
        },
        "nova": {
          "service_pass": <servicePassword>"
        },

                                
    ~~~~

6.  Locate the `keystone`{.filename} section within the override
    section. If it does not already exist, you will need to add it.

    Edit the `keystone`{.filename} section to match one of the following
    examples, depending on whether you are using Active Directory or
    LDAP. Add the service password and substituting in the OU and
    objectClass information that you gathered earlier in the lines with
    italicized variables.

    Active Directory Overrides:

    ~~~~ {.screen}
        "keystone": {
          "users": {
            "admin": {
              "password": "<servicePassword>"
            },
            "monitoring": {
              "password": "<servicePassword>"
            },
          "ldap": {
            "user_attribute_ignore": "password,tenant_id,tenants",
            "tenant_allow_create": "True",
            "tenant_allow_update": "True",
            "user_mail_attribute": "mail",
            "user_enabled_attribute": "userAccountControl",
            "user_allow_delete": "False",
            "role_allow_update": "True",
            "domain_objectclass": "Group",
            "tenant_tree_dn": "<OU=Tenants,dc=example,dc=com>",
            "tenant_allow_delete": "True",
            "role_tree_dn": "<OU=Roles,dc=example,dc=com>",
            "role_member_attribute": "roleOccupant",
            "domain_enabled_emulation_dn": "<OU=Domains,dc=example,dc=com>",
            "group_attribute_ignore": "enabled",
            "user_id_attribute": "cn",
            "tenant_member_attribute": "member",
            "url": "ldap://<LDAPServerHostnameOrIP>",
            "tenant_objectclass": "groupOfNames",
            "tenant_id_attribute": "cn",
            "domain_tree_dn": "<OU=Domains,dc=example,dc=com>",
            "use_dumb_member": "True",
            "user_tree_dn": "<CN=Users,dc=example,dc=com>",
            "user_objectclass": "person",
            "tenant_name_attribute": "ou",
            "tenant_desc_attribute": "description",
            "role_objectclass": "organizationalRole",
            "role_id_attribute": "cn",
            "role_allow_create": "True",
            "domain_attribute_ignore": "enabled",
            "suffix": "dc=example,dc=com",
            "dumb_member": "<CN=Administrator,CN=Users,dc=example,dc=com>",
            "user_enabled_mask": "2",
            "user_enabled_default": "512",
            "role_name_attribute": "ou",
            "user_domain_id_attribute": "businessCategory",
            "domain_enabled_emulation": "True",
            "user": "<DOMAIN\\username> or <CN=Administrator,CN=Users,dc=example,dc=com>",
            "password": "<administratorPassword>",
            "tenant_enabled_attribute": "extensionName",
            "user_name_attribute": "sAMAccountName",
            "user_allow_create": "False",
            "user_allow_update": "False",
            "role_allow_delete": "True"
          },
          "auth_type": "ldap",
          "debug": "True"
          "verbose": "True"
        }
                                
    ~~~~

    LDAP Overrides:

    ~~~~ {.screen}
        "keystone": {
          "users": {
            "admin": {
              "password": "<servicePassword>"
            },
            "monitoring": {
              "password": "<servicePassword>"
            },
          "ldap": {
            "user_attribute_ignore": "password,tenant_id,tenants",
            "tenant_tree_dn": "<OU=Tenants,dc=example,dc=com>",
            "role_tree_dn": "<OU=Roles,dc=example,dc=com>",
            "tenant_attribute_ignore": "tenantId",
            "group_attribute_ignore": "enabled",
            "url": "ldap://<LDAPServerHostnameOrIP>",
            "tenant_objectclass": "groupOfNames",
            "tenant_id_attribute": "cn",
            "tenant_enabled_emulation": "True",
            "use_dumb_member": "True",
            "user_tree_dn": "<CN=Users,dc=example,dc=com>",
            "user_objectclass": "person",
            "role_objectclass": "organizationalRole",
            "user_enabled_emulation": "True",
            "allow_subtree_delete": "false",
            "suffix": "<dc=example,dc=com>",
            "user": "<CN=Administrator,CN=Users,dc=example,dc=com>",
            "password": "<administratorPassword>",
          },
          "auth_type": "ldap",
          "debug": "True"
          "verbose": "True"
        }
                                
                            
    ~~~~

7.  Run **chef-client** on the Chef server and on each server in your
    OpenStack environment to implement the changes.

If you would like to view all of the available Active Directory/LDAP
options available in the Rackspace cookbooks you can review them here:

[`https://github.com/rcbops-cookbooks/keystone/blob/master/attributes/default.rb#L22`{.uri}](https://github.com/rcbops-cookbooks/keystone/blob/master/attributes/default.rb#L22)

### Using replicated Active Directory/LDAP controllers across multiple environments {.title style="clear: both;"}

It is possible to replicate Active Directory/LDAP controllers for
multiple Rackspace Private Cloud environments.

This scenario has the following limitations:

-   All service users must have consistent passwords across the
    Rackspace Private Cloud environments. For example, the
    `nova`{.filename} user must have the same password in each
    environment, and the other service users must be consistent as well.

-   Only one Active Directory tree can be used, and all Rackspace
    Private Cloud users must be in the same tree.

-   If you are using the Active Directory/LDAP server for separate
    development and production Rackspace Private Cloud environments, use
    the production environment service passwords. This will ensure that
    you do not lose connectivity and services during a migration.

-   For Rackspace hosting customers: if your environment is located in
    more than one datacenter and you need assistance from Rackspace
    Support, ensure that your support representative is aware of the
    replication.

**Procedure 4.3. To use replicated Active Directory/LDAP controllers**

1.  On one environment, perform the prerequisite and environment update
    procedures documented in the previous two sections.

2.  On a second environment, stop the OpenStack services. If you do not
    stop these services, both environments may lock out the service
    users until Active Directory releases the lock.

3.  Perform the environment update procedure on the second environment.
    The chef-client run will restart the OpenStack services.

    This environment will experience downtime during the chef-client
    run.

4.  Repeat steps 2 and 3 on each environment that will use the Active
    Directory/LDAP server.

Adding Active Directory/LDAP integration for OpenStack Grizzly {.title}
--------------------------------------------------------------

The instructions in this section apply to Active Directory
implementations in Private Clouds that are running OpenStack Grizzly
(Rackspace Private Cloud v4.1.n).

If you are running OpenStack Havana (Rackspace Private Cloud v4.2.2),
refer to Adding Active Directory integration to the Chef environment
(OpenStack Havana).

Note

The instructions in this section should be used **only** for greenfield
deployments of Rackspace Private Cloud and Active Directory/LDAP. If you
need to use an existing Active Directory/LDAP service with Rackspace
Private Cloud, contact your Rackspace support representative.

The following procedure adds your Active Directory environment
information to the Chef environment, which executes the configuration
changes in your OpenStack environment. The procedure is the same for
Active Directory and LDAP.

In this example, you will integrate Keystone and Active Directory in an
environment called `default`{.filename}. This example uses the Knife
command line tool to edit the environment's `.json`{.filename} file.

**Procedure 5.1. To add Active Directory/LDAP information to the Chef
environment (Grizzly)**

1.  Define your text editor with **EXPORT**. In this example, the editor
    is `vim`{.filename}.

    ~~~~ {.screen}
    $ export EDITOR=vim 
                                    
    ~~~~

2.  Use the **knife** command to enter the environment editing mode.

    ~~~~ {.screen}
    $ knife environment edit default 
                                
    ~~~~

3.  You will now be able to edit the environment `.json`{.filename} file
    directly. Locate the `override_attributes: {`{.filename} setting
    inside the file, and locate the `"keystone": {`{.filename} section
    within the override section. If it does not already exist, you will
    need to add it.

4.  Edit the `"keystone": {`{.filename} section to match the following
    code, substituting in the OU and objectClass information that you
    gathered earlier in the lines with italicized variables.

    ~~~~ {.screen}
        "keystone": {
          "ldap": {
            "user_attribute_ignore": "password,tenantId,tenants",
            "tenant_allow_create": "True",
            "tenant_allow_update": "True",
            "user_mail_attribute": "mail",
            "user_enabled_attribute": "userAccountControl",
            "user_allow_delete": "False",
            "role_allow_update": "True",
            "domain_objectclass": "Group",
            "tenant_tree_dn": "<OU=Tenants,dc=example,dc=com>",
            "tenant_allow_delete": "True",
            "role_tree_dn": "<OU=Roles,dc=example,dc=com>",
            "role_member_attribute": "roleOccupant",
            "domain_enabled_emulation_dn": "<OU=Domains,dc=example,dc=com>",
            "group_attribute_ignore": "enabled",
            "user_id_attribute": "cn",
            "tenant_member_attribute": "member",
            "url": "ldap://<LDAPServerHostnameOrIP>",
            "tenant_objectclass": "groupOfNames",
            "tenant_id_attribute": "cn",
            "domain_tree_dn": "<OU=Domains,dc=example,dc=com>",
            "use_dumb_member": "True",
            "user_tree_dn": "CN=Users,dc=<example>,dc=<example2>",
            "user_objectclass": "person",
            "tenant_name_attribute": "ou",
            "tenant_desc_attribute": "description",
            "role_objectclass": "organizationalRole",
            "role_id_attribute": "cn",
            "role_allow_create": "True",
            "domain_attribute_ignore": "enabled",
            "suffix": "dc=example,dc=com",
            "dumb_member": ""<DOMAIN\\username> or <CN=Administrator,CN=Users,dc=example,dc=com>"",
            "user_enabled_mask": "2",
            "user_enabled_default": "512",
            "role_name_attribute": "ou",
            "user_domain_id_attribute": "businessCategory",
            "domain_enabled_emulation": "True",
            "user": "<CN=Administrator,CN=Users,dc=example,dc=com>",
            "password": "<administratorPassword>",
            "tenant_enabled_attribute": "extensionName",
            "user_name_attribute": "cn",
            "user_allow_create": "False",
            "user_allow_update": "False",
            "role_allow_delete": "True"
          },
          "auth_type": "ldap",
          "debug": "True"
        }
                                
    ~~~~

5.  If the schema uses existing LDAP users for the Nova and Glance
    service users, you should also ensure that these are defined in the
    environment file and that user creation, updating, and deletion is
    disabled. If you do not define them here, the Rackspace cookbooks
    will attempt to create those users for you. The following example
    shows an environment with Nova and Glance service user information
    defined.

    ~~~~ {.screen}
          "override_attributes": {
             "glance": {
                     "service_pass": "<glance user password>"
             },
             "nova": {
                     "service_pass": "<nova user password>"
             },
        "keystone": {
          "ldap": {
            "user_attribute_ignore": "password,tenantId,tenants",
            "tenant_allow_create": "True",
            "tenant_allow_update": "True",
            "user_mail_attribute": "mail",
            "user_enabled_attribute": "userAccountControl",
            "user_allow_delete": "False",
            "role_allow_update": "True",
            "domain_objectclass": "Group",
            "tenant_tree_dn": "<OU=Tenants,dc=example,dc=com>",
            "tenant_allow_delete": "True",
            "role_tree_dn": "<OU=Roles,dc=example,dc=com>",
            "role_member_attribute": "roleOccupant",
            "domain_enabled_emulation_dn": "<OU=Domains,dc=example,dc=com>",
            "group_attribute_ignore": "enabled",
            "user_id_attribute": "cn",
            "tenant_member_attribute": "member",
            "url": "ldap://<LDAPServerHostnameOrIP>",
            "tenant_objectclass": "groupOfNames",
            "tenant_id_attribute": "cn",
            "domain_tree_dn": "<OU=Domains,dc=example,dc=com>",
            "use_dumb_member": "True",
            "user_tree_dn": "<CN=Users,dc=example,dc=com>",
            "user_objectclass": "person",
            "tenant_name_attribute": "ou",
            "tenant_desc_attribute": "description",
            "role_objectclass": "organizationalRole",
            "role_id_attribute": "cn",
            "role_allow_create": "True",
            "domain_attribute_ignore": "enabled",
            "suffix": "dc=example,dc=com",
            "dumb_member": "<CN=Administrator,CN=Users,dc=example,dc=com>",
            "user_enabled_mask": "2",
            "user_enabled_default": "512",
            "role_name_attribute": "ou",
            "user_domain_id_attribute": "businessCategory",
            "domain_enabled_emulation": "True",
            "user": "<DOMAIN\\username> or <CN=Administrator,CN=Users,dc=example,dc=com>",
            "password": "<administratorPassword>",
            "tenant_enabled_attribute": "extensionName",
            "user_name_attribute": "cn",
            "user_allow_create": "False",
            "user_allow_update": "False",
            "role_allow_delete": "True"
          },
          "auth_type": "ldap",
          "users": {
            "admin": {
              "password": "Openstack admin password"
            },
            "monitoring": {
              "password": "monitoring password"
            }
          },
          "debug": "True"
        }    
                                
    ~~~~

6.  Run **chef-client** on the Chef server and on each server in your
    OpenStack environment to implement the changes.

7.  Run **chef-client** again. The second run resolves an issue related
    to [Keystone bug
    1176270](https://bugs.launchpad.net/keystone/+bug/1176270).

    Once this process is complete, you will be able to authenticate with
    Keystone with an Active Directory backend.

If you would like to view all of the available Active Directory options
available in the Rackspace cookbooks you can review them here:

[`https://github.com/rcbops-cookbooks/keystone/blob/master/attributes/default.rb#L22`{.uri}](https://github.com/rcbops-cookbooks/keystone/blob/master/attributes/default.rb#L22)

