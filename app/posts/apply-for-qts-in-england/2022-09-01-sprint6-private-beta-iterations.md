---
title: Private beta design history updates (Sprint 6)
date: 2022-09-01
screenshots:
items:
- text: "Award QTS"
- src: award-qts.jpg
- text: "Request second review"
- src: request-second-review.jpg
- text: "Dynamic content in application form"
- src: dynamic-application-content.jpg
---

### Working on the assessor view

Over the last two sprints, we’ve been focussing on the assessor side of Apply for QTS.

On one level we’ve been working to set out exactly what MVP will be for go-live, but we’ve also been thinking ahead to what we’ll be able to build for assessors further along the line.

MVP is likely to give assessors a one-stop view of everything that an applicant has entered and uploaded, putting everything in one place. That way, it’s easy for them to take a decision on whether to award or decline QTS.

![Save 'In progress' application](save-in-progress-application.png)

There’ll also be a basic level of functionality for requesting further information, which will initially lead into a manual email exchange.

Future iterations will provide a complete approach to requesting further information from the applicant (and from a third party, such as a competent authority). We’ll also have built-in functionality that allows assessors to request a second review from an assessor colleague, which will be more important as new countries come online.

![Request second review](request-second-review.jpg)

A large part of the work over the last few weeks has been given over to working directly with the assessors, to understand their needs and to walk them through the ideas we’re working on.

As part of that, we’ve been working to understand exactly what they're looking for when they review an application, as well as what would constitute an immediate decline and what would trigger a further information request.



### Streamlining user comms

The current system holds a large number of emails. They cover all the situations in which further information might be requested, as well as all the variations of decline notices that we might need to send out. At the moment, they’re held in a disparate repository by country or state, but with many more countries set to come online in future, that approach will be unsustainable.

Despite the country-specific information, much of the email content is actually transferable, so we’ve been working to design a streamlined suite of emails (around 7 or 8 in total) that will work for every country and state. Some, such as an award notice, can be sent with no bespoke content at all, but where the content needs to change for the application in question, the emails will automatically pull through the further information or decline reasons from the assessor’s review.

There’ll also be an optional free text box for the assessors to add any clarifying notes if they need to. Crucially, the new emails are set out in a much more standard GOV.UK style, with clear headings leading the reader through from the subject line, to what we’re telling them or asking them about and what they can do next.



### Updates to the application form

The user-side application form has taken a back seat in recent weeks, but we’ve still been working on tweaks to make it easier for users to know exactly what they need to provide.

For a handful of states and territories where we accept something other than ‘full’ recognition as a teacher, we need to let users know what they can apply with. The challenge comes from this kind of interim or provisional status being called different things in different countries.

As we’re working with a small number of instances, and so as not to undermine the workings of the dynamic ‘bucket’ content, we’ve been using the ‘other’ field that the developers added to the support console. It means we can add a simple line of copy in a standardised format that tells users which types of status we can accept. In time, we’ll also be able to pull that extra field through to the assessor view.


![Dynamic content in application form](dynamic-application-content.png)
