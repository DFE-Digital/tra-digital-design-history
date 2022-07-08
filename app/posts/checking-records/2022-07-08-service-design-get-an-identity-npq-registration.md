---
title: NPQ registration for TRN holders 
date: 2022-07-08
---

Prospective NPQ participants currently have to have a TRN to register for an NPQ. 

The Register for an NPQ service checks that the personal details provided match a record in the Database of Qualified Teachers (DQT) before passing the registration on to the NPQ Provider. This is because at the end of the course, when providers report that someone has completed an NPQ to the TRA, the personal details the provider has - in particular the TRN - need to exactly match the person's DQT record.

The NPQ service is purely transactional with no concept of accounts - it doesn't recognise the same person registering for another NPQ.

Get an identity to access Teacher Services will provide Register for an NPQ with a reliable pointer to an individual's DQT record, and functionality to identify repeat users of Register for an NPQ. 

In future, we expect to use Get an identity to access Teacher Services to identify individuals' records across other Teacher Services, and thereby reduce our reliance on matching names, dates of birth and TRNs across datasets.

## First iteration
The first iteration of the service still requires users to have a TRN to register for an NPQ. It simply replaces Register for an NPQ's validation flow with the new service, Get an Identity to access Teacher Services.

Once we have built and validated this iteration, we can progressively turn on the TRNless features. 

[![NPQ registration with Get an identity to access Teacher Services design](get-an-identity-npq-registration.jpg)](get-an-identity-npq-registration.jpg)


### Failover to manual record linking

Where a user should have a TRN but can't be matched to it, rather than redirecting them to the Find a lost TRN service, Get an identity to access Teacher Services will directly create a lost TRN zendesk ticket. 

The TRA helpdesk will need to enter the TRN into a support screen of the Get an identity service, so that the user can pick up where they left off.

We expect only a very small proportion of users to have to go down the manual route. The Find a lost TRN service is able to match more than 80% of users automatically, and that is based exclusively on users who don't know their TRN. In contrast, analysis suggests most users of the NPQ service know or have access to their TRN.

We do not anticipate this feature increasing the TRA helpdesk's workload, as people who want to register for an NPQ currently contact helpdesk or use the Find a lost TRN service. 


## Things to address next

### 1. Details updates without a TRN 
At present, participants whose details are found to be wrong by providers at the identity checking stage, or whose details change during their NPQ, such as using a different surname after marriage, are told to update their details with DfE via the TRA's Teacher self service portal. You can only access the self service portal if you have a TRN.

Our next step will be to create a mechanism for NPQ participants to update their Teacher Services identity without a TRN if they don't meet the criteria to be in the DQT. This will involve uploading proof of identity or details change, such as a marriage certificate, which will be checked by a support agent within Teacher Services.

In the future, we should pursue a route for NPQ providers, when they perform their identity check, to report back verified identity information (including any updates) to the identity service via the NPQ service.

### 2. Registration without a TRN
When we have a solution for updating records after an identity check which is not reliant on TRN, we can enable users to register for an NPQ without getting a TRN.

This will mean that when we don't find a match to a DQT record AND it's because the person doesn't have a TRN, they will be able to continue to register without any DQT data. We can do this with the understanding that if their self reported details aren't accurate, this will be picked up in the provider identity check, who will ask them to update their details.

We need to work out ASAP how we will confidently determine why we didn't find a TRN in each case - because the person doesn't have one, or due to inaccurate matching data. 

We need to ensure that we don't mistake people whose TRN we failed to find with people who don't have TRNs, because this would equate to telling the NPQ service that someone is not a qualified teacher and does not have any sanctions in cases where that may not be true.

### 3. Certificates without a TRN
By the time that the first TRNless participants complete their NPQs, we will need a mechanism to get an NPQ certificate without a TRN. This could be achieved by sending out certificates by email, or it may be that the redesigned Teacher self service portal also caters to TRNless non-teachers accessing their NPQ certificates.


### 4. Employer access to NPQ records for participants without a TRN
Additionally, by the time that the first TRNless participants complete their NPQs, we need to understand whether there is a need for employers to confirm NPQ completion by people who aren't qualified teachers, and if so, design a solution for this. This functionality could be part of the future employer checks service.


### 5. Integration with GOV.UK account
In future we might want Get an identity to integrate with GOV.UK account. 



