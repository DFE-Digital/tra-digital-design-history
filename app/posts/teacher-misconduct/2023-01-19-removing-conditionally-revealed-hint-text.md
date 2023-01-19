---
title: Removing conditionally revealed hint text
date: 2023-01-19
screenshots:
  items:
    - text: Do they carry out unsupervised teaching work?
      src: question1.png
    - text: Were they employed in England at the time the alleged misconduct took place?
      src: question2.png
    - text: Does the allegation involve serious misconduct?
      src: question3.png
---

At the moment, the eligibility flow has the following questions:

- Do they carry out unsupervised teaching work?
- Were they employed in England at the time the alleged misconduct took place?
- Does the allegation involve serious misconduct?

If the user selects “I’m not sure” to any of these questions” the text “If you’re not sure, you should continue to make a referral and the TRA will assess it” is conditionally revealed.

This was flagged as an accessibility issue in an internal audit. Additionally:

- hint text should be shown before selection in order to help users understand the meaning
- we do not have research that shows this content is useful

So we decided to remove this text.
