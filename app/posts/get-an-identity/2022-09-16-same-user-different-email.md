---
  title: When a user returns with a different email
  date: 2022-09-16
  related:
    sections:
      - title: Related content
        items:
          - text: Trello ticket
            href: https://trello.com/c/pfgkPrPF/700-designs-for-the-same-user-returning-with-a-different-email
          - text: Prototype PR
            href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/153
---

Consider the journey:

- a user has previously been through the Get an identity journey, they matched a record and used the email address, "jane.doe@school.gov.uk"
- later, they return to the service, but this time they use, "jdoe54@gmail.com"
- because the email address is new, we ask for their details again and try to find a match
- they give us the same details, and we match the same record, but now the emails are different

This design decides what will happen in this scenario. During MVP we expect this scenario to be rare.

## When the user matches but the email doesn’t

After the user has given their details and we’ve matched their record, and following the ‘Check your answers’ page, we will:

- highlight that there is an existing email address that is different
- show a redacted version of that email address
- ask them to confirm access to that address, by entering a code

We will use the [same email redaction pattern to the one we implemented on Teacher Self-service](https://github.com/DFE-Digital/dqt-web-portal/blob/main/src/Dqt.Portals/Tests/DqtWebPortals.Tests/RedactionHelperTests.cs#L8-L22).

![Your email address is different to the one on record](01-your-email-address-is-different.png "Your email address is different to the one on record")

## If they can access their old email

After giving a successful code, we’ve confirmed they have access to that email address and they can continue.

Before they leave, we ask which email address they’d like to use. We can show their old email address in full now.

![Which email address do you want to use?](02-which-email-address-do-you-want-to-use.png "Which email address do you want to use?")

## If they cannot access their old email

It’s a bit more complicated if they:

- cannot access the old email address
- do not recognise the old email address

In this case we need to direct them to support, and they need to prove their identity with TRA. After proving their identity, TRA will update the user’s email address on their behalf.

![You need to prove your identity](03-you-need-to-prove-your-identity.png "You need to prove your identity")
