---
title: Inviting people to use the service
date: 2023-09-06
---

Initially we’ll only allow people from teacher supply agencies to use the new service to check the record of a teacher.

The current Employer Access service has around 1000 users from around 350 teacher supply agencies.

We’ll automatically give these users access to the new service.

## Why we’re inviting users from teacher supply agencies first

We’ve chosen to start with users from teacher supply agencies because they:

- can check the Children’s Barred List as part of checking a teacher’s record
- do not need to add teachers to their organisation within the service

### Checking the Children’s Barred List as part of checking a teacher’s record

The Children’s Barred List is maintained by the Disclosure and Barring Service (DBS).

People on the list are not allowed to work with children. This includes teaching roles and other jobs.

In both Employer Access and the new service, the teacher record shows if a teacher is on the Children’s Barred List.

Some types of users can check the Children’s Barred List separately. We will launch a [separate service](/check-the-childrens-barred-list/) to allow this.

Teacher supply agencies are not allowed to check the list separately.

### Not needing to add a teacher to an organisation

Some types of users can add teachers to their organisation in Employer Access. They can see:

- a list of all teachers who have been added to their organisation
- which school a teacher is currently working for, if the school has added them to their organisation

We need to do research to find out more about the user needs which this feature currently meets. We have not yet decided whether to offer a similar feature in the new service.

Teacher supply agencies do not need to add a teacher to their organisation. The school which employs the teacher can instead add the teacher to their organisation.

## How we’ll invite people to use the service

We’ll send an email to all users of Employer Access who work for teacher supply agencies.

{% from "email/macro.njk" import appEmail %}
{{ appEmail({
  subject: "You can now check a teacher’s record using a new service",
  content: "

Dear ((name))

You can now check a teacher’s record using a new service, instead of using Employer Access:

[link to the new service]

The new service allows you to search for a teacher using their last name and date of birth. You do not need their teacher reference number (TRN).

A teacher’s record includes their qualifications and also tells you if they:

- are on the Children’s Barred List
- have been banned from teaching by the Secretary of State for Education
- failed their induction or probation
- have been sanctioned by the General Teaching Council for England (GTCE)

You do not need to check separate lists or make other searches to find out about these restrictions in the new service.

### Get help

Email employer.access@education.gov.uk if you have questions about the new service for checking a teacher’s record.
"
}) }}


## Further considerations

If we find that few people start using the new service, we’ll consider:

* sending further emails
* adding a banner to the Employer Access service with a link to the new service
