---
title: Testing summary tags to show the status of a teacher
date: 2024-02-21
screenshots:
  items:
    - text: Gained QTS, passed induction, no restrictions
      src: qts-induction-no-restrictions.png
    - text: Has a possibile match on the children's barred list
      src: possible-cbl.png
    - text: Has failed induction and is restricted because of it
      src: failed-induction.png
    - text: Restricted due to being found guilty of misconduct
      src: restricted-misconduct.png
    - text: Found guilty of misconduct but not restricted from teaching
      src: guilty-misconduct-not-restricted.png
---

The government design principles include to [iterate, then iterate again](https://www.gov.uk/guidance/government-design-principles#iterate-then-iterate-again) and the service standards to [iterate and improve frequently](https://www.gov.uk/service-manual/service-standard/point-8-iterate-and-improve-frequently).

After launching our first round of private beta to teacher supply agencies, we were able to get more insight from users in their natural settings and continued usability testing on a live version of the service.

We collected feedback, as well as previous insights from:

- alpha user research
- private beta user research
- the helpdesk
- analytics

We also considered previous design decisions that needed validating, such as if leaving something out could cause a problem. For example, we don't show information that's missing or not on someone's record such as national professional development courses for teachers and leaders.

We identified 3 themes which came up more than once, fitted with our developing understanding of our users, and could be explored in manageable iterations to our design. The first of these was status or summary information.

## The earlier design

In Employer Access, users could see a status box on the record which said:
- if the teacher had any alerts
- what date they got QTS
- the status of their induction

The box would be red if there was an alert, orange if something such as an induction was missing, or green if everything was OK. They would also check a list of all teachers with restrictions, and see if their applicant was, or was not, on the list.

We did not include a status box in our design because the information is in the record and we didn’t understand enough about how users interpret these indicators in different situations. 

Our initial design had tags to say if someone was restricted or not. We removed them from the search results page because the focus on this page is to identify a correct record before viewing it. We removed them from the record page because they were repeating information and could be misleading. For example: 

- if someone had been found guilty of misconduct but not been prohibited from teaching we still said they were restricted
- if someone had not yet completed induction we said they were not restricted, but they still may not be allowed to teach in some settings
- if someone had trainee QTS, or EYTS, we said they were not restricted, but they still may not be allowed to teach in some secondary settings

The different indicators needed to be considered as a whole in relation to the setting the teacher wants to work in. We wrote about the decisions in earlier posts:

- [removing the tag showing that someone has teaching restrictions](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/removing-the-tag-showing-that-someone-has-teaching-restrictions/)
- [removing the tag showing that someone has no teaching restrictions](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/removing-the-tag-showing-that-someone-has-no-teaching-restrictions/)

We thought that the status box or restrictions tags could have value for users but needed more understanding before deciding if or how to include them.

## Feedback from users

A lot of users told us they were unsure if the new service included alerts or restrictions at all, as they would only see something if there was a restriction in place. They wanted the absence of something to be made clear, so they know it’s not an error and can be more confident when making decisions. Users told us they need to see something that they can print or screenshot and keep in their records to prove the information was correct when they checked.

> “I don't know if no alerts of just don't show the alerts? Is it actually going to show me an alert?”

> “We have used the new service but there is no reference to any sanctions/alerts sectin on the result page, is this correct? The previous checks included an alerts section which evidenced that this check had been carried out and that there were none or details provided?”

Some users also talked about using the service as a “QTS check”, confirming induction, and using the old status box to screenshot for evidence.

> “You used to get their status which is good” 

> “I want a status like the old service, with alerts = none, QTS & induction status. This is what we screenshot”

We know that our users are busy and work in risk adverse settings where clarity is important. They need to clearly know whether to proceed with recruitment and be able to evidence their due diligence when they get inspected. While the records in our MVP contained the necessary information, not all users felt reassured or confident by using it.

We decided to revisit summary information and explore if we could do this in a way that was helpful but also accurate in different situations. We wanted to then test if this works.

## Design for summary tags

For our colour system, green is suitable to employ, red is restricted from teaching, and blue is for anything else that may need more attention or might mean different things depending on the role being applied for. We wanted to keep it simple and make sure the content makes sense without the colour.

To give structure, we put the tags in a [borderless summary list](https://design-system.service.gov.uk/components/summary-list/) with a single column. They should make sense on their own and relate to a more detailed piece of information within the record, so we did not give them individual heading labels.

We gave the group of tags the heading of “summary” and placed this in a [one-third column](https://design-system.service.gov.uk/styles/layout/) to the right of the main content. This is using the [gestalt proximity law](https://lawsofux.com/law-of-proximity/) to group related items together and distinguish from the rest of the text on the page.

This is also consistent with [Access your teaching qualifications](https://tra-digital-design-history.herokuapp.com/qualifications-service/qualification-service/) which is the teacher facing aspect of this data, although we have used the standard section break dividing lines in 1px [govuk border colour](https://design-system.service.gov.uk/styles/colour/), and headings with `<h3>` and `<h4>` which is more consistent with the rest of our page.

## Restrictions

For restrictions we use a green [tag](https://design-system.service.gov.uk/components/tag/) for “no restrictions”.

We use a red tag for “restricted”. This is the only place we use a red tag, for emphasis.

We introduced a blue tag for “check with DBS”. This is because we include possible matches with the children’s bared list, but tell the user to contact DBS to find out more as we can’t say for certain.

If someone has a restriction then we include inset text at the top of the record to give more detail.

One of the restriction types is “found guilty of misconduct but not restricted from teaching” and there is a link to published outcomes of hearings. In this case we show a green “no restrictions” tag, but also show the inset text with this message.

## Teaching status

We use a green tag if the teacher has qualified teacher status (QTS) or early years teacher status (EYTS). If they have both, we only show QTS because it can be used in both settings.

To keep it simple for testing, we show anything else with a blue “no QTS” tag. There are more statuses, such as partial QTS or trainee which could be added as a refinement. This information is still in the record itself.

## Induction

We use green tags for “passed induction” or “induction exempt”. Anything else has a blue tag for “no induction”.

If someone has failed induction, they are also given a restriction. They will have blue “no induction” and red “restricted” tags. If someone’s induction is in progress they do not have a restriction.

## Testing

We want to test these design with users in different scenarios. This is because we were hesitant about including a similar idea early on as we didn’t know if the combination of these 3 indicators would make sense as an overall status in different situations. We want to see if this helps users digest the information, record evidence or make a decision and if they make sense reduced to concise tags. We want to make sure they don’t add confusion or additional interaction cost to using the service if users have to think about what they mean.

To do this we’ve created 6 scenarios which give a combination of different variations. We’ve put this into our prototype and will test with users in our next round of research. If the idea is validated we’ll review doing this in production. If we find it is more complicated, or doesn’t help, we can use the insight for our backlog for future work.