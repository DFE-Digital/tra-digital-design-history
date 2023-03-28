---
  title: Register with magic link
  date: 2023-03-29
  related:
    sections:
      - title: Prototype of scenarios
        items:
          - text: Replica journey in prototype (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com
---
### Overview
Currently, once a teacher has gets QTS status, they visit the teacher self-service portal (TSSP) to download their QTS certificate. As part of the decommissioning of the TSSP, we’re moving all certificates to the new Access your teaching qualifications (AyTQ) service. Users will need a DfE Identity account (DIA) to access their teaching qualifications.

The first cohort of users that will be given access to the AyTQ service will be those who have attained QTS status.

Since these users have QTS, we don’t need to ask the questions to locate them in the database of qualified teachers (DQT). We’ll use the data gathered in Register and Apply for QTS in England to create a DIA on the user’s behalf. 

Users will then receive an email that points them to create an account to access their QTS certificate.

### Email 
This email contains content that informs the user that they have attained QTS status and instructions to view their QTS certificate on the AyTQ service. The process of creating a DfE Identity account is also mentioned.

The email contains a magic link which is linked to their TRN. It opens the AyTQ start page and also passes the user’s data, so we know who to create the DIA for.

### DfE Identity account (DIA)
As part of setting up an account, the user has to enter their DfE Identity account name, date of birth and mobile number. These data points are different from the ones stored in DQT. An earlier post describes the differences between DQT and DIA data points.

The user is asked to confirm the email address we hold for them. Once confirmed, the user is informed that a DIA has been created and they can access the AyTQ service.

They can sign back in at any point from the original email to AyTQ using their DIA. 

 



