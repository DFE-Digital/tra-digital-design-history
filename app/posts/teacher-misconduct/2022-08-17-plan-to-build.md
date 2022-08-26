---
  title: How we can break down the Report serious misconduct build
  date: 2022-08-17
---

The full service, as designed, is large. There are over 50 distinct page designs to build, most have form fields which will need their own validations, models, etc.

We do not want to spend 6 months building a service without shipping.

We need to reduce scope and deliver the service in stages.

## Stage 1: Eligibility and step-by-step

The smallest parts of the service that can independently deliver benefits are:

- the eligibility screener at the beginning
- the step-by-step overview

### Step-by-step

We can independently write, test and iterate the step-by-step. It can be made available on GOV.UK long before the service is ready.

### Eligibility screener

We can use the eligibility screener at the beginning to direct people to the correct form to download - public or employer, and the screener will prevent people from downloading and completing fields unnecessarily.

With this build we would have:

- a small service deployed to production
- a production URL, and other environments
- other operational work, initial reporting, etc
- a start page

This would include the pages:

- Are you reporting as an employer or member of the public?
- Have you already made a complaint to the school, school governors or your local council?
- You should complain to the school, school governors or your local council first
- Is the allegation about a teacher?
- You can report someone who does unsupervised teaching work
- You need to report this misconduct somewhere else (not a teacher, out of jurisdiction)
- Were they teaching in England at the time the alleged misconduct took place?
- You need to report this misconduct somewhere else (location out of jurisdiction)
- Does the allegation involve serious misconduct?
- You need to report this misconduct somewhere else (not serious misconduct)
- What completing this report means for you
- A new page to download the form

## Stage 2: Employer form

The employer form is the bigger version of the form, but it is also the most used. By shipping this version first we get more benefits sooner.

Much of the employer form is shared with the public form.

A member of the public would continue to be directed to a downloadable form via the screener.

With this build we would also need:

- integration with Teacher misconduct system (TMS)
- a case worker view of the form (perhaps a PDF for TMS)
- a version of the form to send to the accused teacher

### Integration with TMS

If direct integration with TMS is complex, we might consider an email fallback.

On submission, a report could be emailed to TMS automatically, using the same address and process as the Word forms, along with any attachments. It would continue to be manually entered into TMS in the short term.

Directly integrating the service with the TMS could then be tackled separately.

Currently referral forms are manually added via the case record on TMS.

## Stage 3: Public form

When the employer form is built, and probably once it has been iterated and the form works end to end, the public version can be built.
