---
title: Reminding users to complete their referral
date: 2023-01-16

---

{% from "email/macro.njk" import appEmail with context %}

We [removed the ability for users to delete referrals](/teacher-misconduct/removing-the-ability-to-delete-a-referral) because we’ll automatically delete referrals that have not been sent 90 days after their last update.

## How it works

We’ll send an email reminding the user that they need to complete their referral within 7 days of deletion.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral will be deleted in 7 days",
  content: "

Your referral of serious misconduct by a teacher has not been updated in a while.

It’ll be deleted in 7 days on 19 August 2023.

If you would like to keep your referral, you must make changes or complete it.

Complete your referral:

https://www.example.com/referral/1


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}

If the user still does not update or complete their referral, we’ll send another email giving them 1 day's notice before it's deleted.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral will be deleted in 1 day",
  content: "

Your referral will be deleted tomorrow, 19 August 2023.

If you would like to keep your referral, you must make changes or complete it.

Complete your referral:

https://www.example.com/referral/1


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}

If the user still does not update or complete their referral, we’ll send an email letting them know that their referral has been deleted.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral has been deleted",
  content: "

Your referral of serious misconduct has been deleted.

You can start a new referral:

https://example.com/start


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}

## Further considerations

We’ll check user feedback to make sure the current timings of the email reminders are correct.

