---
title: Changing the email inviting people to use the service
date: 2023-09-28
---

We wrote an email [inviting people to use the service](/check-the-record-of-a-teacher/inviting-people-to-use-the-service).

We’ve changed the email so that it no longer mentions that a teacher’s record will say if they’re on the children’s barred list.

The children’s barred list should usually be checked as part of an enhanced Disclosure and Barring Service (DBS) check.

In some circumstances, users are allowed to check the children’s barred list separately. We’ve created a new service to allow them to do this.

The ‘find a teacher’ function in the Employer Access service does not mention the list but does include results from it. We’ve decided to do the same in the teacher record in the new service.

We may decide later to stop showing results from the list in the teacher record. We do not want to encourage users to rely on checking the children’s barred list as part of checking a teacher’s record.

## How we’ll invite people to use the service

Initially we’ll send an email to all users of Employer Access who work for teacher supply agencies.

{% from "email/macro.njk" import appEmail %}
{{ appEmail({
  subject: "You can now check a teacher’s record using a new service",
  content: "

Dear ((name))

You can now check a teacher’s record using a new service, instead of using Employer Access:

[link to the new service]

The new service allows you to search for a teacher using their last name and date of birth. You do not need their teacher reference number (TRN).

A teacher’s record includes their qualifications and also tells you if they:

- failed their induction or probation
- have been banned from teaching by the Secretary of State for Education
- have been sanctioned by the General Teaching Council for England (GTCE)

You do not need to check separate lists or make other searches to find out about these restrictions in the new service.

### Get help

Email employer.access@education.gov.uk if you have questions about the new service for checking a teacher’s record.
"
}) }}

Later we’ll invite people from other types of organisation. We'll send them a [different email] if we’re also inviting them to use the separate service to check the children’s barred list.
