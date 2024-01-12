---
title: Deleting mandatory qualifications
date: 2024-01-11
description: Letting users remove a mandatory qualification for teaching pupils with sensory impairments.
screenshots:
  items:
    - text: Qualification summary card with delete link
      src: summary-card-delete.png

    - text: Question page asking why the mandatory qualification is being deleted
      src: delete-question-page.png

    - text: File upload component revealed if the user says they want to upload evidence
      src: delete-upload-evidence.png

    - text: Check answers screen asking the user to confirm that they want to delete the qualification
      src: delete-confirm.png

    - text: Success message after the qualification has been deleted
      src: delete-success.png

    - text: Different states for the file upload including error messages
      src: delete-evidence-states.png
---

Users sometimes need to remove a mandatory qualification from a teacher’s record. For example a training provider may have sent inaccurate data or a user may have added the qualification by mistake.

In the Microsoft Dynamics system which is being replaced, users deal with this by marking a qualification as inactive.

Doing this does not remove the qualification but hides it from users of other services, for example the one used by employers to [check a teacher’s record](/check-the-record-of-a-teacher).

This is not just the case for qualifications. Most types of data can be marked as inactive.

As a result, the database contains a lot of data which has been kept for a long time even though it’s known to be inaccurate.

Users typically add a note explaining why they’ve marked something as inactive. These notes are displayed in an unstructured list of all notes associated with a record.

If there are a lot of notes it can take time for a user to work out why a piece of data has been made inactive. If there’s no relevant note then it may be impossible to know why it’s inactive.

## What will happen to deleted data

In the TRS console we will not allow users to mark data as inactive. Instead they will be able to delete data.

We still need to keep this data for quality control and auditing. TRA staff sometimes receive enquiries about changes a long time after they were made.

Deleted data will not be included in the teacher’s record within the TRS console. The fact that data was deleted will be recorded in a change history which the user can access.

The change history will also show the reason for the deletion. This will be directly associated with the deletion rather than being stored in a separate note.

Doing this will provide more structure than the old notes feature and make it easier to see changes over time.

The change history may also show what data has been deleted. We need to decide whether all users will be able to see all deleted data or whether there will be rules about this.

## How users can delete a mandatory qualification

A mandatory qualification appears as a summary card in the qualifications tab of a teacher’s record. We’ve added a delete link to this summary card.

If a user clicks the delete link, they‘re taken to a page where they’re asked to choose a reason for deleting the qualification.

This is to help make sure that users only delete qualifications when there’s an appropriate reason for doing so. It will also help users to understand the contents of a teacher’s record if they need to check it later.

We’ve worked with users of the service to create a list of reasons. These are:

- added in error
- provider request
- unable to confirm the data is correct
- another reason

There’s also a text box in which the user must add more detail about the reason for deleting.

This allows flexibility for different situations and allows users to provide context. For example, a user might want to explain why a training provider asked them to delete the qualification.

The user can choose to upload evidence for why the qualification needs to be deleted. For example they could upload an email sent by a training provider.

## Further considerations

If users often need to choose ‘another reason’ for deletion, we may add more reasons to the list. We would like them to choose a specific reason where possible.

If users do not always need to give more detail, we may make it optional to add it. We do not want users to add unhelpful detail simply to have something to put in the compulsory field.

We also need to design the change history. This will include deciding what we show when a qualification is deleted and who can see it.
