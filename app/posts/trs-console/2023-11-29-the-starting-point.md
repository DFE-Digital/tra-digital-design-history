---
title: The starting point
date: 2023-11-29
description: A minimum viable service that will allow DfE staff to manage data in the teacher record system
screenshots:
  items:
    - text: A screen for editing MQs in Dynamics
      src: mq-dynamics.png
--- 

The existing database of qualified teachers (DQT) is being migrated to a new teaching record system (TRS). This system contains data about people who teach in the UK, including: 

- personal details 
- initial teacher training (ITT)
- inductions - qualified teacher status (QTS), and statuses for teaching in early years settings
- mandatory qualifications (MQ) for specialisms in hearing, visual or multi sensory impairments
- alerts, such as being restricted or prohibited from teaching 

The data is used by [teachers for accessing their qualifications](https://tra-digital-design-history.herokuapp.com/qualifications-service/), and [employers to check their record](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/) before starting a teaching role. 

The Department for Education gets data from sources such as training providers which they can input and manage. Officers use a Dynamics dashboard to interact with the DQT. This isn’t user friendly and doesn’t meet Government digital service standards. 

We’re building a console to interact with the new TRS, based on the [GOV.UK](http://GOV.UK) design system. The aim is to enhance the user experience and ensure data accuracy. 

We’re building out the new TRS one feature at a time, instead of rebuilding entirely. It will run alongside the old DQT until it can be replaced. 

The first features will focus on MQs, and requests to change personal details such as name changes. Our priority is to make sure these designs are scalable as larger parts of the system get migrated and enable good practice for data quality. 

We started with an initial set of wireframes for MQs, personal details, making manual changes, and managing alerts. These will be refined and tested with users.