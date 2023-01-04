---
title: New regulations part 1 – English language
date: 2023-01-04
screenshots:
items:
- text: "English proficiency method v1"
- src: english-proficiency-method-v1.png
- text: "English proficiency citizenship"
- src: english-proficiency-citizenship.png
- text: "English proficiency qualifications"
- src: english-proficiency-qualifications.png
- text: "Proof of English proficiency"
- src: english-proficiency-proof.png
- text: "English proficiency provider"
- src: english-proficiency-provider.png
- text: "English proficiency reference"
- src: english-proficiency-provider-reference.png
- text: "English proficiency casework qualifications"
- src: english-proficiency-casework-qualification.png
---

From 1 February 2023, the ‘Apply for qualified teacher status’ service needs to work with new regulations, as the service is opened up to applicants from all over the world.


In this summary, we’ll look at the first brand new requirement – providing evidence of an applicant’s English language proficiency.

## Understanding the requirements
The new regulations offer 4 routes for an applicant to satisfy the English language requirements of QTS. Which of those routes is most appropriate depends on their nationality and where they studied.

### Route 1 – Exemption by birth or citizenship

The applicant was born in (or has since gained citizenship of) England, Scotland, Wales, Northern Ireland or one of the countries on the [exemption list](https://www.gov.uk/english-language/exemptions).

### Route 2 – Exemption by country of study

The applicant studied either their teaching qualification or their university degree in England, Scotland, Wales, Northern Ireland or one of the countries on the exemption list.

### Route 3 ­– uploading a ‘Medium of instruction’ (MOI)

The applicant was taught exclusively in English in a non-exempt country. They must upload a ‘Medium of instruction’ (MOI), which is an official document from the institution of study.

### Route 4 – holding or undertaking a Secure English Language Test (SELT) from an approved provider

The SELT must be from 1 of the 5 [approved providers](https://www.gov.uk/guidance/prove-your-english-language-abilities-with-a-secure-english-language-test-selt), taken within the last 2 years, and be at B2 level (having satisfied the thresholds for that provider in all 4 disciplines of reading, writing, listening and speaking).






## Explaining the options to applicants

### Version 1 – presenting all the routes together

Initially, we planned to show applicants all 4 routes together. The eligibility checker asked a simple yes/no question as to whether they could satisfy any of the options, and gave more detailed information about the routes in the ‘You’re eligible’ page.

The application form then used an interaction with 4 radio buttons, which allowed the applicant to choose their preferred route. In the case of the 2 exemption routes, they could tell us they’d already uploaded the required document, while the remaining routes would take them to upload interactions based on existing patterns.

However, once UR began, we discovered some issues. Applicants:

* did not always complete the form from top to bottom, so ‘already’ did not always make sense

* seemed to be overwhelmed with the 4 options all at once

* assumed their country was on the exemption list, missed the dropdown details component and pursued the wrong route

* Did not understand the term ‘Medium of instruction’



![English proficiency method v1](english-proficiency-method-v1.png)




### Version 2 – filtering using a hierarchy of routes

To address the issues we saw in testing, we decided to filter applicants through to the most appropriate route by asking them separate questions about their nationality and where they studied.

![English proficiency citizenship](english-proficiency-citizenship.png)
<br><br>
![English proficiency qualifications](english-proficiency-qualifications.png)





Crucially, we avoided asking them to decipher for themselves whether or not they were ‘exempt’.


Instead, we directed them to the appropriate content based on their responses to the questions. It now means those who are exempt are directed back to the task list with the language question marked as ‘Complete’, while those who need to provide something more, need only choose from 2 options instead of 4.

![Proof of English proficiency](english-proficiency-proof.png)




UR showed this version was much easier to understand, as was a new explanation of ‘Medium of instruction’ (MOI).


Some applicants mistakenly thought that not appearing on the exemption list meant they could not progress further. To solve that, we put in a simple fix changing the radio buttons from just ‘Yes’ and ‘No’ to ‘Yes’ and ‘No, I’ll show my English language ability using another method’.

## Making sense of SELT

The list of approved English language test providers is short, but the 5 organisations differ on how applicants can show evidence of their results. The original concept was to ask the applicant to provide a reference number and upload their certificate, but it became clear that only 1 of the 5 offers a paper certificate, while another 2 provide PDF versions and the remaining 2 use a dashboard model.

They do, however, all give the applicant some form of reference number (albeit under a variety of names), so we took the decision to use a similar model to the reference number interaction used for ‘Proof that you’re recognised as a teacher’.


We ask the applicant to select which of the 5 providers they studied with, before serving them with content written around that provider’s requirements.

![English proficiency provider](english-proficiency-provider.png)




This content includes the reference number character count and the pass threshold for the 4 disciplines of reading, writing, listening and speaking. We can then re-use this information in case management, so the assessors are clear on what they're looking for.


As asking candidates to key in a long number may lend itself to errors, we’ve also built in a further information request path for instances where assessors cannot find the applicant using the number they’ve provided.

![English proficiency reference](english-proficiency-provider-reference.png)



## Case management

At first glance, the assessor-side journey for English language is relatively simple. The two exemption routes mean checking that the passport or qualifications support the applicant’s exemption, while the other 2 routes mean checking the MOI document or looking up a reference number.

The patterns for all those interactions exist within the current service, but what made it more complicated was that for the 2 exemption routes, assessors would be reviewing the evidence using the same documents they’d use for other parts of the assessment.


In the case of exemption by birth/citizenship, they’d be reviewing the passport (also used in ‘Check personal information’) and for exemption by country of study, they’d be looking at all the qualification documents that also constitute the evidence in ‘Check qualifications’.

When it comes to requesting further information, things could get complicated. For example, if the assessor finds a university degree transcript that’s illegible in ‘Check qualifications’ they can request further information by selecting a predefined reason. If they then need the same documents as proof of exemption by country of study, we run the risk of either selecting the same further information reason twice, or having a set of additional, differently worded reasons.

In either case, the applicant could receive a further information request that at first glance appears to require 2 actions, but in fact needs only one. It’s also an unwieldy system for the assessors to record the same action twice.

We know that assessors can work through an application in any order, so the solution needs to work no matter which section they start with. For that reason, we’ve kept the checklist items and further information/decline reasons for ‘Check personal information’ and ‘Check qualifications’ in their respective sections.


When the assessor comes to ‘Check English language proficiency’ if the applicant has used either the MOI or SELT route, the ‘Check English language’ section surfaces its own further information reasons pertaining to those routes.



![English proficiency casework qualifications](english-proficiency-casework-qualification.png)

If the applicant chooses an exemption route, the ‘Check English language’ section will instead surface a banner that tells the assessor which route the applicant has chosen, directing them to the section they need to assess.
