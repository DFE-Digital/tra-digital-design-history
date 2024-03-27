---
title: Supporting when we can't connect a GOV.UK One Login to a teaching record
date: 2024-03-27
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

## Overview

There are 2 scenarios when people using GOV.UK One Login to access their teaching qualifications may generate a support task:
- they’re [unable to verify their identity]()
- we’re unable to connect with a teaching record

[add link to other TRS support post]: #

## Unable to connect

If we can’t connect the details from GOV.UK One Login with a teaching record, we’ll ask the user to input their National Insurance number. If that doesn’t work we ask for their TRN. If we still can’t connect, we’ll use the information to generate a support task.

This could happen because of:
- a missing National Insurance number, where the teaching record doesn’t have one to match with
- a partial match, where some details match but some don’t, for example there are different versions of a name

### Support task

The support user is shown any information that was provided by GOV.UK One Login. In this case, it is an authenticated email address and their verified:
- name
- any previous names
- date of birth

An ‘additional’ section shows information that the user has inputted. This includes:
- National Insurance number (optional)
- teacher reference number (optional)

They then confirm the connected record, or select a reason for not connecting. 

The user is emailed to say either they can now access their record, or need to try again.

### Change history

If the record is connected we add a change history event to record this and the email address that was used.