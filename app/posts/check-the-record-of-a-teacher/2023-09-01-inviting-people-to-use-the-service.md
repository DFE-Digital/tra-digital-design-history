---
title: Inviting people to use the service
date: 2023-09-01
---

Initially we’ll only allow people from teacher recruitment agencies to use the Check the record of a teacher service.

The current Employer Access service has around 1000 users from around 350 recruitment agencies.

We’ve chosen this group because:

- they do not need the ‘add to my organisation’ function in Employer Access - we have not yet decided whether to offer a similar function in the new service
- they only need to search for teachers in the Children’s Barred List - if they needed to search for other people, they’d need the separate service which will not launch immediately

We’ll automatically give these users access to the service. They will not need to request access or provide extra information.

## Email

{% from "email/macro.njk" import appEmail %}
{{ appEmail({
  content: "

Subject: Employer Access is being replaced by a new service

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

If we find that few people start using the new service, we’ll consider:

* sending further emails
* putting a banner in the Employer Access service
