---
title: Adding mandatory qualifications
date: 2023-12-15
description: Allowing users to add a mandatory qualification for teaching pupils with sensory impairments.
screenshots:
  items:
    - text: A record with no mandatory qualifications
      src: 1-add-mq-blank.png
    - text: Add a training provider
      src: 2-add-mq-provider.png
    - text: Add a specialism
      src: 3-add-mq-specialism.png
    - text: Add the date the course started
      src: 4-add-mq-start-date.png
    - text: Add the status of the course
      src: 5-add-mq-status.png
    - text: Selecting the status as passed reveals an input for the award date
      src: 6-add-mq-status-passed-end-date.png
    - text: Check your answers
      src: 7-add-mq-check-answers.png
    - text: Success screen
      src: 8-add-mq-success.png
---

The first type of qualification included in the TRS console will be mandatory qualifications for teaching pupils with sensory impairments.

Providers of these qualifications send updates to the TRA in spreadsheets, usually once a year. Members of TRA staff then add the qualifications to the database.

## How mandatory qualifications are added in the TRS console

Users add mandatory qualifications in the qualifications tab of a teacher’s record.

It’s very uncommon for teachers to have more than one mandatory qualification. Normally a user will see the message “No mandatory qualifications” and a button allowing them to add one.

If the teacher does already have a mandatory qualification, the details will be in a summary card. The button for adding a new qualification will also be shown.

After clicking the button, the user needs to give details of:

- training provider
- specialism
- start date
- status
- end date - if the status is ‘passed’

For the initial design we’ve put each of these on its own page. This means that a user only has to focus on one piece of information at a time.

### Training provider

The user enters the training provider using an [accessible autocomplete](https://github.com/alphagov/accessible-autocomplete). It includes the 5 current and 9 former training providers.

This is more flexible than restricting users to choosing a current provider. We know that users occasionally need to add an old qualification.

However it means there’s a risk that a user will accidentally add a former provider for a new qualification.

Since there are only 14 providers in total, we could have let users select them with radio buttons.

However, in other parts of the service the list of training providers will be much longer. We decided that we’ll consistently use the accessible autocomplete for lists of training providers.

We plan to store the list of current providers and former providers in a [central DfE resource](https://github.com/DFE-Digital/dfe-reference-data).

#### Problems with provider data

Although there are only 14 current and previous providers, in the DQT database there are 27 provider names.

This is because the provider name field is sometimes used to give additional information.

For example, one provider name is “BPhil in Multi-Sensory Impairment and Deafblindness, University of Birmingham, School of Education”.

We do not record course name and level for most mandatory qualifications. We therefore intend to only show the name of the provider, which will help to keep data simple and consistent.

### Specialism

The user must use radio buttons to select from 3 specialisms:

- hearing impairment
- multi sensory impairment
- vision impairment

### Start date

We use the [GDS date input component](https://design-system.service.gov.uk/components/date-input/) for the start date of the course.

### Status

We collect a status so that we know:

- which people are qualified to teach pupils with sensory impairments
- how many people failed to qualify or are in other stages of training

The user chooses a status from a set of radio buttons. The possible statuses are:

- deferred
- extended, which is when a teacher has been given extra time to complete the course
- failed
- in progress
- passed
- withdrawn

We’ve added some statuses to those available in the Microsoft Dynamics system which is being replaced by the TRS console. The TRA has decided to start reporting on the numbers of people who have failed, deferred or extended courses.

We’ve also changed the name of the field from ‘result’ to ‘status’. We did this because, for example, ‘in progress’ is not a result.

#### Active and inactive data

In the Dynamics interface, the word ‘status’ is used to indicate whether data is active or inactive.

Data is never deleted. Instead it’s made inactive, which means that:

- it’s shown to DfE and TRA staff
- it is not shown to schools or teachers

Data can be made inactive for various reasons. This means that it can be impossible to know why a particular piece of data is inactive. It also means that there is a lot of data in the database of qualified teachers which is not relevant and will never be needed.

We will not have inactive data in the new teaching record system database. Instead users will be able to delete data and the deletion will be recorded in a change log.

Since we do not need to have an active or inactive status, we can use the word status in a different way in the TRS console.

### End date

We only collect an end date if the status is ‘passed’. We’ve used a conditional reveal to show a date input if this option is selected.

We could use the same pattern in future to ask for an expected end date for the other statuses. At the moment we do not ask providers to give this information.

### Check and confirm

Once the user has entered the qualification status, they can review the data they’ve entered. There’s a change link for each item of data, allowing the user to fix anything which is incorrect.

After they confirm that the data is correct, the user returns to the teacher’s qualifications tab. We display a success banner saying “Mandatory qualifiction added”.

## Further considerations

Most providers only offer courses in one specialism. We could choose to only display the valid options for the selected provider.

However, the courses offered change over time and occasionally users need to add old qualifications. We’d therefore need to keep a record of which provider offered each specialism and the dates when they offered it.

This is something we may do in future to help avoid data entry mistakes.
