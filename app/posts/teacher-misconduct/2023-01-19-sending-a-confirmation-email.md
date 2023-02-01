---
title: Sending a confirmation email
date: 2023-01-19
screenshots:
  items:
    - text: Confirmation page
      src: confirmation-page.png
---

{% from "email/macro.njk" import appEmail with context %}

We show users a [confirmation page when they send their referral](/teacher-misconduct/changes-to-the-form).

But once the user leaves the service, they’ll no longer have access to this information. For example, how long it will take the TRA to make a decision about the case.

The user also might not be able to find the original email with the link to their referral.

So we’ve decided to send users a confirmation email.

As part of this work, we changed this content to be clearer and more concise. We've also updated the confirmation page content to match.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral of serious misconduct has been sent",
  content: "

You’ve sent a referral of serious misconduct.

View your referral:

http://www.example.com/referral/1

# What happens next

Your referral will be reviewed within 3 working days.

If a decision is not made about your case within 14 days, you’ll be sent an email letting you know.

The TRA could decide that:

- more information is needed
- the case will not be investigated, for example because it’s unlikely the teacher will be stopped from teaching
- a formal investigation will be launched

You’ll be sent an email with the decision within 20 weeks.

# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}


