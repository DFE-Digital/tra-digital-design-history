---
title: Background to the creation of the TRS console
date: 2023-12-13
description: How we’re improving the way we store and access data about people with teacher reference numbers.
screenshots:
  items:
    - text: Viewing a mandatory qualification in Dynamics
      src: view-mandatory-qualification-dynamics.png
    - text: Viewing an alert in Dynamics
      src: view-alert-dynamics.png
---

The database of qualified teachers (DQT) contains data about people who have a teacher reference number.

Most of these people are allowed to teach in England. The database includes information about:

- personal details, for example name and date of birth
- initial teacher training, for example the name of the provider
- qualified teacher status and early years teacher status, for example the date they were awarded
- induction, for example the start and end dates
- mandatory qualifications for teaching pupils with sensory impairments, for example the teacher’s specialism
- alerts, for example if the person failed their induction and is not allowed to teach

Many older records are incomplete or include data which is no longer relevant. The data in DQT is being improved and moved to a new database called the teaching record system (TRS).

## Who uses the data

The data is used by:

- teachers who want to [access their qualifications](https://tra-digital-design-history.herokuapp.com/qualifications-service/) and download their certificates
- employers who want to [check a teacher’s record](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/) to make sure they’re allowed to teach
- members of Teaching Regulation Agency (TRA) or DfE staff, for example to add or delete qualifications

## Why we’re creating the TRS console

DfE and TRA staff currently access data using a Microsoft Dynamics system. It does not meet the standards for government digital services.

Since we’re replacing DQT with the new TRS database, at the same time we’re building a service for staff to access the data.

The new service will be based on the GOV.UK design system. The name may change, but it’s currently called the TRS console.

## How we’ll create the TRS console

We’re building the new TRS console one part at a time. Users will need to do some tasks in the Microsoft Dynamics service until it can be fully replaced.

We’ll initially focus on:

- mandatory qualifications for teaching pupils with sensory impairment
- requests to change someone’s name or date of birth in the database
- managing alerts

We want to make sure that our designs will work for other parts of the service when we come to design them. For example, we may need the ability to add notes in several parts of the service.
