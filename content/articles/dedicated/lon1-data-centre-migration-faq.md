---
node_id: 4572
title: LON1 Data Centre migration FAQ
permalink: article/lon1-data-centre-migration-faq
type: article
created_date: '2015-03-02 11:04:29'
created_by: DarrenKidgell
last_modified_date: '2015-07-23 16:0353'
last_modified_by: renee.rendon
products: Dedicated
body_format: tinymce
---

### **Overview**

Rackspace is opening a new data centre, LON5, in May 2015. The new data
centre will support our customers&rsquo; growth with newer technologies and
enable us to offer customers our current hosting product portfolio. To
this end, we will be closing the LON1 data centre and all customers'
solutions currently hosted in LON1 will be migrated to the new data
centre. The migration period will start in June 2015.

Rackspace has had widespread success in data centre migrations over the
past 12 years. During this time our dedicated migration teams have:

-   In 2009, migrated 15,000 devices from our LON2 Data Centre into our
    LON3 Data Centre
-   In 2011, migrated 3,828 devices from our SAT1 and SAT2 Data Centres
    to our DFW1 Data Centre
-   In 2012, migrated 8,200 devices from our IAD1 Data Centre to our
    DFW1 and IAD3 Data Centres

During these migrations, the teams returned 100% of solutions online
within the advertised move window and experienced a component failure
rate of less than 1 percent.

