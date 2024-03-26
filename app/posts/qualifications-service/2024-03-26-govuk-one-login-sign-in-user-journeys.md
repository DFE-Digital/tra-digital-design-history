---
  title: GOV.UK One Login user journeys for creating an account and signing in
  date: 2024-03-26
  related:
    sections:
      - title: Related content
        items:
          - text: Access your teaching qualifications prototype (password - qs)
            href: https://qualifications-prototype.herokuapp.com/
          - text: GOV.UK One Login prototype (password - pr0t0type)
            href: https://govuk-one-login-prototype-6d2545e2d700.herokuapp.com
  screenshots:
    items:
      - text: "High level user flows"
        src: high-level-user-flows.png
      - text: "We let the user know if we'll nedd some more information after signing in"
        src: verified-connect-interruption.png
      - text: "We tell the user when we've been successful in connecting their teaching record"
        src: connect-success.png
      - text: "We'll ask users to confirm some more details if we can't connect automatically"
        src: unable-to-connect-check-answers.png
      - text: "We tell the user if we can't connect to their record"
        src: unable-to-connect-interruption.png
      - text: "We confirm if we need to raise a request for support"
        src: support-success.png
      - text: "We tell the user if they've come back to our service without verifying identification with GOV.UK One Login"
        src: unable-to-verify-interruption.png
      - text: "When connected, the user lands on their qualifications"
        src: quals-landing-page.png
---
The user journeys vary depending if the user already has a GOV.UK One Login, if they have verified their identity, if we can connect it to a teaching record and if they need support.

Once signed in there are options to change personal details that either require proof or can be done straight away.

## Signing in

### Existing users whose record we can connect automatically

This is the simplest and will be the most common journey. In this scenario, the user has already created a GOV.UK One login and completed [identity verification](https://www.gov.uk/using-your-gov-uk-one-login/proving-your-identity) before they come to our service. We’re able to connect the details with a teaching record without asking for more information. If they have not yet verified their identity with GOV.UK One Login, they will need to do that within the sign in journey before returning to our service.

They will start on the service start page, complete the [GOV.UK One Login sign in journey,](https://www.sign-in.service.gov.uk/about/signing-users-in) then return to our service on the qualifications page of their record.

When signed in, users will see our service with the new [GOV.UK One Login service header](https://www.sign-in.service.gov.uk/documentation/design-recommendations/let-users-navigate-sign-out).

### Existing users who we can’t connect

This is the same as the first scenario, but we haven’t been able to automatically connect the information from GOV.UK One Login with a teaching record. We’ll need to ask for some more details so we can find the teaching record.

First we’ll show an [interruption page](https://github.com/alphagov/govuk-design-system-backlog/issues/27) which lets them know they’ve signed in and verified their identity, but we need some more information.

We ask if they have a National Insurance number using radio buttons for yes or no. Selecting ‘yes’ reveals an input for the number.

Selecting ‘no’ or if we can’t match the National Insurance number to a record goes to a screen to ask if they have a Teacher Reference Number (TRN). There is a details component to reveal more information about TRNs, including how to check if you have one or request one.

Selecting ‘no’ or if we can’t match the TRN to a record generates an interruption page that says we haven’t been able to find a record. The user is prompted to [check their answers](https://design-system.service.gov.uk/patterns/check-answers/). They can then get support. They will see a [confirmation page](https://design-system.service.gov.uk/patterns/confirmation-pages/).

If the National Insurance or TRN is successful, the user will get an interruption page to say their GOV.UK One Login has been connected to their teaching record and they won’t need to do this again. They can continue to the qualification page of their record.

### New users who can verify their identity

If the user has not created a GOV.UK One Login before, they will need to complete the [create a GOV.UK One Login journey](https://www.sign-in.service.gov.uk/about/signing-users-in). If we can connect automatically to a teaching record they will then land on the qualifications page of our service. If not, they will need to complete the steps for users who we can’t connect.

### Users who can’t verify their identity

This may happen if they select ‘no’ to all of the triage options they get, such as scanning a passport, uploading a document or going to the post office. They can try again or get support with GOV.UK One Login, or continue to our service unverified. If a user is unable to verify their identity with GOV.UK One Login, we’ll only know their email address and we won’t allow access to connect a teaching record.

In this case, we’ll ask for all the details we need to manually verify their identity. This will generate a support ticket. This will be processed in the same way that support verify people for DfE ID. We expect with GOV.UK One Login there will be fewer of these cases, because there are several ways to get verified before getting here.

We’ll show an interruption page to say they haven’t been able to verify their identity and need to get support.

We ask for name, any previous names, date of birth, a proof of identity, National Insurance number, and TRN. The National Insurance number and TRN are optional but will help to connect to a record. 

They get a confirmation page and support will email them to say either they can now sign in and access their record, or we need more information such as a different identity document.

Most of these questions do not repeat information that the user has already entered, although they may have tried to scan a document which contains it. If they have tried the face to face at a post office route, they will already have entered a name and date of birth. It is more likely that this route will be successful, or the user has selected ‘no’ to that option to arrive back in our service unverified. GOV.UK One Login offer [support to users who need it during the sign up process](https://www.sign-in.service.gov.uk/support).

## Prototype

We’ve made [a branch of the Access your teaching qualifications prototype](https://qualifications-prototype.herokuapp.com/landing-pages/v4/start) which includes creating a new GOV.UK One Login and being unable to connect with a teaching record.

Password: `qs`

## User research

We’re going to use the prototype to test with users. We want to make sure the integration is as seamless as possible. 

We’re using the scenario of failing to connect with a teaching record because it potentially involves the most steps and additional parts we’ve designed.