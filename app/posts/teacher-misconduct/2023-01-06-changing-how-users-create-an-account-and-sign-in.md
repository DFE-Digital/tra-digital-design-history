---
title: Changing how users create an account and sign in
date: 2023-01-06

---

{% from "email/macro.njk" import appEmail with context %}

In order to sign in or create an account, we send users a confirmation code by email.

But we did not design a way for users to request another confirmation code, if they do not receive one.

We also wanted to avoid users creating an account before they know if they’re eligible to use the service.

So we:

- added a way for users to request another confirmation code
- changed the way users access the service, depending on whether they have an account or not

## How it works

We first ask users if they have an account or not.

![Changing how users create an account and sign in](account-yes.png)

### If the user has an account

We ask them to sign in to continue making their referral of serious misconduct.

![Changing how users create an account and sign in](sign-in.png)

After the user enters their email address, they’ll be taken to the ‘Check your email’ page.

![Changing how users create an account and sign in](Check-email.png)

They’ll be sent an email containing a confirmation code.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "123456 is your confirmation code",
  content: "


You requested a confirmation code to continue making a referral of serious misconduct.

The code will expire in 1 hour. You can only use the code once.

Confirmation code: [123456]

# Get help

Contact the Teacher Regulation Agency (TRA) if you’re having problems signing in:

Phone: 020 7593 5393
Monday to Friday, 9am to 5pm (except bank holidays)

  "
}) }}

Users can select ‘request another confirmation code’ on the 'Check your email' page if they don’t receive the first one.

If they do, they’ll be taken to the screen to enter their email address again.

![Changing how users create an account and sign in](sign-in.png)


### If the user does not have an account

[We ask the user a series of questions to find out if they’re eligible](/teacher-misconduct/changes-to-the-form) to make a referral of serious misconduct.

This means that:

- users are not asked to create an account before we know they’re eligible
- we do not have to store users’ email addresses if they’re not needed

Once we know they’re eligible to use the service, we ask for their email address.

![Changing how users create an account and sign in](Your-email.png)

The user is then taken to the ‘Check your email’ page to enter their confirmation code and sign in.

### If the user selects that they have an account - but they do not

After entering their confirmation code, they’ll be asked the eligibility questions first.

This means they will not have to provide their email address unless they’re eligible to make a referral of serious misconduct.


### If the user selects that they do not have an account - but they do

After entering their confirmation code, they’ll skip the eligibility questions and go straight to the task list.

This means they can continue their referral from where they left off.

![Changing how users create an account and sign in](Task-list.png)

## Further considerations

We’ll consider future user research to confirm that:

- the "I’m not sure" option is not required when asking if a user has an account
- we do not need help text explaining why a user must provide their email address when creating an account

