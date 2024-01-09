---
title: Editing mandatory qualifications
date: 2024-01-09
description: Letting users change details of a mandatory qualification for teaching pupils with sensory impairments.
screenshots:
  items:
    - text: A record with a summary card showing a mandatory qualification with change links to edit the data in each field
      src: 1-edit-mq-record.png
    - text: Editing a training provider shows the field populated with the existing data
      src: 2-edit-mq-provider.png
    - text: Changing the status from passed to something else will replace the end date with "none"
      src: 3-edit-mq-status-confirm.png
    - text: A confirmation screen showing the current and new data before submiting the change
      src: 4-edit-mq-confirm.png
    - text: Success screen after making a change
      src: 5-edit-mq-success.png
---

Training providers sometimes provide updates about a teacher’s mandatory qualification for teaching pupils with sensory impairments. For example, a teacher who had deferred their course may now have completed it.

This means that users of the TRS console need to be able edit the details of a teacher’s mandatory qualifications.

The design for this is similar to [adding a mandatory qualification](/adding-mandatory-qualifications). The differences are that:

- the inputs are pre filled with the current data
- the user does not need to go through the whole flow

In the edit flow, we want to allow the autocomplete input to return a full list of current and historic training providers. This will allow users to edit old data.

## Further considerations

### Giving a reason for the change

The user is asked to confirm a change before it is submitted. We may add a field here to give a reason for making the change, such as to say that a training provider requested the change.

The user could:

- choose a reason from a list
- add text to explain why the change was made

Adding a reason may be useful if there is a query about the change. It would mean that DfE staff would not need to search through emails or other files to find the reason.

### Adding notes

Users can add notes in the Microsoft Dynamics system which is being replaced by the TRS console.

In these notes, users can give detail about changes they make or add extra context. Since notes can be added in most parts of the system, they’ve become bloated and disorganised.

We will not include the ability to add notes in the initial designs for the mandatory qualifications in the TRS console.

...We may add them later and link the input from the check and confirm page to an event in the change log. This will help to make the extra detail more structured and contextual.

## Unknown results

Some fields on the record may have a “NULL” value, displayed as “Unknown”. We decided not to include an unknown option within the change screens as users should only be changing these to something that is known.

We need to make sure that there are no scenarios where users would need to change something that is known to unknown.

## Removing qualifications

The current design doesn’t include the option to remove MQs. We have some ideas how this may work beyond the MVP and will do workshops with the stakeholders to understand how data should be deactivated, hidden or deleted and what the audit requirements will be.
