---
  title: Get an identity for NPQ, but with TRN as a requirement
  date: 2022-07-06
  screenshots:
    items:
      - text: "Ask questions iteration"
        src: 01-ask-questions-iteration.png
      - text: "What is your TRN?"
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

One of the main aims of the Get an identity service is to remove the requirement for people registering for an NPQ to have a TRN. For example, non-teachers and international teachers without QTS, are eligible to take and pay for an NPQ, but right now we require them to send ID documents to TRA, so we can create them a TRN, so they can register. TRNs are meant to be for teachers, so this isn’t right.

Generally, we want to reduce the dependency on TRNs, in favour of a central teacher record.

## TRN as a temporary requirement

If we rolled out the service [as previously designed](/get-an-identity/npq-without-a-trn/), we would be doing two things at once:

1. Replacing the NPQ validation flow with the service
2. Changing policy around use of TRNs

We do not need to do these two together. We can reduce the risk around the service and begin building it before we change the TRN policy.

This way we can turn off the TRN requirement when we are ready, and do that in a staged way, meaning we control the flow through the non-TRN journey to reduce the risk of the policy change.

## Design changes

This design explores what the Get an identity journey looks like if we make TRN a requirement.

The main changes are:

- the TRN question is moved towards the end, before the QTS question – if we can match on email, name, date of birth and National Insurance number, users do not need to go through the pain of finding or remembering their TRN
- we do not ask if they have or know their TRN, we will depend on the NPQ service to keep their current designs explaining the need and use of TRNs
- when we ask for TRN we give some extra guidance on what a TRN looks like, and link to the Find a lost TRN service

### TRN before QTS

There’s an open question about which we ask first, TRN or QTS provider. If we ask for QTS, then that's one more thing we can use to match, meaning users don't need to dig out their TRN. However, we also saw in research for the Find a lost TRN service that this isn’t the easiest question to answer – we minimised the confusion by iterating the question – but users may still find it difficult to answer.

We should put the easiest question first. We do not know which is easiest, for now, we’re going with TRN – but we are happy to change this if we find otherwise.

Ease of use will also depend on the availability of the QTS autocomplete when picking your ITT provider, which hasn't been built for Find a lost TRN yet.

## Walkthrough

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('727303249') }}
