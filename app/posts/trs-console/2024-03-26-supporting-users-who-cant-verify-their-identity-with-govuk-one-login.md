---
title: Supporting users who can’t verify their identity with GOV.UK One Login
date: 2024-03-26
description: Creating a way for support staff to manually verify users' identity.
screenshots:
  items:
    - text: Support tasks landing page
      src: support-tasks-landing-page.png
    - text: Details about the failed identity verification
      src: failed-id-verify-details.png
    - text: A success screen for connecting a record
      src: record-connected.png
    - text: Change history event for connecting a record
      src: connected-change-history.png
---

## Overview

GOV.UK One Login offers [support for users who have a problem during their service](https://www.sign-in.service.gov.uk/support). For example, if they are struggling to create an account, sign in, or verify their identity.

However, it is possible to pass through and remain unverified. For example, if the user selects ‘no’ to all the identity verification options. Users can also be [verified, but we can’t connect them to a teaching record](). 

[add link to other TRS support post for connecting fail]: #

## Unverified

At the end of the GOV.UK One Login flow if the user hasn’t verified their identity or got support from GOV.UK One Login, they’ll then be passed back to our service unverified. We’ll only know their authenticated email address.

As we require users’ identities to be verified before we can connect their GOV.UK One Login to their teaching record, they won’t be able to access the service at this point.

In this scenario, we need to [offer users another way to prove their identity](https://www.sign-in.service.gov.uk/about/checking-users-identities/evidence-types#:~:text=Users%20who%20cannot%20prove%20their%20identity).

In the [user journey to sign in to Access your teaching qualifications using GOV.UK One Login](), we include some inputs to collect the personal information that we need to manually verify their identity and connect to a teaching record. This includes uploading a proof of ID.

[add link to other AYTQ One Login post]: #

We use this information to generate a support task.

## Support tasks

We’ve redesigned the [manage change requests function](https://tra-digital-design-history.herokuapp.com/trs-console/managing-change-requests/) for support tasks. This is because there will now be support tasks for:
- change requests
- GOV.UK One Login
- [de-duplication]()

[add link to other TRS support post for duplications]: #

A list of support tasks is included in a table in the right hand three quarters column. There are options to sort by date requests or the task type. The default view is sorted with the oldest first.

In future, there may be more user roles associated with support tasks and we can show the relevant tasks based on their roles.

For the wireframes, we’ve used the reference format used by the legacy Dynamics service, such as `CAS-01006-F4Q3Z7`. We won’t be using this format in production but the new format still needs to be defined.

### Filters

We’ve added a filters panel in the left hand [one quarter column](https://design-system.service.gov.uk/styles/layout/#:~:text=%3C/div%3E-,One%2Dquarter,-Open%20this%20example).

This uses:
- [smaller checkboxes](https://design-system.service.gov.uk/components/checkboxes/#:~:text=in%20services.-,Smaller%20checkboxes,-Use%20standard%2Dsized)
- a [secondary button](https://design-system.service.gov.uk/components/button/#:~:text=Nunjucks-,Secondary%20buttons,-Use%20secondary%20buttons) to allow the users to select multiple filters before submitting
- a search [input with suffix](https://design-system.service.gov.uk/components/text-input/#:~:text=a%20phone%20number-,Prefixes%20and%20suffixes,-Use%20prefixes%20and)
- a 1px border

We’ve included the search for when people contact the team about something that’s in progress. We’ve placed the search input at the bottom of the panel because it is more likely that users will select a type of task and work through in chronological order, so will use the filters more often. For example, we know that 2 support staff will work through up to 800 de-duplication tasks a day during busy times and only work on this task. 

In future, we may need to add more filters or categories of filters if there are more support tasks.

## Failed verification details

The support user is shown any information that was provided by GOV.UK One Login. In this case, it is the authenticated email address.

An ‘additional’ section shows information that the user has inputted. This includes:
- name
- previous names (optional)
- date of birth
- National Insurance number (optional)
- teacher reference number (optional)
- proof of identity

### Suggested matches

We show any potential matches with teaching records. Usually, there would only be one. We match based on the email address. We want to do more ‘fuzzy’ matching if close variants of any of the personal details appear to be similar.

The support staff chooses from yes/no radio buttons whether to connect the GOV.UK One Login with the suggested teaching record.

If they select ‘no’, a reveal gives a link to find a record in a new tab and an optional input for a TRN. This is so that they can use the information and manually search the TRS and choose to connect with a record.

If there are multiple suggested matches, they are shown with options to choose between them.

If there are no suggested matches, there is the option to search and add a TRN, or continue without connecting.

### Connecting

The support user will either confirm the connected record, or select a reason for not connecting. The reasons are:
- request and proof don’t match
- wrong type of document
- image quality
- no teaching record with these details

An email is generated to the user to say either they can now access the service with their GOV.UK One Login or the reason for not connecting, advising they need to try again.

### Change history

If we connect the record, we’ll add a change history event to the teaching record to say it’s been connected with a GOV.UK One Login. 

We include a details reveal with the email address that was connected. This is because we currently only have 1 email field in the teaching record which will be the latest one. We plan to add fields for additional email addresses, because users may have different ones for signing in and contact.

### Components for displaying details

Throughout these screens we use:
- a summary list for information that has been submitted by a user but is not a record in TRS
- a summary card for a set of information that forms a record in TRS

This makes it clear which information is being reviewed, and which relates to a teaching record.