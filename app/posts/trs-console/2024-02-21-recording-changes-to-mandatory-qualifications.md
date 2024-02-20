---
title: Recording changes to mandatory qualifications
date: 2023-02-21
description: Showing a change history for a record so that users can see what changed and why it changed.
screenshots:
  items:
    - text: Change history timeline
      src: MQ-change-history.png
---

Sometimes users need to know what has changed in a record and why it changed, for example:

- to answer enquiries or complaints
- for quality control and auditing

## How the old service records changes

Each record in the old Microsoft Dynamics system has a section for notes. Users add notes for many reasons, including to give context for a change.

The notes in a record are not structured, so there’s no connection between a note and a change.

If a record has a lot of notes then it can be hard for users to understand what happened.

## Recording changes in the new service

We will not include unstructured notes in the new TRS console.

Instead we’ll allow users to add information as part of carrying out an action. For example, if a user deletes a mandatory qualification then they:

- must select a reason from a list
- can add additional detals about the reason in a text input
- can upload evidence for why the change was made, such as a PDF file

We may decide not to ask for reasons for some types of change. We want to make it easy to understand records by only including information which is useful.

## How we show the change history

The reasons for a change are stored as part of an event in the database. This event appears in a new change history tab which we’ve added to records.

In this tab we use a [timeline component](https://design-patterns.service.justice.gov.uk/components/timeline/) to display events with the most recent first. This makes it easier to find an event and understand how a record has changed over time.

We’ll initially show events for:

- adding a mandatory qualification
- editing a mandatory qualification
- deleting a mandatory qualification

We’ll need to show more events when we add more features to the TRS console.

### Adding a mandatory qualification

The event created when a mandatory qualification is added shows:

- who added the qualification
- when they added it

We do not ask users to enter a reason for adding a mandatory qualification.

This type of event does not show the details of the qualification which was added because:

- if they have not been changed since being added then these details will appear in the record
- if they have been changed then these details will appear in the event created when the qualification was edited

### Editing a mandatory qualification

The event created when a mandatory qualification is edited shows:

- who changed the qualification
- when they changed it
- the details of the qualification before the change
- the reason for the change, including any additional details
- a link to the evidence for why the change was made

The event does not show the new details for the qualification because that will appear in the record.

### Deleting a mandatory qualification

The event created when a mandatory qualification is deleted shows:

- who changed the qualification
- when they changed it
- the data which was deleted
- the reason for the deletion, including any additional details
- a link to the evidence for why the qualification was deleted
