---
  title: Checking a teachers DQT record
  date: 2023-03-30
  related:
    sections:
      - title: Links
        items:
          - text: DfE Identity account (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com
---
## How will we know if a user has a TRN?

Before we [create a DfE identity account](/get-an-identity/account-created-scenarios) for some services we try to identify if a user has a TRN, we query the DQT to find their record based on the information they entered into DfE Identity account (DIA). We try to match the user against these 6 DQT data points: 


- Email 
- Name
- Date of birth
- National Insurance 
- TRN
- QTS Qualified Teacher Status (QTS) and ITT provider

These data points let us check if a user has a DQT record and also find out if the associated TRN is attached to another existing teaching identity. This reduces the chances of us creating duplicate records.


Based on the matching of these data points, the following scenarios can occur:


### Scenario 1: A user matches any three data points on a DQT record

We find the user on the DQT and the TRN is located. A DIA account is created and the user continues into the consuming service. 

The following data is passed to the consuming service 

- a TRN (found on the DQT) 
- D.O.B (user has added in DIA) 
- GAI name (user has added in DIA) 
- email address (user has added in DIA) 
- and user id (generated by DIA)

DIA also returns a TRN lookup status <b>'found'</b>, which informs the service that this is a TRN user.

![DQT record found and DIA created](account-created.png "DQT record found and DIA created")

### Scenario 2: The user does not have a DQT record (they do not claim to have a TRN or QTS and other details do not match).

This scenario occurs at the end of the DIA journey. For example, they entered all 6 data points and only 2 or fewer data points were matched (and they told us that they do not have a TRN or QTS). This means we are confident they are not on the DQT.
#### Scenario 2A: Register for NPQ.

An DIA is created and they can continue their application without a TRN. Currently only Register for a NPQ (NPQ) permits user to continue without a DQT record.

Data passed to NPQ:

- D.O.B (user has added in DIA) 
- GAI name (user has added in DIA)
- email address (user has added in DIA) 
- and user id (generated by DIA)

DIA also returns a TRN lookup status <b>'none'</b>, which informs NPQ that this is a Non-TRN user.

![No DQT record found and DIA created](account-created.png "No DQT record found and DIA created")


#### Scenario 2B: Access your teaching qualifications .
For the access your teaching qualifications the user will be prevented from continuing until they have record on the DQT.

A DIA account is created and next time they apply a DQT look will occur before they can access the service.

![No DQT record found - user can't continue](no-dqt.png "No DQT record found - user can't continue into service")


### Scenario 3: They do not match a DQT record, but we need to manually check as we suspect they could have a record.

This scenario occurs when 2 or fewer data points are matched, and the user has implied that they have a TRN or QTS. 

They either misentered the TRN or have left it blank after telling us they have one.

They told us that they have QTS but did not enter a recognised institution.

#### Scenario 3A: Register for NPQ .

At the end of the GAI questions we tell them that although we could not find their record, they can continue to apply for an NPQ.

Data passed to NPQ 

- D.O.B (user has added in DIA) 
- GAI name (user has added in DIA)
- email address (user has added in DIA) 
- and user id (generated by DIA)

DIA also returns a TRN lookup status <b>'pending'</b>, which informs NPQ that a manual check is needed before they process the user’s application.

At the same time we raise a ticket for a support agent to manually find their DQT record. 

![Further DQT checks needed by helpdesk - user CAN continue into service](pending-npq.png "Further DQT checks needed by helpdesk - user CAN continue into service")


#### Scenario 3B: Access your teaching qualifications .
For the access your teaching qualifications the user will be prevented from continuing until the DQT checks are complete.

A DIA account is created only if their record is found, they can sign back into the service once they have been notified.

Then Data passed to quals matches that of NPQ. 

![Further DQT checks needed by helpdesk - user CANNOT continue into service](pending-quals.png "Further DQT checks needed by helpdesk - user CANNOT continue into service")

### Support ticket scenarios

Scenario A: If the TRA support agent finds the user’s DQT record.

DIA returns a TRN lookup status  <b>'found'</b>, the application can continue and a TRN is returned to the consuming service.

Scenario B: If we still cannot find a record.

DIA returns a TRN lookup status  <b>'failed'</b>, they are not on the DQT and no TRN is returned.