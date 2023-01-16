---
title: Reminding users to complete their referral
date: 2023-01-16

---

{% from "email/macro.njk" import appEmail with context %}

We [removed the ability for users to delete referrals](/teacher-misconduct/removing-the-ability-to-delete-a-referral) because we’ll automatically delete referrals that have not been sent 3 months after their last update.

## How it works

We now send users an email reminding them that their draft referral will be deleted if they do not take action.


### 7 days before a draft referral is deleted

We remind users that their referral has not been updated in more than 2 months.

We tell the user the date that their referral will be deleted and give them a link to complete their referral.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral will be deleted in 7 days",
  content: "

Your referral of serious misconduct by a teacher has not been updated in over 2 months.

It’ll be deleted in 7 days on 19 August 2023.

If you would like to keep your referral, you must make changes or send it.

Complete your referral:

http://www.example.com/referral/1


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}


### 1 day before a draft referral is deleted

We send users an email telling them they have 1 day before their referral will be deleted.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral will be deleted in 1 day",
  content: "

Your referral will be deleted tomorrow, 19 August 2023.

If you would like to keep your referral, you must make changes or send it.

Complete your referral:

http://www.example.com/referral/1


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}

### After a referral has been deleted

If a user decides not to take any action, their referral is deleted and we send an email letting them know.

We also include a link to start a new referral if users have missed the previous reminders or change their mind.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your referral has been deleted",
  content: "

Your referral of serious misconduct has been deleted.

You can start a new referral:

https://example.com/start/etc


# Get help

Email: misconduct.teacher@education.gov.uk
We aim to respond within 3 working days.

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except public holidays)

  "
}) }}

## Further considerations

We’ll check user feedback to make sure the current timings of the email reminders are correct.

