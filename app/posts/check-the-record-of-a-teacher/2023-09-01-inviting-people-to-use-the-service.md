---
title: Inviting people to use the service
date: 2023-09-01
---

Initially we’ll only allow people from teacher recruitment agencies to use the new service to check the record of a teacher.

The current Employer Access service has around 1000 users from around 350 recruitment agencies.

We’ll automatically give these users access to the new service. They will not need to ask for access or give extra information.

## Why we’re inviting users from recruitment agencies first

We’ve chosen to start with users from recruitment agencies because they do not need to be able to:

- add teachers to their organisation within the service
- check whether people other than teachers are on the Children’s Barred List

### Adding a teacher to an organisation

Some types of users can add teachers to their organisation in Employer Access. They can see a list of all teachers who have been added to their organisation.

We need to do research to find out how useful this feature is. We have not yet decided whether to offer a similar feature in the new service.

Recruitment agencies do not need to add a teacher to their organisation. The school which employs the teacher can instead add the teacher to their organisation.

### Checking the Children’s Barred List

The Children’s Barred List is maintained by the Disclosure and Barring Service.

People on the list are not allowed to work with children. This includes teaching roles and also other jobs.

Recruitment agencies are only allowed to check the list for people applying to work as teachers. The agencies can do this using the new service to check the record of a teacher.

Some types of users can check the Children’s Barred List separately. We will launch a [separate service](/check-the-childrens-barred-list/) to allow this.

## How we’ll invite people to use the service

We’ll send an email to all users of Employer Access who work for recruitment agencies.

{% from "email/macro.njk" import appEmail %}
{{ appEmail({
  subject: "Employer Access is being replaced by a new service",
  content: "

Dear ((name))

You can now check the record of a teacher using a new service:

[link to the new service]

You can search for a teacher using their last name and date of birth. You do not need their teacher reference number (TRN).

A teacher’s record includes their qualifications and also tells you if they:

- are on the Children’s Barred List
- have been banned from teaching by the Secretary of State for Education
- failed their induction or probation
- have been sanctioned by the General Teaching Council for England (GTCE)
- have been banned or restricted from managing independent schools

You do not need to check separate lists or make other searches to find out about these restrictions.

After you try the new service, you’ll still be able to use Employer Access if you prefer.

We’ll contact you when a date has been set for Employer Access to be switched off.

### Get help

Email employer.access@education.gov.uk if you have questions about the new service for checking the record of a teacher.
"
}) }}


## Further considerations

We’re checking whether there are any professional organisations or forums for recruitment agencies. We could ask them to announce the launch of the new service.

If we find that few people start using the new service, we’ll consider:

* sending further emails
* adding a banner to the Employer Access service with a link to the new service
