---
title: Users confused by the one-time password (OTP) confirmation code
date: 2023-03-27
screenshots:
items:

- text: "Page where the user provides their email address"
- src: user-provides-email-address.png
- text: "Email where the user receives the OTP code"
- src: user-receives-otp-code.png
- text: "Page where the user enters the OTP code"
- src: user-inputs-otp-code.png
---

### Background
There have been 260 support queries where users have either replied to an automated email that delivers their one-time password (OTP) code to sign in, or support queries where users are asking for help to sign into the Apply for QTS in England service.

This is how the 260 users responded to the OTP email:

* 104 replied with a comment
* 19 replied with no comment
* 100 emailed the OTP code back
* 33 sent their email address
* 1 sent a web link to the Apply for QTS in England service
* 3 replied with their application documents

These comments indicated that users wanted to:

* confirm their email address
* ask for support
* find out why their QTS application was declined

**Aim**: make it easier for our users to succeed with verifying their email address and signing into the service.

### What we changed


We have not had the opportunity to research why users are either replying to the automated email or have had difficulty in using an OTP to validate their email address. Instead, we’ve opted to look at some of the helpdesk queries for ways to improve this validation process.

We decided to tweak the wording so that those less familiar with OTP email ‘authentication’ can engage with the process.

On the page where the user provides their email address, we explain why we’re asking the user for their address: “We’ll use this to send you a code to continue with your QTS application. Do not use a work or university email that you might lose access to.”

To deter users from replying to the automated email that delivers the OTP, we added the inset text “This is an automated email, please do not reply”.

Also, instead of saying that we were validating the user’s email address, we chose to explain that the code would be used to help them ‘sign into’ the service – a transaction they would hopefully be more familiar with. The content was changed to “Use this code to sign into the Apply for QTS in England service.”

On the page where the user enters the OTP code, we’ve added that “The code will expire in 15 minutes.” as a better place to advise users that the code will need to be entered within that time frame.

#### Impact of these changes

Unfortunately, the content changes did not positively impact the number of users struggling to sign into the service. Since introducing the content changes, only 42% of users have been able to use the OTP request to start their application.

#### Barriers to using the OTP method

There are a number of authentication methods, for example social login, one-time passwords, and biometric authentication. The OTP method may be an unfamiliar method for users in certain countries, and perhaps caused confusion for those experiencing it for the first time.

During user research sessions, some of our users demonstrated limited digital skills, which may also have been another barrier to signing into the service.

Since opening up the service to African countries, we’ve seen a significant increase in the number of people using a mobile device to access the service –currently around 78% of users are now using a mobile device. Using a mobile device to interact with the service can be quite problematic when switching between applications from email (to get the OTP) to adding in the correct passcode in an online browser (input the OTP).

### What we decided to do next

We decided that using a more familiar method of signing into the service would be an effective and easier option for users – especially those with low digital skills. We opted to use ‘magic links’ for users to sign in, as it's a more widely used method that has previously tested well with our users. We stopped using this method, as certain [email clients began to invalidate the magic link before its use](https://tra-digital-design-history.herokuapp.com/apply-for-qts-in-england/apply-for-qts-sign-in/).

To overcome this problem, we added an intermediate page that can prevent email clients from pre-fetching the link and invalidating it before the user has a chance to use it.

The ‘Apply for initial teacher training’ (ITT) team has already successfully implemented this approach on their service, which can be found [here](https://sandbox.apply-for-teacher-training.service.gov.uk/), choose ‘Continue as a candidate’ and sign up to see the flow.

This is how we’ll prevent magic links from being invalidated before they’re used.
1. Users enter their email address on the service.
2. They receive an email that contains a magic link with a token that leads to an intermediate page.
3. The intermediate page contains a form that includes the token from the query string parameters as a hidden field.
4. Submitting the form signs the user into the service and invalidates the token.

### Future considerations

We’ll closely monitor how well magic links perform by reviewing help desk feedback. In particular, we’ll need to measure how many users reply to the magic link email to request support, but also assess how many users are able to transition from their personal email to their application.

If this sign-in method is ineffective, we may want to consider using a different approach, perhaps the ‘[GOV.UK One](https://www.sign-in.service.gov.uk/)’ from GDS for example.


### Screenshots

![Page where the user provides their email address](user-provides-email-address.png "Page where the user provides their email address")

![Email where the user receives the OTP code](user-receives-otp-code.png "Email where the user receives the OTP code")

![Page where the user enters the OTP code](user-inputs-otp-code.png "Page where the user enters the OTP code")
