---
  title: Stopping matching on email address (for now)
  date: 2021-12-14
---

Records in the Database of Qualified Teachers (DQT) can have email addresses associated with them. For most records, this email address is recorded onto DQT by the ITT training provider, either via HESA or DTTP/Register, at the point that the TRN is issued.

If a TRN holder uses the 'Find my TRN' service shortly after the creation of the TRN, it's plausible that their DQT email address is still an email address they regularly use.

However, this becomes less likely over time:

* the TRN holder may change their email address without informing DfE (and they currently don’t have a good reason to keep their DQT email address up-to-date)
* the TRN holder might lose access to the email address (e.g. it could be their uni address that they leave unused)
* the DQT email address might have been purged by DfE, in compliance with GDPR

## Estimating how common this scenario is

To gauge how often TRN holders still used the email address on their DQT record, we:

1. sampled several hundred applications made through the [Teaching Vacancies service](https://teaching-vacancies.service.gov.uk/) (TVS).
2. took the email addresses and TRNs from the applications.
3. matched the applications to DQT records using the TRN.
4. counted how often the email address on the job application matched one of the email addresses on the DQT record.

Around 20% of TVS applications had an exact address email match against the DQT record.

This seemed like a cohort that was sizeable enough to tackle at the MVP stage of the service.

## Iteration 1

In [iteration 1](/find-your-trn/initial-design), we designed an explicit journey whenever a TRN holder used an email address that matched their DQT email address:

* the user enters their email address
* they verify access to the address by following a magic link
* if the provided email address matches an email address on exactly one DQT record, the user is shown their TRN without being asked for any personal data

## Iteration 2

 In [iteration 2](/find-your-trn/iteration-2), [we removed magic links](/find-your-trn/iteration-2/#emailing-the-result-instead-of-magic-links), so the above journey became:

* the user enters their email address
* the user confirms that they have entered their email address correctly
* if the provided email address matches an email address on exactly one DQT record, the user is emailed their TRN without being asked for any personal data

## Learnings from usability testing

We tested the iteration 2 journey with 4 current and ex-teachers, and all participants expressed some degree of discomfort with this journey. The system felt insecure, with validation against the email address seeming too light.

Participants also mentioned that their emails change over time so it seemed odd using this as a means of identifying them. They would have been more comfortable being asked for more immutable things like their National Insurance number or date of birth.

> It seemed like all I had to do was put an email in and they would tell me what my TRN is. I don’t even think I’ve told them my name yet at this point.
> – Participant 4

## Scaling back what the email address is used for

On the back of the research feedback, we:

* excluded the email address from the matching logic
* moved the email address prompt to the end of the flow
* clarified in the guidance on the email address page that the email address is only used to deliver the TRN.

## Considerations for future designs

We would look to reintroduce the email address for matching at a later date.

The [existing designs](/find-your-trn/iteration-2/#your-email-address) didn’t make clear that the email address would be used for two purposes: delivery of the TRN, and matching. Future designs should try to make this explicit, either through interaction (e.g. by having separate questions/pages for the delivery email and matching email) or content (e.g. by explicitly stating what the entered email address will be used for).

We might also explore using the email address as another “3 matches from X” identifier, rather than a special “one and done” identifier.
