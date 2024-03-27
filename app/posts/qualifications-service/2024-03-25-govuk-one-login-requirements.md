---
  title: GOV.UK One Login requirements
  date: 2024-03-26
---
## Overview

[GOV.UK One Login](https://www.sign-in.service.gov.uk/) is intended to become the single way for people to sign in to government services online. It enables users to use the same authenticated email address to sign in. They can also verify their identity, for example by scanning a biometric passport, for services that need it.

It will use data from sources such as credit reference agencies to automatically update personal details. For example, changing a name with a bank will also update government services that use GOV.UK One Login. This will make it simpler to use a single login and reduce the need to update details in multiple places.

Access your teaching qualifications currently uses the [DfE Identity account (DfE ID)](https://tra-digital-design-history.herokuapp.com/get-an-identity/). This includes a sign in, and a place to store additional personal details, such as a preferred name or mobile phone number. We want to replace this with GOV.UK One Login. However, DfE need additional information to link the sign in with a teaching record and to deliver services from the Teaching Regulation Agency (TRA).

We’re starting with Access your teaching qualifications, but we are designing the integration so that related services can move from DfE ID to GOV.UK One Login.

This is only for personal users. Services such as Check a teacher’s record use DfE Sign in (DSI) which enables organisational sign ins. This may be something that GOV.UK One Login can do in future.

In addition to the data collected and stored by GOV.UK One Login, we need some extra information for the service. There are 2 groups of additional data, for: 
- identity verification and connecting to a teaching record
- personal information used by the service which GOV.UK One Login does not provide

There are 3 overarching steps:
1. GOV.UK One Login authentication, for signing in each time
2. GOV.UK One Login identity verification, one time
3. DfE connecting to a teaching record, one time

## Additional requirements for connecting to a teaching record

When a user signs in via GOV.UK One Login and verifies their identity, we get their:
- name
- any previous names
- date of birth

We can use the API to ask for their National Insurance number, but this won’t be available until a future release.

We may be able to match these details to a teaching record. In this case, we won’t need to ask for anything else. We’ll connect their login to their teaching record and they can pass through to our service.

If we can’t automatically connect to the teaching record, for example if there is a discrepancy with a name, or multiple records with similar details, we’ll need to ask for more information. 

First, we’ll ask for their National Insurance number. This is because most people with a teaching record have one, and if we have it, we know it’s a strong match. 

If the user does not have or know their National Insurance number, or we can’t find a teaching record with it, we’ll ask for their Teacher Reference Number (TRN). Everyone using the service should have a TRN, but may not have it to hand. If they do then we should be able to connect to their teaching record, unless there are potential duplications which are waiting to be resolved.

If we can’t connect to their teaching record with the additional details, we’ll use this information to generate a request for support.

## Additional requirements for verifying identity

If they are not able to verify their identity through GOV.UK One Login, we’ll only get their email address. This is because they will have authenticated it with an authenticator app or mobile passcode but not successfully completed the next steps to verify. We’ll need to ask for the full set of verification information and an identity document, which will go to a help desk to manually verify. 

Once someone has verified their identity with GOV.UK One Login, they won’t need to do it again. If they have already used it for another service, they won’t need to do it again when accessing ours.

Once we’ve connected a GOV.UK One Login to a teaching record, we won’t need to do it again. They will be able to access their teaching record by signing in.

## Additional requirements for personal details in the service

Part of replacing DfE ID will include having a place to find and change personal details that the service uses. DfE ID had an account profile page for this. 

We are using Access your teaching qualifications as the interface to a teaching record. This is because it already has links to change personal details and is the main way people can access information that is stored in the teaching record system. We may need to [reconsider the name of the service](https://tra-digital-design-history.herokuapp.com/qualifications-service/renaming-of-service/) if it becomes more about accessing a teaching record than just accessing qualifications.

We will include a page to change personal details that are stored by related services using GOV.UK One Login.

For personal details, GOV.UK One Login will store their name and date of birth. We’ll display these fields, and a link to GOV.UK One Login to change them if needed. This will also be where users can change their email address to sign in, password and how they get security codes.

We’ll store a mobile number which users can change themselves. This is used for contact. We may be able to get this from GOV.UK One Login in future, but only if they used mobile to authenticate their sign in.

We’ll show a date of birth which users can change. They’ll need to submit proof to request this change. We include this because sometimes there are mistakes with dates of birth, for example when the TRN was created by an initial teacher training provider, but there was an error. We want to work towards GOV.UK One Login being the source of truth for dates of birth so we can remove this option and automate it.

### Other names

We’ll show an optional field for name on certificates. This is because some users have a name they use professionally for teaching and another that is on their identity documents, for example if they recently got married but want to keep their previous last name at work. Users will need to submit proof to change this.

We’ll show an optional field for preferred name. This is because some of the related services use it, for example if the user preferred a name to be used when contacting them that is different to a professional or official name. They won’t need to submit evidence to change this. GOV.UK One Login are planning to do discovery in future into handling preferred names in their service.

## User journeys

There is a [separate design history entry to explain the user journeys for signing in and connecting with a teaching record](https://tra-digital-design-history.herokuapp.com/qualifications-service/govuk-one-login-sign-in-user-journeys) and [changing personal details](https://tra-digital-design-history.herokuapp.com/qualifications-service/govuk-one-login-change-details-user-journeys), including our plans for testing with users.