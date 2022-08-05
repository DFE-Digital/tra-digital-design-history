---
  title: Removing the account choice
  date: 2022-08-05
  related:
    sections:
      - title: Related content
        items:
          - text: Prototype PR
            href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/131
---

Originally we tested a version of the design where:

- at the end of the journey users could decide whether to make 'an account'
- we gave reasons why they might return
- users could change the email address they would use for their account
- users could choose not to associate their account with an email
- we gave guidance on not using shared email addresses

However, in practice and given the technical implementation, this is not a true choice. We would still be creating a central record for them in Get an identity. Users who chose not to create an account would just be missing out on the shortcut.

When we tested this page in research we found that:

- people did not change their email address
- the account was not controversial
- no one decided not to create an account

## Design changes

We have [removed the 'Next time' page](/get-an-identity/npq-without-a-trn/#first-time-user-next-time-you-use-this-service).

We are keeping the note about skipping these questions on the [continue to service page](/get-an-identity/npq-without-a-trn/#first-time-user-finished-asking-questions).

The use of shared email addresses is still a valid concern, but we will put in place validations to prevent people from using them ([Trello ticket](https://trello.com/c/Bhm8DSAB/600-add-validations-to-prevent-sign-up-with-common-shared-email-addresses)), for example we will block `head@` or `headteacher@`.
