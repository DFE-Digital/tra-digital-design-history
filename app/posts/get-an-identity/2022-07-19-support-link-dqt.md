---
  title: Support screens for adding a DQT record
  date: 2022-07-19
  screenshots:
    items:
      - text: "User list"
        src: 01-user-list.png
      - text: "User page"
        src: 02-user-page.png
      - text: "What is their TRN?"
        src: 03-what-is-their-trn.png
      - text: "Is this the right record?"
        src: 04-confirm-record.png
      - text: "Record added"
        src: 05-record-added.png
  related:
    sections:
      - title: Related content
        items:
          - text: Prototype PR
            href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/127
---

A support agent that manually identifies a DQT record for a Get an identity user needs a way to link the two records.

In this design a support agent would:

- pick a user from the list of users
- choose to add a DQT record for that user
- lookup the DQT record by using their teacher reference number (TRN)
- check the record is correct (for example, they haven't typo’d the TRN)
- add the record, or cancel the request

The user list will change, we still need to design a way to find users in support.

## Verifying a name by adding a DQT record

If the name we have is not verified, when a DQT record is added, if the names match, then we will mark the name as verified.

If the names do not match then there is no change.

## Video walkthrough

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('731408424') }}
