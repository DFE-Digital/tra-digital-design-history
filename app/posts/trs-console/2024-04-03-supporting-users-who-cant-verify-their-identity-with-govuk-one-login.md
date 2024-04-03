---
title: Supporting users who cannot verify their identity with GOV.UK One Login
date: 2024-04-03
description: Creating a way for support staff to manually verify users’ identities.
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

We’re working to [use GOV.UK One Login with some TRA services](/qualifications-service/using-govuk-one-login-with-tra-online-services/), starting with Access your teaching qualifications.

When [signing in for the first time using GOV.UK One Login](/qualifications-service/signing-in-for-the-first-time-using-govuk-one-login/) users need to:

- create a GOV.UK One Login - if they do not have one already
- verify their identity - if they have not done it already
- give additional information to connect their teaching record - if we cannot connect it automatically

GOV.UK One Login offers [support for users who have problems using the service](https://www.sign-in.service.gov.uk/support).

However it’s still possible that:

- a user cannot verify their identity, for example if they select ‘no’ for all the identity verification options
- we cannot match a GOV.UK One Login with a teaching record, even if the user’s identity has been verified

There’s another design history entry for [supporting users when we cannot connect a GOV.UK One Login to a teaching record](/qualifications-service/supporting-users-when-we-cannot-connect-a-govuk-one-login-to-a-record).

## What happens when a user cannot verify their identity

If the user hasn’t verified their identity at the end of the GOV.UK One Login journey then they’re passed back to our service.

We’re only given their authenticated email address.

The user will not be able to access our service. We require a user’s identity to be verified before we connect their GOV.UK One Login to their teaching record.

We therefore need to [offer users another way to prove their identity](https://www.sign-in.service.gov.uk/about/checking-users-identities/evidence-types#:~:text=Users%20who%20cannot%20prove%20their%20identity).

We do this by asking users to:

- give additional information
- upload evidence of their identity

This is described in the [design history entry about signing in for the first time](/qualifications-service/signing-in-for-the-first-time-using-govuk-one-login#if-the-user-cannot-verify-their-identity). It allows us to collect the information which support staff need to:

- manually verify the user’s identity
- connect their GOV.UK One Login to a teaching record

We use the information entered to generate a support task.

## How support tasks appear in the TRS console

We’ve redesigned the [manage change requests feature](https://tra-digital-design-history.herokuapp.com/trs-console/managing-change-requests/). It’s now called ‘support tasks’.

This is because there will now be tasks for:

- change requests
- problems with GOV.UK One Login
- [preventing duplicate TRNs from being created](/trs-console/preventing-duplicate-teacher-reference-numbers-from-being-created)

A list of support tasks is included in a table in a three-quarters page width column.

For the initial design, we’ve used the reference format used by the Dynamics service which is being replaced by the TRS console. It uses references such as ‘CAS-01006-F4Q3Z7’.

We will not use this format in the live service but the new format had not been defined when we created the initial design.

We’ve linked to each task from its reference number as that is how it was done on the manage change requests page. We’d like to consider whether this is the best approach.

### Sorting and filtering

We’ve added the option to sort by:

- date when a task was created
- task type

The default view is sorted with the oldest first.

We are not sure that users will need to sort by task type since they’ll also be able to filter by it.

We’ve added a filter panel in a one-quarter page width column. It uses:

- [smaller checkboxes](https://design-system.service.gov.uk/components/checkboxes/#:~:text=in%20services.-,Smaller%20checkboxes,-Use%20standard%2Dsized)
- a [secondary button](https://design-system.service.gov.uk/components/button/#:~:text=Nunjucks-,Secondary%20buttons,-Use%20secondary%20buttons) to allow support users to select multiple filters before submitting
- a search [input with suffix](https://design-system.service.gov.uk/components/text-input/#:~:text=a%20phone%20number-,Prefixes%20and%20suffixes,-Use%20prefixes%20and)
- a one pixel border

We’ve included the search input in case someone contacts the support team about a task that’s in progress. It will make it easier to find a specific task.

We expect that users will more often use the filters so that they can select a type of task and work through in chronological order.

For example, we know that 2 members of support staff usually work through up to 800 de-duplication tasks each day at the start of an academic year. They will not want to see other types of tasks.

In future, we may need to add more filters or categories of filters if there are more support tasks.

We may also be able create more user roles so that we show only the relevant tasks to a user.

## Details of the user who failed identity verification

When they click through to a failed identity verification task, the support user is shown the email address that was provided by GOV.UK One Login.

An ‘additional’ section shows information that the user entered or uploaded. This includes:

- name
- previous names - if the user gave any
- date of birth
- National Insurance number - if the user gave it
- teacher reference number - if the user gave it
- proof of identity

### Potential matches

We show any teaching records which are a potential match based on the email address.

#### One potential match

Usually there is only one potential match. In future we may do more ‘fuzzy’ matching if close variants of any of the personal details appear to be similar.

The support user must choose whether to connect the GOV.UK One Login with the suggested teaching record.

If they select ‘no’ then a reveal shows an optional TRN input and a link to find another record in a new tab.

The support user can find a matching record then return to the task to enter the TRN.

#### Multiple potential matches

If there are multiple suggested matches then they’re shown with an option to choose between them.

#### No potential matches

If there are no suggested matches then the user can search for a record in another tab and enter the TRN.

### Choosing whether to connect a record to the GOV.UK One Login

The support user can either:

- confirm that they want to connect a record - either a potential match or a record which they’ve found and entered manually
- choose a reason for not connecting a record

The reasons for not connecting are:

- request and proof do not match
- wrong type of document
- image quality
- no teaching record with these details

An email is sent to the user to either:

- tell them that they can now access the service with their GOV.UK One Login
- give them the reason for not connecting and telling them that they can try again

We did not write the emails as part of the initial design work.

### Change history

If the support user connects a record then we add a change history event to the record. It says that the record has been connected with a GOV.UK One Login.

We include a reveal for ‘support request details’. It contains the email address of the GOV.UK One Login that was connected.

### Components for displaying details

In this task we use:

- a summary list for information that has been submitted by a user but is not a teaching record
- a summary card for a set of information that forms a teaching record

This helps to make it clear which information is being reviewed and which relates to a teaching record.
