---
title: Preliminary check (part 2)
date: 2023-07-27
screenshots:
items:
- text: Assessor is about to decline an application
- src: about-to-decline.png
- text: Application overview after being declined
- src: application-overview-declined.png
- text: Application overview before the preliminary check
- src: application-overview-preliminary-check.png
- text: Assessor checks the email
- src: check-email.png
- text: Assessor has declined the application
- src: declined.png
- text: Assessor performs the preliminary check
- src: preliminary-check.png
---

### Background

In March 2023, we launched a feature called ‘Preliminary checks’. This allowed Teaching Regulation Agency (TRA) admin to quickly check an applicant’s eligibility for QTS by reviewing their qualifications.

The feature allowed admin to move through applications quickly to identify and decline ineligible applicants.

After observing how the feature was used, it was clear that there were efficiencies we could make to the way admins interact with the preliminary check process.

### User needs we’ve tried to meet

As an admin staff member, I need to be able to quickly identify applications that are clearly ineligible so that I can decline them rather than passing them on to assessors.

### What we’ve done

We’ve made the assessment process more focused by asking admins to check just 2 criteria: that the applicant’s qualifications meet the required academic level and that the applicant is qualified to teach a specific age range.

To save time we've removed the need for admins to create decline reasons when responding to applicants. This part of the process has now been automated.

We've placed the assessment questions and certification documents on the same page. This means admins no longer need to move across different screens within the case management system (CMS).

### How it works

To streamline the process we’ve removed all spokes in the assessment section except for ‘Preliminary check (qualifications)’.

![Application overview before the preliminary check](application-overview-preliminary-check.png)

On the main assessment page, we’ve included all relevant information needed to make a judgement on eligibility. Admins are now able to access qualification certificates, review the list of checks to make, and answer 2 ‘Yes’ or ‘No’ questions.

![Assessor performs the preliminary check](preliminary-check.png)

Assessment questions:

1. Does the teaching qualification meet the required academic level? (Level 6 or higher)

2. Is the applicant qualified to teach one of the subjects we currently accept?

If the admin answers ‘Yes’ to both questions, the application is moved into full assessment.

If the answer to one or both questions is ‘No’, then the application is directed through the decline journey, with the system pulling through the decline reasons.

The application will move straight to a ‘Declined’ status, skipping the initial assessment altogether as shown in the screenshot below.

![Assessor is about to decline an application](about-to-decline.png)

We provide a description of the reason(s) for declining the application. This means that admin do not need to spend time writing their own response or copying and pasting pre-made statements.

The following page displays a preview of the email that will be sent to the applicant to confirm the outcome of their application.

![Assessor checks the email](check-email.png)

Next we confirm to admin that the application has been declined.

![Assessor has declined the application](declined.png)

Finally, the application status is updated to ‘DECLINED’ and the preliminary check pre-assessment task status shows as ‘COMPLETED’. A case history note will then be applied, which states “Qualifications: NOT PASSED”, followed by the decline reason.

![Application overview after being declined](application-overview-declined.png)

### Future considerations

In future, we could use this pattern to set -up country-specific preliminary check journeys that focus on different assessment spokes, for example, work history.

During testing, admin used a spreadsheet to check what qualifications the TRA can accept. The spreadsheet also recorded any newly received qualifications that are pending approval from policy personnel. For the service to be more comprehensive, we should consider how we design out the need for assessors to use external documents/platforms.
