---
title: MVP
date: 2022-09-27
---

We’re mapping versions of Get an Identity in [Miro](https://miro.com/app/board/uXjVPZGw840=/).

The MVP, as we’ve described in previous posts, will support users who have TRNs to Register for an NPQ. 

[![MVP service design](mvp-service-design.jpg)](mvp-service-design.jpg)

The service is composed of three parts:

## 1. Authenticate

Users can access the service with any email address, whether it is associated with an existing identity or not, and then enter a one time passcode to demonstrate they have access to that email account. 

There is no identity verification. Users registering for an NPQ do not get access to any sensitive data, and identity checks are performed by NPQ providers, so there is no need for any further security for MVP. We expect this will change when we onboard other services. 

We’ve written about the pros and cons of introducing mobile numbers for 2FA in [Asking for mobile numbers to improve security](/get-an-identity/mvp-2fa/), and about the impact that integrating with GOV.UK Account may have in [Exploring GOV.UK Sign-in for MVP](/get-an-identity/integrating-govuk-accounts/). 

After entering the one time passcode:

a) If the email address a user provided already belongs to an identity, then we have already have a link to their record in DQT, so we do not need to do anything else. The user will see the record they have been matched to, and then continue to register for an NPQ. (also see previous TRNless users in the "what’s next" section below) 

b) If the email address is new, the matching flow kicks in.

## 2. Match

The flow to match a user to a DQT record is based on Find a lost TRN. We need users to provide three identifiers which match a DQT record to confirm their TRN. This might include their email address, current or previous name, date of birth, national insurance number, or, if they have QTS, their ITT provider.

During the matching, we also ask for the user’s preferred name (see [Asking for people's names](/get-an-identity/names-in-get-an-identity/)) and under certain conditions, unlock their teacher self service portal account (see [Unlocking Teacher Self-Service Portal accounts](/find-a-lost-trn/unlocking-tssp-accounts/))

a) If we find a TRN

- we store the TRN as part of the identity, so that we do not need to do any more fuzzy matching next time the identity is used
- If we asked the user what their TRN was, but the record we matched them to had a different TRN, then we tell them the TRN we found. We wrote about this in [When TRNs do not match what the user said](https://tra-digital-design-history.herokuapp.com/get-an-identity/trn-edge-cases/)
- we compare the details the user gave us to the ones in the DQT record. If anything is different, we send them an email telling them what is in their DQT record, and letting them know they can update their details through the teacher self service portal (also see updating your details whilst registering in what's next)

b) if we do not find a TRN

- in the MVP, all users have to have TRNs, so we create a support ticket to match the user to a TRN. (also see no match scenario in the "what’s next" section below)
- people can continue to register for an NPQ in the meantime before a support agent finds their TRN
- We have written about the support process in more detail in  [Support screens for adding a DQT record](https://tra-digital-design-history.herokuapp.com/get-an-identity/support-link-dqt/)

c) if we find a TRN but it has already been claimed by another identity, then we let the user update their email address 

## 3. Update

In the scenario above, someone is accessing get an identity for the second time with a different email address. We send another one time passcode to the existing email address we have on record for that TRN. 

a) If the user has access to that email account, they can retrieve the passcode, then choose which email address to use in future. 

b) If they do not have access, they need to contact support and prove their identity. 

We wrote about this in [When a user returns with a different email address](https://tra-digital-design-history.herokuapp.com/get-an-identity/same-user-different-email/)

When users with TRNs need to change other details, such as their name, date of birth, or national insurance number, they can do this through the teacher self service portal of the DQT. Changes made to DQT records will be synchronised with get an identity and therefore available to register for an NPQ if needed. Also see Updating your details if you do not have a TRN in the what’s next section below.

# What’s next after MVP?

## Updating your details if you do not have a TRN

The main blocker to get an identity supporting TRNless users is that these people don’t have a way to update their details. We wrote about this in  [Details updates without a TRN](https://tra-digital-design-history.herokuapp.com/get-an-identity/service-design-get-an-identity-npq-registration/#1.-details-updates-without-a-trn). 

We need to do more work on this, but we currently think we can offer a google form as short term solution, with the need to be better met by the teacher account in the near future. 

![Phases to enable updates](updates-phases.jpg)

## No match scenario

When we are ready to allow our first TRNless users, there will instead be two different possibilities when we can not match someone to a TRN automatically:

1. They do not have a TRN
2. They do have a TRN, but we did not find it, for example because some of their details are inaccurate in DQT

The service will need to distinguish between these two cases. We wrote about the importance of this in [Registration without a TRN](https://tra-digital-design-history.herokuapp.com/get-an-identity/service-design-get-an-identity-npq-registration/#2.-registration-without-a-trn) and about how we might achieve it in [Knowing if someone has a TRN](https://tra-digital-design-history.herokuapp.com/get-an-identity/improving-chances-of-a-match/). 

## Previous TRNless users

In future when users do not have to have TRNs, it will be possible to get an identity (by registering for an NPQ), then get a TRN (e.g. by starting teacher training), then use another service that authenticates using get an identity (e.g. another NPQ). Given this, we may need to check DQT every time a TRNless person authenticates with Get an Identity, in case they have been given a TRN in the meantime.

## Updating your details whilst registering

In future, rather than sending someone an email to tell them the details they gave us do not match DQT, we may want to allow them to prove their new name / change their date of birth / etc. before they carry on to Register for an NPQ.