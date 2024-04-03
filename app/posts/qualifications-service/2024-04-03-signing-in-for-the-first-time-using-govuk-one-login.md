---
  title: Signing in for the first time using GOV.UK One Login
  date: 2024-04-03
  related:
    sections:
      - title: Related content
        items:
          - text: Access your teaching qualifications prototype (password - qs)
            href: https://qualifications-prototype.herokuapp.com/
  screenshots:
    items:
      - text: "User journey diagram"
        src: high-level-user-flows.png
      - text: "The user has not been able to verify their identity with GOV.UK One Login so they need to get support (not included in research)"
        src: unable-to-verify-interruption.png
      - text: "The user has verified their identity but we need more information to connect their teaching record"
        src: verified-connect-interruption.png
      - text: "We’ve connected the user’s teaching record (not included in research)"
        src: connect-success.png
      - text: "We cannot connect the user’s teaching record and they’ll need to get support"
        src: unable-to-connect-interruption.png
      - text: "The user needs to check the details they gave before asking for support"
        src: unable-to-connect-check-answers.png
      - text: "The user has submitted a support request"
        src: support-success.png
      - text: "Teacher record shown once the user signs in"
        src: quals-landing-page.png
---
To access their teaching qualifications after we [replace DfE Identity with GOV.UK One Login](/qualifications-service/using-govuk-one-login-with-tra-online-services), a user will need to have:

- created a GOV.UK One Login
- verified their identity for their GOV.UK One Login
- connected their teaching record to their GOV.UK One Login

These steps must be completed in order, but they may be completed at different times. For example, the user may have created a GOV.UK One Login several months earlier when using a different service.

## Creating a GOV.UK One Login

The service start page allows a user to sign in with their GOV.UK One Login to access their teaching qualifications.

If the user does not have a GOV.UK One Login, they need to start by [creating a GOV.UK One Login](https://www.sign-in.service.gov.uk/about/signing-users-in).

## Verifying identity for a GOV.UK One Login

If the user has already verified their identity then our service gets their:

- name
- previous names
- date of birth

Otherwise the user is prompted to [verify their identity for their GOV.UK One Login](https://www.gov.uk/using-your-gov-uk-one-login/proving-your-identity).

### If the user cannot verify their identity

A user may not be able to verify their identity. For example, they may say ‘no’ to all the options in the GOV.UK One Login journey such as:

- scanning a passport
- uploading a document
- going to a post office

The user can [get support from the GOV.UK One Login team](https://www.sign-in.service.gov.uk/support) but they can also choose to continue into our service. In that case, GOV.UK One Login only gives us their:

- name
- email address

We do not allow the user to try to connect their GOV.UK One Login to a teaching record. Instead we show an interruption page to say we have not been able to verify their identity and they need to get support.

We ask the user for their:

- name
- previous names
- date of birth
- National Insurance number - if they know it
- teacher reference number (TRN) - if they know it

We also ask the user to upload proof of their identity.

After they give the required information, the user is taken to a confirmation page. It tells them that the support team will email them to say either:

- the user can now sign in and access their teaching qualifications
- we need more information such as a different identity document

We generate a support ticket which includes the details which the user entered.

We expect that there will be fewer support requests once GOV.UK One Login replaces DfE Identity because there are several ways to for users to be verified.

## Connecting a teaching record to a GOV.UK One Login

We’ll often be able to connect a teaching record to a GOV.UK One Login without asking for more information.

If this is the case then we’ll allow the user to continue into the service.

Since the user has signed in to GOV.UK One Login, the pages in our service have the new [GOV.UK One Login service header](https://www.sign-in.service.gov.uk/documentation/design-recommendations/let-users-navigate-sign-out).

### If we cannot automatically connect a teaching record

We may need to ask for more details so we can find the correct teaching record.

First we show an [interruption page](https://github.com/alphagov/govuk-design-system-backlog/issues/27) which tells the user that:

- they’ve signed in and verified their identity
- we need more information

We think it’s important for users to know that they have a GOV.UK One Login at this point. They could use it to access another government service even if they do not connect it to their teacher record.

#### Asking for a National Insurance number

When the user continues from the interruption page we ask them whether they have a National Insurance number. We use radio buttons for yes or no, revealing an input for the number if they choose yes.

Most people with a teaching record have a National Insurance number. If we match it then we can be confident that we’ve found the right record.

The user is taken to an interruption page saying that their GOV.UK One Login has been connected to their teaching record and they won’t need to do this again. They can continue to the qualification page of their record.

#### Asking for a TRN

If we were not able to make a match using the response to the National Insurance number question then we ask the user whether they have a TRN. We use radio buttons for yes or no, revealing an input for the number if they choose yes.

We also use a details component so that the user can reveal more information about TRNs. This includes how to find a lost TRN or request one.

Everyone using the service should have a TRN, since they’re trying to access their teaching qualifications.

If they give their TRN then we should be able to connect to their teaching record unless there’s an issue such as a possible duplicate record.

The user is taken to an interruption page to saying that their GOV.UK One Login has been connected to their teaching record and they won’t need to do this again. They can continue to the qualification page of their record.

#### If we still cannot connect a teaching record to the GOV.UK One Login

If we still cannot find a match using the response to the TRN question then we show an interruption page. It tells them that they can get support.

After continuing, the user is prompted to check the answers they gave about their National Insurance number and TRN. They can then click the green button to get support.

The user is then taken to a confirmation page. They cannot continue in the service.

## User research

We created this journey in the AYTQ prototype so that we could test it with users. We wanted to make sure the integration with GOV.UK One Login is as seamless as possible.

We chose to test the scenario where we cannot connect to a teaching record. We did this because it involves the most steps and also allowed us to talk to users about what kind of support they might need.
