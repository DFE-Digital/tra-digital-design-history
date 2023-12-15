---
title: Viewing mandatory qualifications
date: 2023-12-14
description: Letting users see whether a teacher has a mandatory qualification for teaching pupils with sensory impairments.
screenshots:
  items:
    - text: Record with no mandatory qualifications
      src: record-no-mq.png
    - text: Record with a mandatory qualification
      src: record-with-mq.png
    - text: Record with a mandatory qualification with incomplete data
      src: mq-missing-data.png
---

Users of the TRS console will be able to search for a record and view data including:

- teaching qualifications
- whether someone is prevented from teaching, for example by a prohibition order

Depending on what permissions they have, users may also be able to add, edit and delete data.

The first part of the TRS console to be built will handle mandatory qualifications. These are required for teaching pupils with hearing, visual or multi sensory impairments.

There are around 14,000 records with a mandatory qualification.

The list of training providers changed in September 2023 but will remain the same for at least 3 years. There are 5 providers offering mandatory qualifications.

## Navigating within the service

Since this is the first type of data we’re including in the TRS console, we needed to make decisions about the basic design of the service.

For example we’ve used the [sub navigation bar](https://design-patterns.service.justice.gov.uk/components/sub-navigation) from the Ministry of Justice design system.

This is consistent with the design of the [access your teaching qualifications](https://tra-digital-design-history.herokuapp.com/qualifications-service) and [register trainee teachers](https://becoming-a-teacher.design-history.education.gov.uk/register-trainee-teachers) services.

## Showing qualification details

If the record has no mandatory qualifications, we show text which says so. A green primary button lets the user add a mandatory qualification.

If the record has a mandatory qualification then we use a summary card to display the fields, which are:

- training provider
- specialism
- start date
- status
- end date

The possible statuses are:

- deferred
- extended, which is when a teacher has been given extra time to complete the course
- failed
- in progress
- passed
- withdrawn

We only collect an end date if the status of the course is passed. For any other status we do not show the end date field.

Each field has a change link to edit the data.

It’s possible for a teacher to have more than one mandatory qualification, so we show a primary button to allow the user to add another.

## Missing data

Some data is incomplete or is of low quality. For example, 67% of the data either:

- does not have a provider name
- has other information in the provider field, such as a description of the course

In cases where the data has a value of null or is missing, we’ll display “None” or “Unknown”.

We’ll work with people who use the service to improve the quality of data. For example we’ll use the centralised [DfE reference data repository](https://github.com/DFE-Digital/dfe-reference-data) to store provider names and decide how to migrate data that doesn’t fit the standard.

## Further considerations

We’ll need to consider:

- deleting mandatory qualifications
- showing other qualification types
- adding permissions

### Deleting mandatory qualifications

In this initial design we did not use a summary card action. This is something which affects the whole piece of data, for example to delete a qualification. It appears in the title bar of a summary card.

We need to decide what needs to be recorded for auditing purposes before we can design the deletion journey.

### Showing other qualification types

For now, the only qualification type in the TRS console will be mandatory qualifications. When we add other types we’ll need to design a way for the user to choose what type of qualification to add.

### Adding permissions

Initially the service will have a very small number of users. We’ll allow them to view, add, edit and delete mandatory qualifications.

As we release the service to more users, we’ll need to add permissions so that they can only take appropriate actions within the service.
