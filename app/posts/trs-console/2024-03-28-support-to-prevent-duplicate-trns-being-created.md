---
title: Support to prevent duplicate TRNs being created
date: 2024-03-28
description: Checking potential duplications before a new TRN is created.
screenshots:
  items:
    - text: Support tasks landing page
      src: support-tasks-landing-page.png
    - text: Check if the request is a duplicate
      src: check-duplicate.png
    - text: Check a request where there is a teaching restriction
      src: check-alert.png
    - text: Confirm allocating a new TRN
      src: confirm-new-trn.png
    - text: Choose which details to merge
      src: choose-details.png
    - text: Request and record successfully merged
      src: record-merged.png
---

## Overview

There are 3 ways that TRNs can be generated:
- an initial teacher training provider requests one for a new teacher (Register trainee teachers)
- an international teacher applies for QTS (Apply for QTS in England)
- someone starts employment and is registered for pensions

These use different sets of numbers and synchronise data daily to try and avoid duplicates. However, it is possible that a TRN can be requested for someone who already has one.

It’s mostly around the start of the academic year. For example, there may be an overlap between when someone is registered on a training course and by a new employer for their pension.

There is a small team of around 2 support staff who focus on this task full time when they do it. There can be approximately 5-6,000 of these tasks a year.

### Avoiding duplication

When a request is made in the system for a new TRN, we check if the details provided already exist in a teaching record.

If there is a possible match, the new TRN request goes in to a ‘pending bucket’, and a task is generated to check if it is a duplicate.

If it is not a duplicate, the new TRN request is authorised.

If it is a duplicate, the information from the TRN request and the existing teaching record may be merged or chosen between.

## Support task

The task shows the data from the new TRN request in summary list. We’ve used this pattern across support tasks for information that has been submitted by someone but is not a record.

We display any possible matches in a summary card. We’ve used this pattern to signify groups of data that are in a record.

The support user chooses between:
- use the existing TRN
- allocate a new TRN

Allocating a new TRN means it is not a duplicate and the request is granted. Using the existing TRN means that they are duplicates, and the support user will choose which information to keep.

If there are multiple possible matches we display them and the user can choose which one to use.

### Alerts

If there is a restriction on the record, such as a prohibition order, there is a notification banner highlighting this. This so the task can be sent to the teacher misconduct team who will review it.

### Merge personal details

If the support user selects to use the existing TRN, they will need to choose which information to keep.

We only show any details which are different between the request and the record, for example if one field is blank or they contain different data.

If there are no differences, this screen is skipped.

We use [inline small radio buttons](https://design-system.service.gov.uk/components/radios/#:~:text=in%20services.-,Smaller%20radios,-Use%20standard%2Dsized) where there is a choice because it is a frequent use interface and we don’t need to make them more prominent. 

Radio buttons are used to choose between sources of data. For previous names, we use checkboxes because users may want to keep both sources. We need to test if this is confusing and if we need it for any other fields where users may need to use both sources. 

We might think about splitting this into one screen with radios for either/or choices and another screen with checkboxes for either/or/both/neither choices, to avoid mixing input types. However, it is likely that there will be few fields to choose from.

We use a 3 column table to layout the inputs and compare between new and existing data. There is an option separated by an input-border colour to select all. The ‘select all’ has no validation so it can be skipped.

At this point, the de-duplication process reports the potential duplicate when personal details are entered and before a new record is created, so we should not have ITT or other qualifications data to check.

### Check answers

We show the new record in a summary card to show how it will appear with the selected options.

For now, the change links return to the previous screen. As we scale the product it may be that we need to include something to manually change fields, for example if both sources had different spellings of a name that were slightly wrong. Support users can already do this through the ‘make manual PII changes’ flow after completing a de-duplication task.

### Change history

If the request and record is merged, we add a change history event to say they were merged. If any data is deleted in this action, we include a reveal for ‘previous data’. This is how we’ve established the change history to be able to resolve mistakes.
