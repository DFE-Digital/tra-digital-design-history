---
  title: Renaming of service
  date: 2023-03-20
  related:
    sections:
      - title: Identifying duplicate accounts
        items:
          - text: Replica journey in prototype (password, gai) See edge cases
            href: https://get-an-identity-prototype.herokuapp.com
---


A key requirement for the DfE Identity account (DIA) is to reduce the chances of the same user creating duplicate accounts.  

The Apply for a national professional qualification (NPQ) service uses Get an Identity (GAI) as its authentication solution. The GAI journey also incorporates a database of qualified teachers (DQT) lookup to locate a teacher record, which is passed to the NPQ service. When a user matches against an existing GAI account (matched to a DQT record) using a new email, we prompt the user to sign in to the existing account with a one time passcode (OTP). This prevents duplicate GAI accounts being created.

This matching only works when the teacher has a record on the DQT.  What about the users who do not have a DQT record?

DIA needs to collect its own set of user data. This will help us determine whether an account is unique or a duplicate.


## What user data does DIA collect?

When creating an DIA, we ask the user for the following data points:

- Email
- Mobile number
- First and last name
- Date of birth