We realise that you have chosen Rackspace as your hosting provider
because you trust our expertise and commitment to support you. You can
rest assured that we have invested significant planning and resources in
thorough migration planning. This article answers many of the questions
you may have about this planned migration. If you have further
questions, see the [contact
information](#Who%20should%20I%20contact%20if%20I%20have%20more%20questions%20about%20the%20migration?)
at the bottom of this article.

 

**Content**

-   [Why is Rackspace closing the LON1 Data
    Centre?](#Why%20is%20Rackspace%20closing%20the%20LON1%20Data%20Centre?)
-   [How will this migration be
    performed?](#What%20are%20the%20high%20level%20stages%20of%20the%20migration?)
-   [Will service be
    interrupted?](#Will%20there%20be%20any%20interruption%20to%20service?)
-   [Will there be any IP or DNS
    changes?](#Will%20there%20be%20any%20IP%20or%20DNS%20changes%20I%20need%20to%20worry%20about?)
-   [When are my servers scheduled to be
    migrated?](#When%20are%20my%20servers%20scheduled%20to%20be%20migrated?)
-   [How do I prepare for the
    migration?](#How%20will%20I%20need%20to%20prepare%20for%20the%20migration?)
-   [Is the move date flexible? Can I choose the date of the
    migration?](#Is%20the%20move%20date%20flexible,%20can%20I%20choose%20the%20date%20of%20the%20migration?)
-   [I have more than one solution with Rackspace. Will they all be
    migrated at the same
    time?](#I%20have%20more%20than%20one%20solution%20with%20Rackspace,%20will%20they%20all%20be%20migrated%20at%20the%20same%20time?)
-   [Will my services
    change?](#Will%20any%20of%20the%20services%20that%20Rackspace%20currently%20offer%20me%20change?)
-   [How will my solution be
    transported?](#How%20will%20my%20solution%20be%20transported?)
-   [Will my server have to be migrated again in the
    future?](#Are%20there%20any%20guarantees%20that%20my%20server%20will%20not%20have%20to%20be%20migrated%20again%20afterwards?)
-   [Am I entitled to any compensation resulting from this
    move?](#As%20a%20customer,%20am%20I%20entitled%20to%20any%20compensation%20resulting%20from%20this%20move?)
-   [Where is LON5 located?](#Where%20is%20LON5%20located?)
-   [Does the LON5 Data Centre have the same level of redundancy and
    security as the LON1 Data
    Centre?](#Does%20the%20LON5%20Data%20Centre%20have%20the%20same%20level%20of%20redundancy%20and%20security%20as%20the%20LON1%20Data%20Centre?)
-   [What assurance can Rackspace provide customers regarding security
    controls in the new LON5 Data
    Centre?](#What%20assurance%20can%20Rackspace%20provide%20customers%20regarding%20security%20controls%20in%20the%20new%20LON5%20Data%20Centre?)
-   [Has an SSAE16 / ISAE 3402 SOC report been completed for the LON5
    Data
    Centre?](#Has%20an%20SSAE16%20/%20ISAE%203402%20SOC%20report%20been%20completed%20for%20the%20LON5%20Data%20Centre?)
-   [Will the LON5 Data Centre be PCI-DSS
    compliant?](#Will%20the%20LON5%20Data%20Centre%20be%20PCI-DSS%20compliant?)
-   [What are the green credentials of the new LON5 Data
    Centre?](#What%20are%20the%20green%20credentials%20of%20the%20new%20LON5%20Data%20Centre?)
-   [Who should I contact if I have more questions about the
    migration?](#Who%20should%20I%20contact%20if%20I%20have%20more%20questions%20about%20the%20migration?)

 

******Why is Rackspace closing the LON1 Data Centre?**

 

Rackspace has operated the LON1 Data Centre for nearly 14 years,
providing you and other customers with a stable and secure location.
Although it has served Rackspace and our customers well, advances in
data centre design and our own product portfolio enhancements over the
years have rendered LON1 less efficient and flexible than our other data
centre facilities. Significant upgrades to electrical and network
infrastructure would be required to deploy many of our new products and
services to solutions present in LON1. The risks involved in
implementing these upgrades, outweigh the benefits of such significant
works.

 

### ****

[\<top\>](#TOP)

### **How will this migration be performed?**

1.  Your migration date will be determined by the location of your
    hosted devices. To minimise the impact to customers we will move
    servers in small contiguous blocks.
2.  Before your migration date, Rackspace will work with you and your
    account team to establish any specific requirements for the move.
3.  On the date of your migration, all affected devices will be
    physically powered down.
4.  The affected devices will be securely transported to the new data
    centre facility.
5.  All devices will be reconnected and powered up.
6.  Your configuration will be tested and verified at an infrastructure
    level. Your account team can arrange further testing, if needed.

The geographical relocation will not be apparent to external users.

### 

[\<top\>](#TOP)

### **Will service be interrupted?**

To minimize the amount of downtime for customers, Rackspace has designed
the migration to occur in small contiguous blocks.. Our project plan
also seeks to reduce the amount of unplanned downtime by including
additional resources and multiple contingency plans. The total scheduled
migration window will be eight hours but our goal is to return to
service as quickly as possible.

[\<top\>](#TOP)

### **Will there be any IP or DNS changes?**

No, the primary and secondary IP addresses of your devices will move
with the devices to the new location. You will not need to make any
changes to your DNS.

[\<top\>](#TOP)

### **When are my servers scheduled to be migrated?**

1.  You will receive a notification via a ticket on the Rackspace
    customer portal at least three months in advance of your migration
    date. The ticket will include the specific date and time that your
    solution will be moved.
2.  You will receive an additional notification 60 days and 30 days
    before the migration date.
3.  One week before the migration date, you will receive a final
    reminder.
4.  On the night of the migration, you will receive a notification
    confirming the migration will proceed as scheduled.
5.  After your solution arrives in LON5, you will receive an update
    notification confirming a safe physical delivery of your solution.
6.  After your solution is back online you will receive a further update
    confirming the completion of the migration.

[\<top\>](#TOP)

### **How do I prepare for the migration?**

Rackspace will use all of our experience of data centre migration
projects to help support you during the migration to LON5. We have a
dedicated migration team that will work with you and your account team
to determine and arrange any special requirements that you might have
for pre- and post-migration as we power down and power up your solution.
The migration team will then be focused on successfully executing on all
the specifications on the night of the migration.

We encourage customers to make their own offsite backups and to use the
Managed Backup solution Rackspace offers. If your solution is not
currently being backed up, we recommend that you talk to your Rackspace
account team to get backups in place before the migration date.

[\<top\>](#TOP)

### **Is the move date flexible? Can I choose the date of the migration?**

The migration project has been split into phases based on the physical
data centre configuration. To avoid having to change IP addresses on
your solution we have to move customers in a set time frame during each
phase. Rackspace will give you advance notice of this date and time so
that you can plan accordingly with your customers and end users but  we
cannot change the date of your move without further impacting your
solution.

If your scheduled migration date is so impractical for you that a
rescheduled date becomes absolutely necessary then an IP address change
might be required on your solution. This change will include DNS changes
and potential configuration work on your side to accommodate the new IP
addresses.

### 

[\<top\>](#TOP)

### **I have more than one solution with Rackspace. Will they all be migrated at the same time?**

Migration time depends on where those solutions are physically located
within the data centre. The move has been split into phases; if the
solutions are in the same phase, they will be moved in the same time
frame.

[\<top\>](#TOP)

### **Will my services changes?**

There will be no change to any of the services that you currently
consume. The only change to your solution will be the physical location.

As part of the migration strategy, Rackspace is excited about the number
of additional value-add services that we will be able to offer our
customers from our full Managed Cloud portfolio.

[\<top\>](#TOP)

### **How will my solution be transported?**

We will be using a third party specialist transport company. To ensure
the safe transportation of your solution Rackspace has carefully and
extensively planned this migration and selected appropriate partners to
mitigate any risks arising from the move. Vendor analysis and risk
evaluation and mitigation documents are available upon request from the
migration team if you want to review them.

The vehicles will be loaded within our data centres and are subject to
our stringent physical security controls. They will be unloaded within
the same conditions in LON5.  The tailgate of the truck will be locked
with a special bolt by Rackspace personnel.  The trucks will have GPS
tracking. They will not carry the Rackspace logo. The trucks will be
followed by Rackspace personnel from LON1 to LON5.

[\<top\>](#TOP)

### **Will my server have to be migrated again in the future?**

Rackspace has invested heavily in the design and construction of the
LON5 Data Centre and in our partnership with Digital Realty Trust, a
company dedicated to data centre design and construction.

The lease associated with the LON5 Data Centre is in excess of 20 years.
We hope that this provides you some reassurance that we are making every
effort not to migrate you again in the future.

[\<top\>](#TOP)

### **Am I entitled to any compensation resulting from this move?**

To carry out the migration, we are scheduling an eight hour migration
window as a scheduled maintenance. You might be entitled to a service
credit under your contractual arrangements with Rackspace for downtime
that is not associated with a permitted scheduled maintenance. You will
be entitled to claim any service credit due to you in the normal manner.

[\<top\>](#TOP)

### **Where is LON5 located?**

This facility is located near Crawley, Sussex. For security reasons, we
have not published the address in this FAQ. You can obtain the address
from your account team on a confidential basis and with valid
justification, such as the need to coordinate the installation of
private circuits.

[\<top\>](#TOP)

### **Does the LON5 Data Centre have the same level of redundancy and security as the LON1 Data Centre?**

Yes, the LON5 Data Centre provides the same or improved levels of
redundancy and more resilience in its electrical and mechanical
infrastructure than LON1. Security protocols and operations for LON5 are
in line with all data centres in the Rackspace global portfolio.

[\<top\>](#TOP)

### **What assurance can Rackspace provide customers regarding security controls in the new LON5 Data Centre?**

All Rackspace entities implement uniform global data centre security and
environmental controls in their data centres.

The new LON5 Data Centre will implement the same standard security
controls that have been implemented in our other data centres and that
have been assessed in those other data centre as meeting the
requirements of our ISO 27001, PCI-DSS SP L1 and ISAE / SSAE standards.

LON5 will undergo external assessment against ISOv27001 before opening
to our customers, with the other compliance standards being audited
externally in line with our set annual compliance schedule.

Customers will be able to request a copy of our ISO 27001 certificate,
as well as an attestation from our Compliance Director that states that
the appropriate security and environmental controls have been
implemented to meet the PCI DSS SP L1 and ISAE/ SSAE standards to which
we adhere.

[\<top\>](#TOP)

### **Has an SSAE16 / ISAE 3402 SOC report been completed for the LON5 Data Centre?**

The LON5 Data Centre will come online in the middle of the Rackspace
ISAE / SSAE annual audit cycle and will therefore not be assessed upon
opening.

The reporting period for the Rackspace Service Organization Controls
(SOC) 1, 2, and 3 reports is from 1 October to 31 September. The
assessment will be conducted by our auditors between September and
November 2015, with the final report being made available in early
December 2015.

[\<top\>](#TOP)

### **Will the LON5 Data Centre be PCI-DSS compliant?**

The LON5 Data Centre will come online before the Rackspace Annual
PCI-DSS Service Provider audit.

The PCI-DSS SP L1 external audit will occur between May and July 2015.
The Attestation of Compliance will then be available for customers by
early August 2015.

[\<top\>](#TOP)

### **What are the green credentials of the new LON5 Data Centre?**

In support of our commitment to our customers, our employees and the
environment, our LON3 Data Centre and our UK head office (LON4) are
certified to the international environmental management standard, ISO
14001, which provides a framework for managing our environmental
responsibilities, including energy and waste management. We will extend
the scope of this to LON5 in the next audit cycle. In the meantime
following are some of the initiatives we have implemented in LON5 to
reduce our carbon footprint:

-   The data centre construction will have a BREEAM rating of Very Good.
    BREEAM for new construction covers items such as environmentally
    sourced paint, LED lighting, minimising land fill and impact on
    environment during construction
-   LON5 will have an annualised Power Usage Effectiveness (PuE) of 1.15
    (versus 1.58 in LON3)
-   Removal of the mechanical cooling systems in the data halls means we
    can maintain a more stable PuE rating for the facility
-   The indirect cooling solution uses much lower water quantities than
    other systems in its class and significantly less water than a
    cooling tower
-   Rain harvesting will be leveraged and used in back of house
    amenities and for the adiabatic spray in the indirect cooling
    solution.
-   Sun pipes in some areas will bring in natural light to reduce the
    need for artificial lighting
-   Power will be pulled into the site from higher up the grid to attain
    a more efficient delivery of power to the site

[\<top\>](#TOP)

### **Who should I contact if I have more questions about the migration?**

You can raise a ticket in the My Rackspace portal. Please request in the
ticket that it gets assigned to the LON DC Migration ticket queue.\
 You can contact the following members of the migration team directly:

Sarah Welburn\
 Tel: +44 (0) 20 8734 4265\
 Email: sarah.welburn@rackspace.co.uk

Josie Harper\
 Tel: +44 (0) 20 8734 2669\
 Email: josie.harper@rackspace.co.uk

You can also ask your account team for more information.

[\<top\>](#TOP)

