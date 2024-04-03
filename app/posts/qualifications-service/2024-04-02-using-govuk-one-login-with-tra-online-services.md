---
  title: Using GOV.UK One Login with TRA online services
  date: 2024-04-02
---

[GOV.UK One Login](https://www.sign-in.service.gov.uk/) is intended to become the single way for people to sign in to government services online. It allows users to:

- sign in to each service using the same authenticated email address
- verify their identity so that details are available to services that need them

A user will only be asked to verify their identity the first time they access a service which needs it. Some services will only need an authenticated email address.

Once someone has a GOV.UK One Login, their personal details are automatically updated from sources such as credit reference agencies.

For example, if a user changes the name they use for their bank accounts then this change will also be made in their GOV.UK One Login.

## Replacing DfE Identity with GOV.UK One Login

Users of TRA services currently access them using a DfE single sign in service. This is either:

- DfE Sign In - for services used by people working in organisations such as schools
- [DfE Identity](https://tra-digital-design-history.herokuapp.com/get-an-identity/) - for services used by individuals such as teachers

GOV.UK One Login will replace DfE Identity.

We’re starting by adding it to the Access your teaching qualifications (AYTQ) service. We chose this service because:

- it allows users to view their teaching record, which includes personal details
- it gives a route for users to change the personal details in their teaching record - there's a link from AYTQ to DfE Identity

Once we move from DfE Identity to GOV.UK One Login, we’ll have a different set of personal details to show and for users to change.

## New user journeys

We wanted to do research to find out the impact of this change on users. In particular we wanted to see how users deal with:

- creating a GOV.UK One Login and verifying their identity
- being asked additional questions so that we can connect their GOV.UK One Login to a teacher record
- being told that they need to get support to connect their teaching record to their GOV.UK One Login

We also wanted to find out:

- whether users understand that they’re creating a GOV.UK One Login which can be used for other services
- if it’s important for them to understand this

We created design history entries to give details of the user journeys we tested. These are:

- [signing in for the first time](/qualifications-service/signing-in-for-the-first-time-using-govuk-one-login)
- [changing personal details](/qualifications-service/changing-personal-details-after-signing-in-through-govuk-one-login)
