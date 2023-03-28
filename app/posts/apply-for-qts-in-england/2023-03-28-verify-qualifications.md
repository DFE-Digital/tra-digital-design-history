---
title: Verifying qualifications
date: 2023-03-28
screenshots:
items:

- text: "Consent letter"
- src: consent-letter.png
- text: "Ecctis dashboard"
- src: ecctis-dashboard.png
- text: "Ecctis verification history"
- src: ecctis-verification-history.png
- text: "Qualification accepted"
- src: qualification-accepted.png
- text: "Qualification rejected"
- src: qualification-rejected.png
- text: "Waiting on qualification response"
- src: qualification-waiting-on.png
- text: "Response reviewed"
- src: response-reviewed.png
- text: "Select qualifications to verify"
- src: select-qualifications-to-verify.png
- text: "Task completed"
- src: task-completed.png
- text: "Waiting on task"
- src: task-waiting-on.png
- text: "Verification steps"
- src: verification-steps.png
- text: "Would you like to verify qualifications?"
- src: verify-qualifications-question.png
---

As application numbers increase in the Apply for qualified teacher status (QTS) in England service (through the rollout to new countries) assessors need the ability to verify a percentage of the qualifications that applicants provide.

As with [verifying letters of professional standing](https://tra-digital-design-history.herokuapp.com/apply-for-qts-in-england/verify-lops/), the new feature needs to allow the assessors to ‘spot check’ qualifications, unlike ‘Verifying references’ where the default is to follow up all the references for every application.

With qualifications, assessors need to be able to choose for each application whether they verify qualifications at all and within that, whether they verify all of the qualifications or a selection of them.

### Why it matters

Expanding the service to many more countries means a large increase in the number of applications being received. As part of that, it’s important to be able to verify the evidence that applicants are providing and to be able to choose how often the TRA does this.

### User needs being met

* As an assessor I need the option to verify one or more of an applicant’s qualifications with Ecctis, so that I can progress the application.

* As an assessor I need to know verification of qualifications has been received so that I can continue the assessment of the application.

### Choosing to verify qualifications

Like verifying references (and unlike verifying letters of professional standing), it’s quite common that an applicant will have submitted more than one qualification as part of their application. For that reason, if the assessor chooses to verify qualifications, we show them a screen that plays back all of the qualifications with check boxes, much like the references journey.

![Would you like to verify qualifications?](verify-qualifications-question.png)
<br>
![Select qualifications to verify](select-qualifications-to-verify.png)

As with references, all the checkboxes are ticked by default, but the assessor can deselect those that they do not want to verify.

Once they’ve chosen which qualifications they want to follow up, we give a brief explanation of their next steps and what they can expect to see on the task list while those steps are in progress.

![Verification steps](verification-steps.png)

### Contacting Ecctis

From this point, the process for verifying qualifications exists largely outside the new system, and will remain so for the time being. That’s because the route involves contacting the applicant with a consent letter in which they give the TRA permission to check the validity of their qualifications.

In many cases, the assessor is able to email the applicant a standard consent note, which they can complete and return. However, some institutions require their own consent letters to be sent out to the applicant, which the assessor would only know once they look up that institution on the Ecctis portal.

![Consent letter](consent-letter.png)

Once the assessor has understood, sent and received the required consent letters, they need to submit a separate verification request per qualification to Ecctis, and it’s these responses from Ecctis that we need to be able to record and review.

Unlike the ‘Verify letter of professional standing’ journey, which is a two-step process (because more than one person may be working on that part of the assessment), the ‘Verify qualifications’ process is a one-step process. It both acknowledges receipt of a response from Ecctis and confirms whether or not that response shows the qualification to be acceptable.

The reason for the difference is that assessors can use the Ecctis portal dashboard to see all the verification requests no matter who requested the verification, and where each of those cases is up to.

For that reason, it’s unnecessary for our service to capture and play back information on where to find the response and overly time-consuming for the assessor (who in most cases will be carrying out the whole process).

![Ecctis dashboard](ecctis-dashboard.png)
<br>
![Ecctis verification history](ecctis-verification-history.png)

When a response is received, the assessor can come back into the service and use the ‘Verify LOPS’ link on the task list. This status will only ever show as ‘Waiting on’, ‘Completed’ or ‘Overdue’ if the response has not been received within 30 working days.

![Waiting on task](task-waiting-on.png)

When a response is received (or 30 working days have passed without receiving one) the assessor can use the ‘Record qualifications responses’ link to get to the overview page, where they’re able to see the list of qualifications. From there, they can access a page for each individual qualification.

![Waiting on qualification response](qualification-waiting-on.png)

On these individual pages, for  each qualification we ask an initial question about whether or not a response has been received. If so, we then ask the assessor whether, having reviewed it, the response shows that the qualification is legitimate.

![Response reviewed](response-reviewed.png)

Depending on whether they answer ‘Yes’ or ‘No’, the listing for that qualification on the overview page will show as either ‘Accepted’ or ‘Rejected’.

![Qualification accepted](qualification-accepted.png)
<br>
![Qualification rejected](qualification-rejected.png)


Only when the overview page shows a status of ‘Accepted’ or ‘Rejected’ by every qualification can the ‘Verify qualifications’ task show as ‘Completed’ on the task list. If any qualifications remain in ‘Waiting on’ or ‘Overdue’ the task cannot be completed until the assessor returns and marks them as either ‘Accepted’ or ‘Rejected’.

![Task completed](task-completed.png)
