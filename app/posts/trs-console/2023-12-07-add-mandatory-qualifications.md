---
title: Add mandatory qualifications
date: 2023-12-07
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

The first type of qualification in the TRS console will be mandatory qualifications for teaching pupils with sensory impairment.

Providers of these qualifications send updates to the TRA in spreadsheets, usually once a year. Members of TRA staff then add the qualification to the database.

## How mandatory qualifications will be added to the TRS console

It is very uncommon for teachers to have more than one mandatory qualification.

This means that normally a user will see the message “No mandatory qualifications” and a button allowing them to add one.

After clicking the button, users need to give details of:

- training provider
- specialism
- start date
- status

For the initial design we’ve put each of these on its own page.

## Training provider

The user enters the training provider using an [accessible autocomplete](https://github.com/alphagov/accessible-autocomplete).

There are currently only 5 current training providers and 9 former providers so we could have used radio buttons.

However, in other parts of the service the list of training providers will be much longer. We decided that we’ll consistently use the accessible autocomplete.

We’re proposing to store the list of current providers and former providers in a [central DfE resource](https://github.com/DFE-Digital/dfe-reference-data). with the add MQ action using current data and editing to use both lists. This is to help keep new data good quality.

We could have used radio buttons, but the autocomplete component allows more flexibility with the list of values and we can use the same design pattern for future features, such as initial teacher training which has nearly 200 providers.

### Old data

In the old DQT database there are 27 provider names, because some used this field to give multiple names for the same institution with detail about something else as well. For example, there are several names for the University of Birmingham. Some of them include the title and level of the course within the provider name, such as “BPhil in Multi-Sensory Impairment and Deafblindness, University of Birmingham, School of Education”. We don’t record this course level for all providers, and only display the specialism so we’re proposing to just use the name of the establishment. This will help to keep data consistent and simpler.

## Specialism

There are only three specialisms:

- hearing impairment
- multi sensory impairment
- vision impairment

We provide this input as radio buttons. We know that most providers only offer one of these, so we could only display the valid options for the selected provider. However, these change over time and we’d need to consider which provider offered which type of training in the past. This is something we may add as a refinement in future to help avoid data entry mistakes.

## Start date

We use the [GDS date input component](https://design-system.service.gov.uk/components/date-input/) for the start date of the course. This is mandatory for all courses.

## Status

We collect a status to understand how many people have qualified and how many people are in other stages of training for MQs.

We only collect an end date if the status is “passed”. We’ve used a conditional reveal to show a date input if this option is selected. We could use the same pattern in future to ask for an expected end date for the other results, if the service decide to monitor this.

The service have decided to start monitoring more detail about numbers of people who have failed, deferred or extended courses so they can report on this. We added some extra options to allow this.

We changed the word ‘result’ to ‘status’. This is more accurate because some of the options are not completed results. It is focused on the information that is being presented to other services. In the old Dynamics interface, status meant if data was active or inactive, but we’re not replicating that functionality.

## Check and confirm

Once the user has entered the qualification status, they can review the data they’ve entered. There’s a change link for each item of data, allowing the user to fix anything which is incorrect.

After they confirm that the data is correct, the user returns to the teacher’s qualifications page. We display a success banner saying “Mandatory qualifiction added”.