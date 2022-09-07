---
  title: Exploring GOV.UK Sign-in for MVP
  date: 2022-09-07
  related:
    sections:
      - title: Related content
        items:
          - text: GOV.UK Sign-in
            href: https://www.sign-in.service.gov.uk/
          - text: Roadmap
            href: https://www.sign-in.service.gov.uk/features/roadmap
---

[GOV.UK Sign-in](https://www.sign-in.service.gov.uk/) lets users sign in to services with a central GOV.UK account.

It is new and we've been accepted on to the beta programme. We need to decide if, when and how to integrate with it.

> Let your users sign in to your service with their email address, password and two-factor authentication.
>
> They’ll be able to use these details to access all services that use GOV.UK Sign In. This is part of our ‘one login for government’ vision.

## What users would see

A video walkthrough of the GOV.UK Sign-in registration journey:

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('747247603') }}

## What is the user need?

By using a GOV.UK account our users would benefit from:

- reuse of an existing account, signing in to education services with the same account they use across government
- give data once, and update in a single place – sharing of data between services, but only when it is implemented
- prove who they are once and reuse, but only when it is implemented

These user benefits are not realised in the beta.

Users will not already have an account, and few services will be using GOV.UK Sign-in. No data is currently shared between services. Identity assurance is a long way off.

## Service needs

As a service we would get accounts with stronger security, through:

- password protection
- 2 factor authentication (2FA) using a UK phone number or authenticator app

We don't intend to build passwords into our journey, but we’d get 2FA 'for free'.

## Pain points with GOV.UK Sign-in

By introducing GOV.UK Sign-in to the user journey, we are asking users for more, without giving any tangible benefit.

We don’t get any information for free from GOV.UK Sign-in, we still need to ask users for:

- name and previous names
- date of birth
- National Insurance numbers
- teacher reference numbers
- QTS providers

### Do I have an account?

On Get an identity we avoided the concept of accounts, and the choice of sign in or register. Instead users give us their email and we sign them in if we recognise it. This works well for occasional use services.

With GOV.UK Sign-in users need to determine if they already have a GOV.UK Sign-in account.

Users need to choose whether to sign in or register. They will not already have an account, but they will confuse it with other government accounts, such as Government Gateway, Verify, and so on.

### Passwords

[We chose not to implement passwords](/get-an-identity/npq-without-a-trn/#no-passwords) for Get an identity. We needed to justify why a user needs another email and password to remember. For services such as register for an NPQ, where return use is less likely, this is difficult to justify.

With GOV.UK Sign-in users need to:

- decide on a password
- remember or save their password

### Set up 2 factor authentication (2FA)

[We are exploring this for Get an identity](/get-an-identity/mvp-2fa/).

2FA is mandatory for GOV.UK Sign-in.

International users would need to use an authenticator app as phone number based 2FA is only supported for UK numbers.

Authenticator apps are confusing, but especially so for users who will not have English as a first language.

## Conclusion

For now only Register for an NPQ will be using Get an identity. Repeat use is rare within the NPQ service, and the need for accounts is hard to justify. The service would not benefit from the increased security of using GOV.UK Sign-in. We should hold off on integrating GOV.UK Sign-in until more services are using Get an identity.

We should only integrate with GOV.UK Sign-in when there are tangible benefits for our users. This will be shaped by the services using Get an identity and their needs. Along with the ongoing uptake of GOV.UK Sign-in and their development of new features.
