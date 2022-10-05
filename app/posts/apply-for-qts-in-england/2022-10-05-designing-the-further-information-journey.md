---
title: Designing the further information journey
date: 2022-10-05
screenshots:
items:
- text: "Application list"
- src: application-list.png
- text: "Assessor task list"
- src: assessor-task-list.png
- text: "Select further information reasons"
- src: select-fi-reasons.png
- text: "Play back further information reasons"
- src: playback-fi-reasons.png
- text: "Service start page"
- src: further-information-start.png
- text: "Further information task list"
- src: further-information-task-list.png
- text: "Question to applicant"
- src: question-to-applicant.png
- text: "Application status change"
- src: received-further-information-status-change.png
- text: "Review requested information task active"
- src: review-requested-active.png
---

The QTS further information request journey sees assessors communicating back and forth to track down and confirm receipt of missing or incomplete information.

At the moment, it’s handled by email through Zendesk, with assessors contacting applicants to explain what they need, and applicants sending any documents as attachments.

## Types of further information

There are 2 broad categories of further information request. The first is where further information is requested from applicants themselves. The second category is information requested from a third party, commonly a competent authority, although it could be a school or workplace.

As we know further information requests from applicants are more numerous, and more pressing to get right for the end user, we’re focussing on those for MVP.

## The problem

The current system is a manual, labour-intensive, almost bespoke approach that lends itself to large banks of emails, confusion as to what’s required, and documents that are not clearly named (and do not always find their way to the correct application).

The process can easily become a back and forth volley between assessor and applicant, with numerous emails and phone calls. That simply cannot be scaled up once the new regulations are in force, large numbers of new countries come online, and the number of applicants skyrockets.

What’s needed is a standardised, scalable approach that’s consistent and repeatable for any applicant from any country.

## User needs

### As an assessor

* I need to know a case is on hold awaiting further information so that the application isn't worked on.
* I need to know what information is missing and what results in a decline or further information request so that the application is being correctly and fairly assessed.
* I need to know further information has been received so that I can continue the assessment of the application.

### As an applicant

* I need to know if I have missed any evidence needed and guidance on how to obtain it so that I can gather evidence and supply it.

## Part 1 – helping the assessor to request further information

Assessors will see the case list shown below, with details and statuses of current applications. From here, they can open up an application and begin their assessment.

![Application list](application-list.png)

The application view is presented as a task list, much like the one applicants see. Assessors need to work through the application, deciding whether each of the sections has been completed to their satisfaction.

The part of the task list that allows them to make a recommendation on next steps only becomes active once they’ve reviewed all of the sections.

![Assessor task list](assessor-task-list.png)

If the assessor marks everything as being completed to their satisfaction, they’ll be given the option to award QTS or to ask a colleague for a review.

Where something is wrong or missing, they’ll be given a list of reasons to choose from, with the opportunity to write short explanatory notes directly to the applicant.

![Select further information reasons](select-fi-reasons.png)

Some of the reasons require a further information request, while others result in a straight decline.

If an application has both, then the decline reason effectively outranks the further information reasons. Here. the assessor will be given the option to either decline QTS or request a review.

However, if the assessor notes 1 or more reasons that require further information (with no straight declines), they’ll be routed to the further information request journey.

On the next screen, they’ll see a playback of the reasons for requesting further information (that they selected earlier), along with any notes they added. There’s then a chance to review the email, which for MVP will be a standardised email.

![Play back further information reasons](playback-fi-reasons.png)

## Part 2 – making it easy for the applicant to respond

Once the assessor has submitted their request, the applicant will receive an email telling them that they need to supply more information with a link to sign back in.

When they follow the link and sign in, that triggers another email with a magic link that takes them to a landing page setting out what they need to do next.

![Service start page](further-information-start.png)

Once they select ‘Start now’, they’ll get a task list very similar to the one they worked through when they submitted their original application.

We know consistency throughout the journey is important to applicants – further interactions that are similar to what they’ve seen before have landed well in user research.

We’ve found that users are more comfortable in knowing what’s required of them if the design and content carry over the look and feel of their experience so far.

> "So far so good. I understand this completely. There's no confusion here."

> "No, very straightforward. Very simple."


![Further information task list](further-information-task-list.png)

The task list sets out the areas of the application that need more information. As they select each one, they'll see the specific reason that information is needed, the notes from the assessor, and either a free text box for questions, or an upload interaction where a document is needed.

![Question to applicant](question-to-applicant.png)

Once they’ve completed the task list, they’ll be able to submit their further information, at which point they’ll see a standard 'Submit’ screen and receive a confirmation email.

## Part 3 – back to the assessor

When the applicant submits their further information, it triggers a status change in the application, to ‘Received further information’, which lets the assessor know they can pick up the application again.

![Application status change](received-further-information-status-change.png)

It also makes the ‘Review requested information from applicant’ part of the task active, allowing the assessor to follow the link and review the further information that the applicant has provided.

![Review requested information task active](review-requested-active.png)
