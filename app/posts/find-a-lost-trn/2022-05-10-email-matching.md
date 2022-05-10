---
  title: Email matching
  date: 2022-05-10
---

After launching Find a lost TRN, we found that some of the first requests that failed to match would have been successful if we had checked against the email given.

We originally descoped email matching from the Find a lost TRN journey because of [confusion in our early designs](/find-a-lost-trn/stopping-matching-on-email-address/):

> All participants expressed some degree of discomfort with this journey. The system felt insecure, with validation against the email address seeming too light.

In those designs we:

- automatically emailed a TRN if the email address matched
- did not explain how we had found the TRN

## Options for matching by email

Options include using email as:

- a direct, single factor match, but explaining how we made the match
- one of the three required factors for matching
- a stronger factor, perhaps matching email and one other thing (for example date of birth)

## Email as 1 of 3 factors

We are already collecting emails, and the addresses seem to have a tendency to match without needing guidance about what email address to use.

We could begin matching without any design changes.

Our email address screen is currently at the end of the journey. Everyone needs to give an email to get their TRN, we can bring this forward to the start. By putting the email question at the beginning we can shortcut the journey if there are matches.

The shortest journey becomes:

- email address matches
- name matches
- date of birth matches

We would not need to ask the National Insurance and QTS questions. The National Insurance number form has the highest error rate, avoiding this question will help users get their TRN faster.

### Video of email matching journey

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('708160369') }}

## User research

We have only tested this journey with a single user – they were surprised how quickly we got a match, but there was no discomfort like before.

This change is small, and isn't worth a dedicated round of research. We do need to continue testing this feature, and try some of the variants. This can happen as part of later research rounds, when we have more things to test.

Our confidence is otherwise high that this will improve the journey for users.
