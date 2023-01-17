---
title: Sending users a link to access their referral
date: 2023-01-17

---

{% from "email/macro.njk" import appEmail with context %}

From user research, we know that users often complete their referral over several sessions.

So we’ve designed a way for users to quickly and easily access their referral.


## How it works

When users create an account and sign in for the first time, we’ll send an email with a link so they can access their referral.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral of serious misconduct by a teacher",
  content: "

You’ve created a referral of serious misconduct by a teacher.

Complete your referral:

http://www.example.com/referral/1


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}


