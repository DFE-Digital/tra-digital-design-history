---
  title: Checking records for NPQ, but with TRN as a requirement
  date: 2022-07-06
  screenshots:
    items:
      - text: "Ask questions iteration"
        src: 01-ask-questions-iteration.png
      - text: "What is your trn"
        src: 02-what-is-your-trn.png
      - text: "Check answers iteration"
        src: 03-check-answers-iteration.png
  related:
    sections:
      - title: Related content
        items:
          - text: Prototype PR
            href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/119
---

One of the main aims of the Checking records service is to remove the requirement for people registering for an NPQ to have a TRN. For example, non-teachers and international teachers without QTS, are eligible to take and pay for an NPQ, but right now we require them to send ID documents to TRA, so we can create them a TRN, so they can register. TRNs are meant to be for teachers, so this isn’t right.

Generally, we want to reduce the dependency on TRNs, in favour of a central teacher record.

## TRN as a temporary requirement

If we rolled out the Checking records service [as previously designed](/checking-records/npq-without-a-trn/), we would be doing two things at once:

1. Replacing the NPQ validation flow with the Checking records service
2. Changing policy around use of TRNs

We do not need to do these two together. We can reduce the risk around the Checking records service and begin building it before we change the TRN policy.

This way we can turn off the TRN requirement when we are ready, and do that in a staged way, meaning we control the flow through the non-TRN journey to reduce the risk of the policy change.

## Design changes

This design explores what the Checking records journey looks like if we make TRN a requirement.

The main changes are:

- the TRN question is moved towards the end, before the QTS question – if we can match on email, name, date of birth and National Insurance number, users do not need to go through the pain of finding or remembering their TRN
- we do not ask if they have or know their TRN, we will depend on the NPQ service to keep their current designs explaining the need and use of TRNs
- when we ask for TRN we give some extra guidance on what a TRN looks like, and link to the Find a lost TRN service

## Walkthrough

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('727303249') }}
