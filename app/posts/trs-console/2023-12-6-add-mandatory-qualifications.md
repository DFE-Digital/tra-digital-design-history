---
title: Add mandatory qualifications
date: 2023-12-6
description: The flow for adding a mandatory qualification to a teacher's record
screenshots:
  items:
    - text: A record with no mandatory qualifications
      src: 1-add-mq-blank.png
   
    - text: Add a training provider
      src: 2-add-mq-provider.png
   
    - text: Add a specialism
      src: 3-add-mq-specialism

    - text: Add the date the course started
      src: 4-add-mq-start-date

    - text: Add the status of the course
      src: 5-add-mq-status

    - text: Selecting the status as passed reveals an input for the award date
      src: 6-add-mq-status-passed-end-date
    
    - text: Check your answers
      src: 7-add-mq-check-answers

    - text: Success screen
      src: 8-add-mq-success
--- 

DfE users typically get information from training providers of mandatory qualifications (MQs) annually which updates them on who is studying and what their status is. It is very uncommon for teachers to have more than one MQ, so the typical starting point is the blank screen.

## Training providers

The first field to input is the training provider. This uses an [accessible autocomplete] (https://github.com/alphagov/accessible-autocomplete). This allows us to use a single source of truth for a list of providers and is scalable.

There are currently only five providers of MQs. There are nine historic providers. We are proposing storing a list of current providers and a list of historic providers in a [central DfE resource] (https://github.com/DFE-Digital/dfe-reference-data), with the add MQ action using current data and editing to use both lists. This is to help keep new data good quality.

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

We use the [GDS date input component] (https://design-system.service.gov.uk/components/date-input/) for the start date of the course. This is mandatory for all courses.

## Status

We collect a status to understand how many people have qualified and how many people are in other stages of training for MQs. 

We only collect an end date if the status is “passed”. We’ve used a conditional reveal to show a date input if this option is selected. We could use the same pattern in future to ask for an expected end date for the other results, if the service decide to monitor this.

The service have decided to start monitoring more detail about numbers of people who have failed, deferred or extended courses so they can report on this. We added some extra options to allow this.

We changed the word ‘result’ to ‘status’. This is more accurate because some of the options are not completed results. It is focused on the information that is being presented to other services. In the old Dynamics interface, status meant if data was active or inactive, but we’re not replicating that functionality.

## Check and confirm

The user is asked to check their inputs are correct. Then the qualification is displayed on the record with a success message.