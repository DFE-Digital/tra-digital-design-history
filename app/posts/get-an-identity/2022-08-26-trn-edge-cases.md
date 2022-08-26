---
  title: When TRNs do not match what the user said
  date: 2022-08-26
  screenshots:
    items:
      - text: "Your TRN is different"
        src: 01-your-trn-is-different.png
      - text: "You have a TRN"
        src: 02-you-have-a-trn.png
---

We identified two edge case scenarios for TRNs:

1. A user gives us a TRN, but our match finds a different one
2. A user tells us they do not have a TRN, but we find that you do

In both scenarios:

- we have matched them on other factors
- we want to tell people their actual TRN

## Different TRNs

We think this could happen if:

- a user mistypes their TRN
- they have found and used the wrong 7 digit number (for example another number on their payslip or pension documents)
- they have [multiple TRNs](/find-a-lost-trn/improvement-for-users-with-two-trns/) (which to the user could be presented as their TRN changing)

### During MVP, when TRNs are required

Given that the TRN question is one of the last, and that we will often match before the TRN question, the chances of this happening are lower.

## You do have a TRN

This will happen if a user tells us they do not have a TRN, but then the personal details they give us match an existing DQT record.

We will always check to see if a record exists.

## Design changes

In both of these scenarios, after a user sees the ‘Check your answers’ page, they will be taken to a page showing their actual TRN, and outlining what has happened.

We will also email them a copy of their TRN.
