---
title: View mandatory qualifications
date: 2023-12-6
description: View a teacher's record which has a mandatory qualification for teaching children with sensory impairments
screenshots:
  items:
    - text: A record with no mandatory qualifications
      src: record-no-mq.png
   
    - text: A record with a mandatory qualification
      src: record-with-mq.png
   
    - text: A record with a mandatory qualification with incomplete data
      src: mq-missing-data.png
--- 

In the new TRS console, users will be able to search for a record and view the data in it. This is where they can input new data or edit existing data.

We’re starting with mandatory qualifications, which enable teachers to specialise in hearing, visual or multi sensory impairments. There are approximately 14,000 records with mandatory qualifications. The design for this should be scalable to other data types, such as initial teacher training which is more common.

We’ve used a [secondary navigation bar] (https://design-patterns.service.justice.gov.uk/components/sub-navigation) from the MoJ design system. This is consistent with recent design work in the related areas of [access your teaching qualifications] (https://tra-digital-design-history.herokuapp.com/qualifications-service), and [register trainee teachers] (https://becoming-a-teacher.design-history.education.gov.uk/register-trainee-teachers).

## No qualifications

If the record has no qualifications, text is displayed to say “no mandatory qualifications”, with a primary button to add a mandatory qualification.

## With a qualification

The qualification view uses a summary card to display the fields. Each field has a change link to edit the data. 

In the initial design, the card action is not used. This will potentially be to “remove qualification”. The required action for deleting data and what needs to be recorded for auditing purposes is to be defined and may not be included in the MVP.

### Missing data

Some of the old data is incomplete or not formatted in this way. For example, 67% of the old data either doesn’t have a provider name, or has other information in this field such as a description of a type of course.  

In cases where the data is ‘NULL’ or missing, we will display “None” or “Unknown”. We will work with the service to define the quality of data for the new system, such as using the centralised [DfE reference data repository] (https://github.com/DFE-Digital/dfe-reference-data) to store provider names, and how to migrate data that doesn’t fit the standard.

We only collect an end date if the result of the course is passed. If the result is not passed, we won’t show the end date field.