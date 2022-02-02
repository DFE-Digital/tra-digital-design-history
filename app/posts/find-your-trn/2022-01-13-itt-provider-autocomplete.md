---
  title: Auto-completion when choosing an ITT provider
  date: 2022-01-13
  screenshots:
    items:
      - text: "Suggestions"
      - text: "Choice made"
---
In order to retrieve their TRN, teachers are asked a series of questions. [One such question prompts the teacher for the name of their initial teacher training (ITT) provider](/find-your-trn/iteration-2/#have-you-ever-been-enrolled-in-initial-teacher-training-in-england-or-wales).

In the [Iteration 3 designs](/find-your-trn/iteration-3), the user's response was captured with a free-text field. In subsequent research, [we came across users who were expecting](/find-your-trn/iteration-3/#other-findings) their responses to be auto-completed.

## Potential sources for provider names

We could potentially have drawn the ITT provider names out of the [Teacher Training Courses API](https://api.publish-teacher-training-courses.service.gov.uk/#about). However, that API only contains existing ITT providers, and wouldn't help users who underwent training a while back and whose training providers no longer exist.

We decided to try using the free-text ITT provider names that are stored against the teachers' records within the Database of Qualified Teachers (DQT). There isn't currently an API that exposes this information but it could plausibly be unlocked to populate the auto-complete functionality.

## Are we using the appropriate provider name?

[Some ITT providers, namely school direct providers, can have multiple names](https://bat-design-history.netlify.app/publish-teacher-training-courses/courses-as-an-accredited-body/#marketing-name-vs-school-name):

* an alliance name – a marketing name that represents a group of schools
* the name of the lead school in the alliance

DQT stores the name of the lead school, and this may not be the name that teachers will remember from their training and try to enter. For instance, the teaching school alliance might be called "West London Teaching School Alliance", but the lead school is "Sacred Heart High School" (the latter is the name recorded in DQT).

We should monitor for auto-complete failure on this page in future user research, and when the service is live. DQT also stores the UK provider reference number (UKPRN), so it may be possible to add the provider marketing name by joining to another source on the UKPRN, if needed.

## Disambiguating school providers

The data contains similarly-named lead school providers (e.g. St Mary's, St Joseph's). In future iterations, we may want to include the school's postcode to help tell the different schools apart, [similarly to how it's done in other teacher services](https://bat-design-history.netlify.app/register-trainee-teachers/searching-for-a-school-part-2/).

## Data cleansing needed on the DQT extract

We post-processed the DQT extract of provider names, before embedding it into our prototype:

1. Some names contained extra DRB and EBR strings (e.g. `EBR University of Reading` and `Tipton Green Junior School DRB - 333/2082`). We assumed these acronyms stand for Designated Recommending Bodies and Employment-Based Routes. These strings were removed.
2. Some names contained extra numbers/codes (e.g. `University Of Plymouth - 8715` and `Wishmore Cross School DRB - 936/7024`). These extra characters were stripped out.
3. The list was de-duplicated while ignoring case (to deal with similar entries like `Institute of Education`/`Institute Of Education`).
