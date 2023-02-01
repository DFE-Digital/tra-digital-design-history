---
title: Changing the automated email reply for getting help
date: 2023-02-01

---

{% from "email/macro.njk" import appEmail with context %}

When a user emails 'misconduct.teacher@education.gov.uk' to get help, they receive an automated email reply.

This email gives details of when the user can expect to receive a response, depending on their request. For example, if they have questions about an existing case.

At the moment, the email includes:

- different acronyms and service names, for example TRA and Teacher Misconduct Unit (TMU)
- language that does not follow the [GOV.UK Style guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style), such as ‘receipt of your correspondence’, ‘please’, ‘thank you’

So we changed the content to make it clearer and simpler.


<!-- markdownlint-disable MD025 MD001 -->
{{ appEmail({
  subject: "Your email has been received",
  content: "

Your email has been received.

You’ll get a response within:

- 1 working day if your request is about attending a hearing
- 3 working days if your request is about the online referral service
- 15 working days if your request is about an existing case or anything else

If you’ve sent a new referral, response times can vary. 

Read more about response times:

https://www.gov.uk/government/publications/teacher-misconduct-disciplinary-procedures

Call 0207 593 5393 if your request is urgent.

  "
}) }}


