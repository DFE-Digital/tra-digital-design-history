---
  title: Edit GAI user details
  date: 2022-11-02
  related:
    sections:
      - title: Related content
        items:
          - text: Replica journey in prototype (password, trn)
            href: https://find-a-lost-trn-prototype.herokuapp.com/get-an-identity/email/
          - text: Prototype PR
            href: https://github.com/DFE-Digital/tra-digital-design-history/pull/137
---

We’ve designed a journey that lets users of Get An Identity (GAI) update their details, held in both the database of qualified teachers (DQT) and GAI. It also assures that users of GAI services keep their details such as their name up-to-date. 

## What users would see

A video walkthrough of a user editing their GAI details

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('766860694') }}

## What is the problem?

GAI provides a secure way for teachers to access DfE services such as; registering for a National Professional Qualification (NPQ).  

GAI requires users to enter their email address to create an account. They need to authenticate the email by entering a one time code. Next, GAI asks a series of questions to match the user (teacher) against their DQT record. On completion, they will be handed over to the register for a NPQ service.

The problem, existing GAI users have no way of amending their details following the creation of a GAI account. Based on this need we designed a flow which would let users to update their details within the GAI service. 


## Confirm your details page 

A user returning to a GAI service will be prompted to enter their email. After entering their one time code they will then be prompted to review their details before accessing the NPQ service.
 
If their details are correct they can select to continue into the register for NPQ service. If their details have changed or are incorrect they can amend them. 

The page displays the following user details:

- Name (held in DQT)
- Preferred name (held in GAI)
- TRN (held in DQT)
- Email address (Held in GAI)

![The user can confirm or update their GAI and DQT details](1-confirm-details.png "The user can confirm or update their GAI and DQT details")

## Updating your user details

### Name
The user’s name is displayed within its own section and is the name displayed on any teaching certificates. This is because ‘full name’ is held within the DQT database. Unlike the preferred name and email, users have to access the teacher self service portal to make this change. 

On selecting the CTA the teacher self-service portal's start page opens in a new tab. 

![Changing your name requires accessing the Teacher profile](2-update-details.png "Changing DQT names requires accessing the Teacher self-service portal")

### Preferred name
A user can choose to add a preferred name during the GAI journey. If specified, the user will be addressed by their preferred name in all email correspondence from the NPQ service. So if your birth name is Johanna and you’d like to be known as Jo, the email will read Dear Jo.


![Entering your preferred name during the GAI ID flow](8-enter-preferred-name.png "Entering your preferred name during the GAI ID flow")

Within the update your details, a user can choose to either amend or add a preferred name by selecting the change button and completing the preferred name flow.

![The amending of a users preferred name](3-preferredName.png "The amending of a users preferred name")

![The preferred name has been updated and user can continue into NPQ service](4-preferredname-updated.png "The preferred name has been updated and user can continue into NPQ service")




###  Email
The GAI email address can be amended within this page. On selecting the change button, the user will be prompted to enter their new email address and to enter a one time code, sent to the new email address. Once authenticated, the user will access all GAI services using this new email address.


![The user enters their new email address](5-edit-email.png "The user enters their new email address")

![For authentication, a code is emailed to the new address](6-enter-code.png "For authentication, a code is emailed to the new address")

![The email has been updated and the user can continue into NPQ service](7-email-updated.png "The email has been updated and the user can continue into NPQ service")