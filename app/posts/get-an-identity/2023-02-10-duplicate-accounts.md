---
  title: Identifying duplicate accounts
  date: 2023-02-10
  related:
    sections:
      - title: Identifying duplicate accounts
        items:
          - text: Replica journey in prototype (password, gai) See edge cases
            href: https://get-an-identity-prototype.herokuapp.com
          - text: Lucid board showing flow
            href: https://lucid.app/lucidspark/b88634d8-2452-4ed6-9c7c-010383770731/edit?view_items=KZDsx9Mr-.mh&invitationId=inv_9a36d007-204a-41ed-b8c3-1f49d5e63a05
---


A key requirement for the DfE Identity account (DIA) is to reduce the chances of the same user creating duplicate accounts.  

The Apply for a national professional qualification (NPQ) service uses Get an Identity (GAI) as its authentication solution. The GAI journey also incorporates a database of qualified teachers (DQT) lookup to locate a teacher record, which is passed to the NPQ service. When a user matches against an existing GAI account (matched to a DQT record) using a new email, we prompt the user to sign in to the existing account with a one time passcode (OTP). This prevents duplicate GAI accounts being created.

This matching only works when the teacher has a record on the DQT.  What about the users who do not have a DQT record?

DIA needs to collect its own set of user data. This will help us determine whether an account is unique or a duplicate.


## What user data does DIA collect?

When [creating an DIA](/get-an-identity/integrating-qts/#create-account-journey), we ask the user for the following data points:

- Email
- Mobile number
- First and last name
- Date of birth

The following scenarios describe the steps the service takes to stop duplicate accounts from being created.


## Duplication scenarios

### Scenario 1
User enters an <b>existing email address</b> that matches a DIA:

- Selects to create an account
- Enters their email address (DIA recognises email)
- Confirms their email with OTP (Confirms user as owner of the DIA)
- A sign in interstitial page informs the user they have an account and prompts them to sign in
- User signs in to their service

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('797379055') }}


### Scenario 2
User enters an <b>Existing mobile phone number</b> that matches a DIA:

- Selects to create an account
- Enters their email address (Does not match existing account)
- Confirms their email with OTP
- Enters their mobile number  (DIA recognises number)
- Confirms their number with OTP  (Confirms user as owner of the DIA)
- A sign in interstitial page informs the user they have an account and prompts them to sign in
- User signs in to their service

{{ appVimeo('797379082') }}


### Scenario 3
User enters a Name and Dob that matches a DIA

- Selects to create an account
- Enters their email address (Does not match existing account)
- Confirms their email with OTP
- Enters their mobile number  (Does not match existing account)
- Confirms their number with  OTP
- Enters their name (TSA recognises name)
- Enters their Date of Birth (TSA recognises DOB)
- An account disambiguation page is presented

Where user is given two options:

1. Sign in to an existing account? (that matches the Name and DOB entered)
- Select to log in to an existing account
- Enters OTP sent to email associated with account
- User signs into service

2. Continues to create an account using email they entered
- TSA account created screen is displayed
- Continues to the consuming service

{{ appVimeo('797379097') }}

![Choose account ](chooseEmail.png "Choose account")
