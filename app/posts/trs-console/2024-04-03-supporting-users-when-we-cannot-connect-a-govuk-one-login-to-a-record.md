---
title: Supporting users when we cannot connect a GOV.UK One Login to a teaching record
date: 2024-04-03
description: Creating a way for support staff to manually connect a teaching record.
screenshots:
  items:
    - text: Support tasks landing page
      src: support-tasks-landing-page.png
    - text: Details about the support request for unable to connect
      src: unable-to-connect-details.png
    - text: Confirmation banner for record not connected
      src: record-not-connected.png

---

People [signing in to a TRA service for the first time using GOV.UK One Login](/qualifications-service/signing-in-for-the-first-time-using-govuk-one-login/) may generate a support task because:

- they’re unable to verify their identity
- we’re unable to connect their GOV.UK One Login with a teaching record

There's another design history entry for [supporting users who cannot verify their identity with GOV.UK One Login](/trs-console/supporting-users-who-cant-verify-their-identity-with-govuk-one-login). It includes details about the design of the list of support tasks, including its sort and filter options.

## Why we may be unable to connect a teaching record

If we cannot automatically match a user’s GOV.UK One Login with a teaching record then we ask the user to enter their National Insurance number.

If we still cannot match with a teaching record then we ask for their teacher reference number (TRN).

If we still cannot find a match then we use the information the user has already entered to generate a support task.

This could happen for various reasons. For example:

- the teaching record may not include a National Insurance number, so it cannot be matched to a number entered by the user
- the user may say that they cannot enter either an National Insurance number or a TRN

## What the support user needs to do

When they click through to the support task, the support user is shown the information that was provided by GOV.UK One Login. This is the user’s:

- name
- email address
- any previous names
- date of birth

An ‘additional’ section shows information that the user entered. This includes:

- National Insurance number
- teacher reference number

The support user needs to either:

- confirm the connected record
- choose a reason for not connecting

Details of how a support user makes this decision are in the design history entry about [supporting users who cannot verify their identity with GOV.UK One Login](/trs-console/supporting-users-who-cant-verify-their-identity-with-govuk-one-login).

After the support user has made a decision, the user is emailed to say either:

- they can now access their record using their GOV.UK One Login
- they need to try again

## Updating the change history

If the record is connected we add a change history event to record this and the email address that was used.
