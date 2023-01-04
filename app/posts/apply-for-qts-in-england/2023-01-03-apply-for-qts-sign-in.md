---
title: Signing into ‘Apply for QTS in England’ service
date: 2023-01-03
screenshots:
items:
- text: "Code received by email"
- src: code-received-by-email.png
- text: "Confirm email address"
- src: confirm-email-address.png
---

We started private beta with a ‘magic link’ method as a secure way for applicants to sign in to the Apply for QTS in England service. This allowed us to check that applicants could access the email address they’d supplied, without the need for them to create and remember a password for the service.

Applicants were emailed the link and given 20 minutes to use it to access their application, or to submit further information.

This method has been successfully tested by related services such as ‘Apply for initial teacher training (ITT)’. We also ran our own testing of the magic link approach during user research sessions, which also tested well.

By the time the new service had received 60 applications for QTS, we had experienced 2 support queries from applicants who had issues with their magic link. The links appeared to have ‘expired’ despite applicants using them straight away.

Looking at the Notify delivery reports, we saw that this issue was likely to affect around 1 in 12 applicants.

From screen grabs shared by applicants, and research with other services, we’ve understood this to be an issue with Safe Links. Certain email providers perform a security screening of magic links and identify them as malicious, which leads to the link being invalidated and acting as though it’s already been used.


## What we changed
We decided to replace the magic links with an email based one-time password (OTP) to authenticate applicants – an approach used by ‘Refer serious misconduct by a teacher’ service.


## How it works
When applicants want to sign into Apply for QTS in England, they’ll receive an email from us with a 6-digit code. They will then need to input this code into the service within 15 minutes to confirm their email address and sign in.

Email-based OTP ensures that the applicant:

* has control of, and has entered a valid email address to sign into the service
* does not need to remember or write down a password
* does not experience their email provider invalidating links that give access to the service


## Future considerations
We will continue to monitor support queries to check that the use of OTP is not causing problems for applicants trying to sign into the service.

### Screenshots
#### Email received by the applicant
![Email received by the applicant](code-received-by-email.png)

#### Entering the one-time password
![Entering the one-time password](confirm-email-address.png)
