---
title: Private beta design history updates
date: 2022-07-25
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

## Eligibility checker updates from UR testing

In this sprint we switched on the eligibility checker for all the tranche 2 countries as well as all the countries and
states that fit into what we call ‘bucket 1’.

Bucket 1 countries and states are those with a competent authority that can provide, through an online service, both
proof of recognition for applicants and whether or not they have sanctions on their record.

In terms of content iterations, we’ve mainly focused on the application form, based on what we learned from wave 1 of
user testing.

However we’ve been looking at the qualifications content and it’s really important to make sure we update the
eligibility checker too, so the journey makes sense from beginning to end, and the questions we ask are presented in the
same order.

### Swapping the order of teacher training qualification and degree

In the checker, we found that asking about university degrees before teacher training qualifications was wrongfooting
those who have a single degree qualification that encompases their teacher training.

In these cases, having said ‘Yes’ to having a university degree, the applicants struggled to understand the next
question about a teacher training qualification, because they felt they’d already answered it.

To make it clear, and to fit with the updated application form, we now ask about the teacher training qualification
first. We then follow up with the degree question, but we clearly explain that this could be the same thing as their
degree, or a separate qualification.

### Clarifying sanctions

This was a quick fix, but an important one. We ask whether applicants have any sanctions on their record, but the old
hint text talked about the record being “free of” sanctions. It took some applicants a while to figure out whether to
answer yes or no.

With the new wording, the structure of both the question and the hint text take the “must have no” approach, making it
easier to understand.

### Tailored 'You’re eligible' page

The UR sessions showed us that while the idea of a tailored ‘You’re eligible’ page at the end of the checker was well
received, the copy around qualifications needed more clarity (fitting with the key theme) and it was also long – long
enough for people to switch off and miss things.

To deal with the first point, the copy is now much clearer – we explain again that their teacher training qualification
and university degree may be the same thing, or 2 separate qualifications and we also explain what a ‘transcript’ is.

To deal with the length of the page we added 2 existing GOV.UK components. First, we use the ‘Inset text’ pattern to
make it very clear at the beginning, that even if they’re eligible, they may need to take time to gather all the things
they’ll need to apply.

![Tailored 'You're eligible' page](tailored-youre-eligible-page.png)

Second, we used the ‘Accordion’ pattern to truncate the list of things they’ll need, so now they see the 3 categories –
Proof of identity, Proof of qualifications and Proof that you’re recognised at a teacher.

They can then expand the accordion to read the detail, but the page looks far less overwhelming.

![Accordion for things you need](accordion-for-things-you-need.png)

## Building the application form

Before we went into testing, we knew we’d have applicants with separate university degrees and teacher training
qualifications, as well as those with specific teaching degrees that cover both.

However, what we also discovered was that some applicants with a teaching degree want to tell us about further degree
qualifications, even though they don’t have to.

What that means is the content needs to satisfy 3 broad types of applicants:

1. Those with a teacher training qualification and a separate university degree.
2. Those with a degree that encompasses their teacher training.
3. Those whose degree encompasses their training, but with other degrees that they want to tell us about.

The key to this is building a journey that allows applicants to upload multiple documents both where they need to as
well as where they do not need to, but choose to.

Even if they have a single qualification, they still need to upload a transcript and possibly a translation, so a
multiple upload journey is a must.

![Cannot start university degree yet](university-degree-cannot-start.png)

The route we’ve built and will be taking onto wave 2 of user research aims to serve the applicant with only the copy
they need to see. We open with the teacher training qualification path, where we ask for the title of the qualification,
the institution where they obtained it and their start and end dates. They then progress to an upload interaction, with
the option to upload a translation, followed by a similar interaction for the transcript of that qualification.

After we play back the information they’ve given us and they confirm they’re happy, we then ask them “Add another
qualification?”. Here we explain that if their teacher training qualification was a standalone course, they must also
add a degree. We also explain that if their degree encompassed their training too, they do not need to add another
qualification, but they can if they want to.

If they answer ‘Yes’ (either because they need to add a separate degree, or they choose to add an additional one), when
they return to the task list they’ll be able to move to the ‘University degree’ journey, which behaves much like the
teacher training path.

If they answer ‘No’, when they get back to the task list they’ll see that ‘University degree’ says ‘Not needed’.

![University degree not needed](university-degree-not-needed.png)
