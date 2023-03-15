---
title: New regulations part 3 – Requesting references
date: 2023-03-15
screenshots:
items:

- text: "Check your answers"
- src: check-your-answers.png
- text: "Email applicant"
- src: email-applicant.png
- text: "Email referee"
- src: email-referee.png
- text: "About you question"
- src: question-about.png
- text: "Age question"
- src: question-age.png
- text: "Comments question"
- src: question-comments.png
- text: "Dates question"
- src: question-dates.png
- text: "Hours question"
- src: question-hours.png
- text: "Misconduct question"
- src: question-misconduct.png
- text: "Planning question"
- src: question-planning.png
- text: "Reporting question"
- src: question-reporting.png
- text: "Suitability question"
- src: question-suitability.png
- text: "Request references"
- src: request-references.png
- text: "Response submitted"
- src: response-submission.png
- text: "Service start page"
- src: start.png
---


### Background

Unlike the previous qualified teacher status (QTS) regulations, where we only asked for references for an applicant’s current or most recent role, the new regulations require references from every role that the applicant tells us about.

Due to the anticipated numbers of applications under the new regulations, we need to make the process of requesting references as smooth and automated as possible. Since we’re asking for a reference for every role, it’s important to make sure the applicant understands the kinds of roles we can consider, and which roles we cannot count as part of their experience.

When the applicant first enters the ‘Work history’ spoke of the application form, they’ll see a summary of the requirements that all roles must meet. They need to check a box to confirm they understand that they should only tell us about roles that meet the following requirements.

* They were qualified to teach before starting the role.
* They worked with children aged between 5 and 16 years.
* They were responsible for planning, preparing and delivering lessons to at least 4 students at a time.
* They were responsible for assessing and reporting on the progress of those students.

From here, each time they enter a role, they’ll need to add the name, job title and email address of someone who can verify that they worked in that institution across the dates they’ve provided.

### What the assessor will see

When an assessor has worked through all the sections of an application and is ready to award QTS, they’ll move through the references flow. They’ll see the following screen with the references prepopulated and ticked by default for all the roles the applicant has entered.

![Request references](request-references.png)

At this point the assessor still has the ability to uncheck a reference if they need to. In doing so, should the references then fall below the minimum 9-month threshold, they can send a further information request to the applicant.

If the assessor is happy to proceed, they’ll see a preview of the email that each person providing a reference will receive, followed by a preview of the email the applicant will receive telling them we’ve contacted their references.

![Email referee](email-referee.png)
<br>
![Email applicant](email-applicant.png)

### What the person providing the reference will see

In building the reference-side journey, we were able to repurpose what we’ve already built for the [request information from applicant journey](https://tra-digital-design-history.herokuapp.com/apply-for-qts-in-england/designing-the-further-information-journey/).

As with requesting further information, the person providing a reference will receive an email, followed by a one-time password (OTP) that takes them to the journey they need to complete.

With the eventual roll-out to almost 200 countries, we know it may not always be easy for applicants to provide references from people who have a good grasp of English. For that reason, instead of asking them to provide a freeform response that covers all the required information, we’ve built a series of Yes/No questions, that map directly to the policy requirements.

Before we take the person providing a reference through the questions about the applicant, we replay what they’ve been asked to do. We then show them a screen that asks them to confirm their own details. If there are any discrepancies with what the applicant has told us, the person providing a reference can edit their own details and the assessor will see this played back when the reference is received.

![Service start page](start.png)
<br>
![About you question](question-about.png)

We then ask a series of 7 questions. In each case, if the applicant answers ‘No’ (or ‘Yes’ in the case of questions about misconduct and suitability to work with children), we’ll show a free text box that allows them to briefly explain their answer.

![Dates question](question-dates.png)
<br>
![Hours question](question-hours.png)
<br>
![Age question](question-age.png)
<br>
![Planning question](question-planning.png)
<br>
![Reporting question](question-reporting.png)
<br>
![Misconduct question](question-misconduct.png)
<br>
![Suitability question](question-suitability.png)

Once they’ve worked through the Yes/No questions, there’s an optional question that allows them to add any other concerns they may have.

Initially this question was much more open-ended, asking them whether there was anything else that they’d like to tell us about the applicant. However, user testing showed that people often felt compelled to write a lengthy character reference here.

As we’re only really interested in concerns at this point, we’ve rephrased the question to reflect that.

![Comments question](question-comments.png)

Once the reference is complete, there’s a standard ‘Check your answers’ screen, which includes a link to our privacy policy and a declaration before submitting the answers.

![Check your answers](check-your-answers.png)

Finally, the person providing the reference will see a ‘Submitted’ screen, which reassures the user that they do not need to do anything else.

![Response submitted](response-submission.png)
