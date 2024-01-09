---
title: Editing mandatory qualifications
date: 2024-01-09
description: Letting users change details of a mandatory qualification for teaching pupils with sensory impairments.
screenshots:
  items:
    - text: Record showing a mandatory qualification with change links for each field
      src: 1-edit-mq-record.png
    - text: Training provider input showing the existing data
      src: 2-edit-mq-provider.png
    - text: Check details page
      src: 4-edit-mq-confirm.png
    - text: Check details page when changing the status from ‘passed’
      src: 3-edit-mq-status-confirm.png
    - text: Success alert after confirming a change
      src: 5-edit-mq-success.png
---

Users of the TRS console may need to edit the details of a teacher’s mandatory qualifications, for example to:

- fix a mistake
- change the status of a qualification following an update from the training provider

We’ve designed a way for users to do this.

## How it works

This design is very similar to that for [adding a mandatory qualification](/trs-console/adding-mandatory-qualifications).

Details of the teacher’s mandatory qualifications appear in the qualifications section of their record. Each field has a change link.

When the user clicks a change link they’re taken to a page where information can be entered for the relevant field.

The current information is already entered. For example, if the training provider is the University of Birmingham then that will appear in the page’s accessible autocomplete input.

The user can either:

- change the information on the page then click the continue button
- click a link to cancel the change and return to the teacher’s record

If they click the continue button, they’re taken to a check details page where they can confirm the change. They do not need to go through the other pages of information, as they would if they were adding a new mandatory qualification.

After the user confirms the change, they’re taken back to the qualifications page of the teacher’s record. An alert tells them that the mandatory qualification has been changed.

### Changing status to or from ‘passed’

If the user changes the status of a qualification to ‘passed’, they’ll need to enter an end date for the course.

If the user changes the status from ‘passed’ to something else, the end date will be changed to ‘None’.

In both cases the check details will show the status and end date changes.

## Further considerations

We expect that we’ll need to display a log of changes to a teacher’s mandatory qualifications.

We’ll consider allowing users to:

- give a reason for the change
- add notes
- remove qualifications

We may also change the way we deal with fields which have missing data.

### Displaying a change log

We know that users sometimes need to see what changes have been made to a teacher’s record.

We intend to create a change log for each teacher’s record. It will indicate that a mandatory qualification has been changed.

### Giving a reason for the change

We may add a way for the user to give a reason for making the change, such as to say that a training provider requested it.

We could ask the user to:

- choose a reason from a list
- add text to explain why the change was made

Adding a reason may be useful if there is a query about the change later. It would mean that members of staff would not need to search through emails or other files to find the reason.

### Adding notes

Users can add notes in most parts of the Microsoft Dynamics system which is being replaced by the TRS console. This includes adding notes about a mandatory qualification.

TRA staff have processes which require them to add notes, such as when they make a change. They can also add notes to provide other context.

The notes in the Microsoft Dynamics system can be hard to follow, partly because they can be added in so many parts of the system. We intend to allow notes in fewer parts of the TRS console.

We hope that if we allow users to give a reason for a change to mandatory qualifications then they will not also need to add a note.

If we find that users do need to be able to add other notes, we’ll try to make them more structured than in the Microsoft Dynamics system. For example we could make sure that every note is linked to an event in the change log.

## Removing qualifications

The current design does not include a way to remove a mandatory qualification.

We need to do more work with colleagues in the TRA to understand how data should be deactivated, hidden or deleted. We also need to find out more about any audit requirements.

## Dealing with missing data

Some fields in the record may have a value of ‘NULL’ in the database. We display this as ‘Unknown’ in the teacher’s record.

We’ve decided not to allow users to change a field’s value to ‘Unknown’. We need to make sure that there are no situations where a user would need to do this.
