---
title: Creating an account and signing in
date: 2023-02-06
---

{% from "email/macro.njk" import appEmail with context %}

We initially planned to use DfE Sign-in. But it’s reserved for users outside of DfE. This decision may change if we give panelists access to the service.

So we have designed flows for:

- creating an account
- signing in
- reseting your password

## How it works

### Creating an account

We’ll send each caseworker an email inviting them to create an account.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Create your account",
  content: "

Create an account to manage referrals of serious misconduct by a teacher.

Set up your password:
((link))

You have until 10 February 2023 at 11:09am to set up your password.
  "
}) }}

Clicking the link takes them to the service to set up their password.

![Change password](change-password.png)

Once they enter their password, they’ll be taken to the referrals page.

### Signing in

If the user is signed out, they’ll see the sign-in page.

![Sign in](sign-in.png)

If they have forgotten their password, they can click ‘Reset your password’.

![Reset password](reset-password.png)

Once they submit their email address they’ll be shown a page with instructions about how to reset their password.

![Check email](check-email.png)

Here’s the email that they’ll receive to reset their password.

<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Reset your password",
  content: "

You requested a link to reset your password.

Change your password:
((link))

If you did not make this request, ignore this email. Your password will not be changed.
  "
}) }}

Clicking the link takes them to a page to enter a new password.

![Change password](change-password.png)

Once they enter their new password, they’ll be taken to the referrals page.
