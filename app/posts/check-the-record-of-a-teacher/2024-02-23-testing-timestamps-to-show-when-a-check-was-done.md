---
title: Testing timestamps to show when a check was done
date: 2024-02-23
screenshots:
  items:
    - text: timestamp on a search results page for no results
      src: no-records-found.png
    - text: timestamp on a record page
      src: record-page.png
---

The second of our [3 iterations to test in private beta based on user feedback](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/testing-summary-tags-to-show-the-status-of-a-teacher) is adding a timestamp.

In Employer Access, users had a print button which they could use to print the page. We didn't include this in Check the record of a teacher because:

- users can print from the browser
- we wanted to better understand requirements from governing bodies about evidence for doing checks
- we wanted to see if this problem could be better solved at a system level, for example by seeing if we could share data for an end to end journey between teaching vacancies, teacher checks, and inspecting bodies
- we don't want to encourage use of ink and paper from our digital service unless we know users need it

We wanted to find out more in our research how users would do this without a print button and what their needs are for keeping records.  

## User research

In our user research for private beta round 1 with teacher supply agencies, users told us about keeping copies as evidence of searches which they could show when audited. Some kept additional paper copies, but all used a variety of digital document management. The evidence included:

- screenshot of the teacher reference number (TRN)
- screenshot of the status box in Employer Access
- screenshot showing that a name was not on a list of people with restrictions

One mentioned the lack of a print button. When asked what they would do, they tried using the `File > Print` browser commmand and were satisfied with the outcome.

One of the benefits of using the print command was that users could save to a PDF file and it could generate the date and time the search was done.

> "schools just want to know the check is done, when it was done and the recruitment policy"

When asked if anything was missing, one said:

> "...there isn't a 'print' link to be able to print or download the checks. That's a requirement for an employer to hold time-stamped proof"

This is consistent with feedback from the alpha user research.

## Design

We've added text that says the date and time a search was made on the record page. This is so that users who screenshot will be able to record and show when they did the check. It also helps the service to be clear that the data presented is correct at that time, as it could change.

We've also done this on the search results page when there are no results. This is because some people use this to show that someone has not been a teacher and previously restricted. For example, when applying for a new teacher training course.

If there are no results it displays: "Records searched at"

On the record page it displays: "Record checked at"

The date and time are formatted to the [GOV.UK style guide for dates and times](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style).

It does not display on search result pages where there are results, becuase this is not used for evidence.

To do this we've used a medium size class [caption](https://design-system.service.gov.uk/styles/headings/#headings-with-captions). This is so that they appear in [govuk-border-colour](https://design-system.service.gov.uk/styles/colour) which helps to seperate it from the rest of the body content. As this is secondary to the main user need of the page we did not want the timestamp to distract from the more important information.

We've placed the caption in `{% block beforeContent %}` which means it sits closer to the breadcrumbs at the top of the page than the heading. This means we can use the same position on the search results or record pages so it does not conflict with the `h1` which it may not directly relate to. 

We also considered placing it within the breadcrumbs, however this would be non standard nesting of 2 components and could be confusing for users as it would appear to be part of the page title. This is important because the user need for the timestamp is in screenshots after the search has been done, and not to understand while viewing the page.

## Testing

We've included this in our prototype and are testing it with users. We want to make sure:

- it is useful and neccessary for evidence
- users do screenshot this instead of using a print function
- it does not distract from the rest of the page

We are observing if users notice or talk about it in usability testing. We may prompt them with questions about how they would save the result of the check for their records and what information needs to be included.

We are also going to speak with governing bodies to understand if our design meets their requirements for evidence.