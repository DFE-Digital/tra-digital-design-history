---
  title: Hide details to protect personal data
  date: 2022-03-17
  screenshots:
    items:
      - text: "Signed in home page"
        src: 01-signed-in-home-page.png
      - text: "Update email"
        src: 02-update-email.png
      - text: "Update phone number"
        src: 03-update-phone-number.png
      - text: "Update National Insurance number"
        src: 04-update-national-insurance-number.png
  related:
    sections:
      - title: Related content
        items:
          - text: Risk documentation
            href: https://docs.google.com/document/d/1UlIEqeEqJRzYu7wE2tpR7mufY_N9l3hux7jcT34p4aE/edit
          - text: Trello
            href: https://trello.com/c/ggZFIZCj/241-remove-or-obfuscate-personal-info-in-teacher-self-serve-portal
          - text: Prototype PR
            href: https://github.com/fofr/teacher-self-service-portal-prototype/pull/5
          - text: Homepage content changes
            href: https://docs.google.com/document/d/11IZQXHu6bBZUwXzqJVheRv5XvwQ01xZ2tIXLQqfQoj4
---

When we launch [Find a lost TRN](/find-a-lost-trn), it will be easier to recover a TRN, and by extension, easier to sign in to the portal.

To reduce the risk posed by a bad actor gaining access to someone’s account we are:

- removing employment data
- removing address information
- hiding parts of email addresses, phone numbers and National Insurance numbers

Name, TRN and date of birth are used to sign in – they are known and do not need to be hidden.

## Design notes

The designs balances:

- the user need to see what information is stored, for example: to know if it is old and they need to update it
- the user need to easily update something
- the privacy needs outlined
- minimising design changes to a legacy service to keep technical changes small

We have also [improved content on the signed in home page](https://docs.google.com/document/d/11IZQXHu6bBZUwXzqJVheRv5XvwQ01xZ2tIXLQqfQoj4).

## Updating personal details

Users can still update their:

- email address
- phone number
- name
- date of birth
- National Insurance number

We are splitting the single contact details form into two:

1. Update your email address
2. Update your phone number
3. Removing the address form

### Validation

Form values for email, phone and National Insurance number will show redacted values. If a form is submitted with the redacted value it should be a no-op (users are known to submit forms to leave a page).

When submitting a National Insurance number or phone number, if the value submitted does not match the redacted value but still contains asterisks (*), we need to show a validation error.

When submitting an email address, an asterisk is a valid character in the local part of the address (the bit before the @). If the domain part (the bit after the @) of the address contains asterisks (*), we need to show a validation error.

Submitting a blank value should continue to behave as it does currently.

We may have validation rules that handle some of this already.

## Redaction

### Email

`jane.doe@example.com` becomes `j***@***.com`
`jj@example.sch.uk` becomes `j***@***.sch.uk`

We always use the same number of `*` to hide the real length of an email and to make it less guessable. This is instead of replacing each character with an asterisk.

There is a risk that a longer or shorter redacted email could confuse the user – it can imply a different email address to the one on record.

We hide the domain part as this may be an employer.

### Phone number

`07123456789` becomes `07*******89`

### National Insurance number

`QQ 12 34 56 C` becomes `QQ ** ** ** C`.
