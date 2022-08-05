---
  title: Don’t allow shared emails
  date: 2022-08-05
---

Now that we are [no longer giving a choice about accounts](/get-an-identity/no-account-choice/), we need to be sure that users are not signing in with emails that have shared access.

For example, if a user associates an account with `headteacher@`, and then they leave their job, the next headteacher could use that email address to see the person’s details. Equally, emails like `office@` often go to shared inboxes.

We can block commonly used shared email addresses.

## Common shared email addresses

If a user enters an email address with any of the following patterns, we will prevent them from continuing and ask them for another email address.

### Exact match

- headteacher@
- head@
- ht@
- info@
- office@
- admin@
- adminoffice@
- hello@
- enquiries@
- generalenquiries@
- post@
- headteacherpa@
- contact@
- school@
- academy@

### Wildcards

If the first part of an email address contains:

- headteacher
- admin
- office
- enquiries
- contact
- info
- school

## Error message

The error message will be:

> Enter a personal email address, not a shared one

Besides the input we will also give an example:

> For example, jane.doe@school.gov.uk

![Screenshot showing the error message to use](validation-message.png "Screenshot showing the error message to use")
