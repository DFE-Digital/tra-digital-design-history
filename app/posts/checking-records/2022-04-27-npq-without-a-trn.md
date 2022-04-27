---
  title: NPQ registration with records being checked by a service
  date: 2022-04-27
  screenshots:
    items:
      - text: "What is your email address?"
        src: 01-what-is-your-email.png
      - text: "Confirm your email address"
        src: 02-confirm-email.png
      - text: "First time user: We’ll ask you some questions"
        src: 03-ask-questions.png
      - text: "First time user: Do you have a TRN?"
        src: 04-do-you-have-a-trn.png
      - text: "First time user: Do you know your TRN?"
        src: 05-do-you-know-your-trn.png
      - text: "First time user: What is your TRN?"
        src: 06-what-is-your-trn.png
      - text: "First time user: Your name"
        src: 07-your-name.png
      - text: "First time user: Your name (if they have no TRN)"
        src: 07-your-name-no-trn.png
      - text: "First time user: Your date of birth"
        src: 08-your-date-of-birth.png
      - text: "First time user: Do you have a National Insurance number?"
        src: 09-do-you-have-a-national-insurance-number.png
      - text: "First time user: What is your National Insurance number?"
        src: 10-what-is-your-national-insurance-number.png
      - text: "First time user: Do you have QTS?"
        src: 11-do-you-have-qts.png
      - text: "First time user: Did a training provider award QTS?"
        src: 12-did-a-training-provider-award-qts.png
      - text: "First time user: Next time you use this service"
        src: 13-next-time-you-use-this-service.png
      - text: "First time user: Check answers"
        src: 14-check-answers.png
      - text: "First time user: Check answers (if they have no TRN)"
        src: 14-check-answers-no-trn.png
      - text: "First time user: Finished asking questions"
        src: 15-finished-asking-questions.png
      - text: "First time user: Finished asking questions, but no account made"
        src: 15-finished-asking-questions-no-account-made.png
      - text: "Check answers at the end of the NPQ registration journey"
        src: 16-check-answers-at-the-end-of-the-npq-journey.png
      - text: "Repeat user: You’re signed in"
        src: 17-youre-signed-in.png
  related:
    items:
    - text: Register for an NPQ design history
      href: https://teacher-cpd-design-history.herokuapp.com/register-for-an-npq/
    - text: Video of existing NPQ journey
      href: https://youtu.be/MdaS0gJsP-c
---

Building on the work of [Find a lost TRN](/find-a-lost-trn), we are reusing our record checking questions to create a service for identifying users.

We are starting by prototyping the service as part of the NPQ registration journey, replacing their questions about identity with our service.

This means capturing the following personal information:

- teacher reference number (TRN)
- name
- previous name
- date of birth
- National Insurance number
- QTS awarding body

This information is then used to match against the database of qualified teachers (DQT) and the continuing professional development (CPD) databases. We keep asking for information until we make a match, we need a minimum of 3 matching details.

The quickest match happens if TRN, name and date of birth match. In this case the user would not be asked for their National Insurance number or QTS awarding body.

## Why NPQs

Users registering for an NPQ must currently have a TRN. Anyone can take an NPQ – including people working internationally and people not working in education. These users do not have a TRN and need to get one before they can register for their NPQ. This can be a painful and slow process.

TRNs are meant for qualified teachers. By giving TRNs to people studying an NPQ we are polluting the database of qualified teachers.

By replacing questions about identity, we can create a way to register for an NPQ without a TRN.

## Design decisions

### No passwords

Early designs focused on accounts and passwords. We needed to justify why a user needs another email and password to remember.

We iterated to a simpler concept: next time you use this service, you can use your email address to skip these questions.

### Seamless integration with a service

While users are navigating questions in the checking records service, the design of the pages matches the NPQ design. This means showing the NPQ service name in the header. We do not warn users that they are crossing service boundaries.

However – the services will likely have different policies on:

- cookies
- privacy and data retention
- accessibility

We might also find that maintaining a single-design between the services becomes unmanageable, for instance if they begin to use different versions of the GOV.UK design system.

A clear differentiation might be needed.

### Creating a ‘checking records’ section in the journey

While we do not warn users about service boundaries, we did find it necessary to bookend the checking records part of the journey.

The beginning and end of the journey use [blue interruption cards](https://github.com/alphagov/govuk-design-system-backlog/issues/27) to achieve this. ([The opening bookend](#first-time-user-we-ll-ask-you-some-questions) and the [closing bookend](#first-time-user-finished-asking-questions))

By creating this context we can talk about skipping ‘these’ questions when it comes to using an email address to sign in next time.

## Video walkthroughs

### Latest iteration

{% from "embed/macro.njk" import appEmbed with context %}
{{ appEmbed({
  youtubeId: 'wU-MG4Z7Ddw',
  title: 'Video of journey through NPQ registration when records are checked by a service'
}) }}

This version uses the ‘skip questions using your email address’ concept.

### Existing NPQ journey

You can compare our current designs with a video walkthrough of the existing NPQ journey:

{{ appEmbed({
  youtubeId: 'MdaS0gJsP-c',
  title: 'Video of the existing NPQ journey'
}) }}

In this version a user must have a TRN to continue.

### First iteration

A version of the design that creates accounts and asks for passwords.

{{ appEmbed({
  youtubeId: 'HB0fvaVltBs',
  title: 'An earlier iteration of the journey using accounts and passwords'
}) }}
