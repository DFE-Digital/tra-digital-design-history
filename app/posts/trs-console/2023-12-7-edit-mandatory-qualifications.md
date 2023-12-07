---
title: Edit mandatory qualifications
date: 2023-12-7
description: Make changes to a mandatory qualification on a teacher's record
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

DfE users need to edit MQ data on the record if they get updated information from a training provider, so that the correct information is displayed on teacher’s records.

The design is similar to adding an MQ, but the inputs are pre filled with the current data and the user does not need to go through the whole flow.

## Confirm changes

The user is asked to confirm a change before it is submitted. In future, we may add a field here to select a reason for making the change, or a text input to a note, such as to say it was in response to an email from a training provider. This can be used for auditing and quality control. 

## Notes

In the old DQT, there is a ‘notes’ function, where users can write detail about changes they make or add extra context for internal use. However, this became bloated and unorganised so it’s not included in the MVP. We may add this as a refinement and link the input from the check and confirm page to an event in the change log. This will help to make the extra detail more structured and contextual.

## Training providers

In the edit flow, we want to allow the autocomplete input to return a full list of current and historic training providers. This will allow users to edit old data.

## Unknown results

Some fields on the record may have a “NULL” value, displayed as “Unknown”. We decided not to include an unknown option within the change screens as users should only be changing these to something that is known.

We need to make sure that there are no scenarios where users would need to change something that is known to unknown. 

## Removing qualifications

The current design doesn’t include the option to remove MQs. We have some ideas how this may work beyond the MVP and will do workshops with the stakeholders to understand how data should be deactivated, hidden or deleted and what the audit requirements will be. 