---
title: Telling users about the service
date: 2023-09-26
related:
  items:
    - text: Searching the DBS barred list
      href: /check-the-record-of-a-teacher/dbs-standalone-barred-list-search/
    - text: Inviting people to use the service
      href: http://localhost:8080/check-the-record-of-a-teacher/inviting-people-to-use-the-service/
---

The children’s barred list is usually checked as part of an enhanced Disclosure and Barring Service (DBS) check.

Some types of organisation are also allowed to check the list separately and will therefore be given access to this new service.

The organisations which can check the list separately are:

- schools
- colleges
- local authorities
- universities

We’ll invite users from these organisations to use the service during the private beta phase. We’ll do this at the same time as we invite them to use the service for checking a teacher’s record.

## How we’ll tell users about the service

We’ll send an email to all users of Employer Access who are allowed to use the new service.

{% from "email/macro.njk" import appEmail %}
{{ appEmail({
  subject: "Check a teacher’s record and the children’s barred list using new services",
  content: "

Dear ((name))

You can now use new services instead of Employer Access to:

- check a teacher’s record
- check the children's barred list

# Check a teacher's record

Use the new service to check a teacher's record:

[link to the new service]

This new service allows you to search for a teacher using their last name and date of birth. You do not need their teacher reference number (TRN).

A teacher's record includes their qualifications and also tells you if they:

- failed their induction or probation
- prevented from teaching by a prohibition order
- were sanctioned by the General Teaching Council for England (GTCE)

You do not need to check separate lists or make other searches to find out about these restrictions in the new service.

# Check the children's barred list

Use the new service to check the children's barred list:

[link to the new service]

The children’s barred list contains details of people who are not allowed to work with children.

The list is usually checked as part of an enhanced Disclosure and Barring Service (DBS) check before someone starts working with children at a school or college.

You should only use the new service if either:

- you want a new employee to start working with children while they wait for the result of an enhanced DBS check
- your new employee does not need an enhanced DBS check because they’ve worked with children in a school or college within the last 3 months

# Get help

Email [employer.access@education.gov.uk](mailto:employer.access@education.gov.uk) if you have questions about the new service for checking a teacher’s record.
"
}) }}

## Further considerations

If we find that few people start using the new service, we’ll consider:

- sending further emails
- adding a banner to the Employer Access service with a link to the new service
