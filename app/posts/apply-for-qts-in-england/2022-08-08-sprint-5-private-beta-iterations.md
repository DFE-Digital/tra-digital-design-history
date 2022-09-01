---
title: Private beta design history updates
date: 2022-09-01
screenshots:
items:
- text: "Tailored 'You're eligible' page"
- src: tailored-youre-eligible-page.png
- text: "Accordion for things you need"
- src: accordion-for-things-you-need.png
- text: "Cannot start university degree yet"
- src: university-degree-cannot-start.png
- text: "University degree not needed"
- src: university-degree-not-needed.png

---

## Connecting the eligibility checker and application form

Much of the sprint saw the developers building the application form, based on the prototypes we’ve been using and the learnings from 2 waves of user research. They’re building it into the new ‘Test’ environment, which we’ll be taking forward for user research in future.

A key focus of the ongoing iteration work has been joining the 2 parts of the journey (the eligibility checker and the application form) into one seamless flow. Up to now, the eligibility checker has functioned on its own – it’s currently live, but directs those who get through it successfully to the existing application form.

Ultimately, it needs to segue into the new application form, and to do that, we need to develop the ‘Save and return’ journey.

Once users successfully make their way through the eligibility checker and begin the form itself, there are key steps along the way that might see them taking a break and coming back. The obvious example is when it comes to document uploads – a user may realise they’re short of something and they’ll need to save their progress while they locate the missing document. They’ll then want to come back later to continue their application.


### Back through the checker

At first glance, a solution might be to email the user a link that would let them come straight back to where they left off. But there are issues with that. First, they might lose the email with the link in, so they wouldn’t have a way of getting back in. Secondly, the link should not last very long for security reasons.

What we need is a way of routing them back to the start of the service that makes it easy for them to skip the checker and carry on working. We’ve now added a ‘Save as draft’ button to the task list which signs the user out, explaining that we’ve saved their progress and giving them a clear set of instructions on what to do next, with a link to come back.

![Save 'In progress' application](save-in-progress-application.png)

The link takes them to the beginning of the eligibility checker, but we’ve modified the checker to ask all users whether it’s their first time using the service. If it’s not, they’ll have already entered their email into the application form, so they can enter it again here to skip the checker and go back to their part-completed form.

If they answer ‘No’, then they’ll need to go through the checker. It’s essential that anyone coming to ‘Apply for qualified teacher status (QTS)’ service for the first time goes through the checker. That makes sure we satisfy one of the key requirements of the build, which was to deal with the problem of applications being made by ineligible applicants.



### Other changes to the eligibility checker and application form

Beyond the save and return work, we’ve been tightening up the user experience of the checker and form. We know that the ‘Qualifications’ spoke is working well now, but we’ve been working to standardise the document upload interaction and we’ve made it possible to upload multiple pages for a single document.

We’ve also agreed the certified translation requirements and added copy around that, fine-tuned the requirement to see evidence of a name change and standardised the formatting of headings on the task list.

Finally, we've added a new page that allows those who do not yet have any work experience to tell us so, but still ‘complete’ that section of the form.

![No previous work experience](no-work-experience.png)

### Beginning the case management system

This sprint also saw the beginning of the work to build the case management system, which will be the main focus of the next sprint. So far, we have a working prototype that allows users to see a number of placeholder applications and their status.

![Application management](application-management.png)
