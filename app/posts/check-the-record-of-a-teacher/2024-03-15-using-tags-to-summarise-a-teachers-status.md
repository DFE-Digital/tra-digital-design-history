---
title: Using tags to summarise a teacher’s status
date: 2024-03-15
screenshots:
  items:
    - text: Has QTS, passed induction and has no restrictions
      src: qts-induction-no-restrictions.png
    - text: Possible match on the children's barred list
      src: possible-cbl.png
    - text: Failed induction
      src: failed-induction.png
    - text: Prohibited from teaching due to serious misconduct
      src: restricted-misconduct.png
    - text: Found guilty of misconduct but not restricted from teaching
      src: guilty-misconduct-not-restricted.png
---

At the start of the private beta phase we invited teacher supply agencies to use the new service to check a teacher’s record.

Since then we’ve invited further groups to use the service. We’ve collected insights from:

- alpha user research
- private beta user research
- support requests
- feedback given within the service
- analytics

From this we’ve identified 3 themes which:

- have come up more than once in feedback
- fit with what we’ve learned about our users
- can be explored through small iterations to the design of the service

These themes are:

- providing a summary of a teacher’s status
- showing when a search was made
- giving more useful information when there are no search results

## How a teacher’s status is shown in Employer Access

The new service will replace one called Employer Access. In the older service, a teacher’s record includes a status box which says:

- if the teacher has any alerts, for example if they failed their induction or have been prohibited from teaching for serious misconduct
- the date when they got qualified teacher status (QTS) or early years teacher status (EYTS)
- their induction status, for example if they’re currently in their induction period

The status box is:

- red if there’s an alert
- yellow if something is missing, for example if they have not passed induction yet
- green if there are no problems with the record

## Our design for the initial private beta release

We did not include a status box in the initial release because:

- it would repeat information which is in the record and we were not sure that this was useful
- we did not know enough about how users interpret status indicators in different situations

A red or yellow status box in Employer Access does not necessarily mean that a teacher cannot be employed. For example:

- an academy could choose to employ a teacher who does not have QTS
- a college could choose to employ a teacher who has not passed induction

We knew that the most important thing to indicate is that a teacher has an alert. But even for alerts the meaning can vary.

For example, an alert can say that the teacher was found guilty of serious misconduct but has not been prohibited from teaching.

In addition, older restrictions imposed by the General Teaching Council of England do not prohibit people from teaching in academies or independent schools.

### Removing tags before launching the service

Instead of a status box, our early designs had tags to say whether or not someone had a teaching restriction. By ‘restriction’ we meant anything which would cause an alert to appear on the record.

Before private beta started we [removed the tags from the search results page](/removing-the-tag-showing-that-someone-has-teaching-restrictions/) because the purpose of that page is to help users identify and click through to the correct record. It does not matter at that point whether the teacher has a restriction.

We then [removed the tags from the record page](/removing-the-tag-showing-that-someone-has-no-teaching-restrictions) because they were repeating information and could also be misleading.

For example we were not sure whether to say that someone has a restriction if they have an alert because they:

- have been found guilty of misconduct but not prohibited from teaching
- have a possible match to a record on the children’s barred list - we tell users to contact the Disclosure and Barring Service (DBS) to check whether the teacher is actually on the list

There are also situations where no alert is shown but the teacher would not be able to work in some roles. For example if they:

- have not completed induction - an alert appears if they fail induction, but they also may be within their induction period or may not have started yet
- are still training and therefore do not have QTS yet

We decided to leave out the tags and gather more information from users after the initial release.

Users would still see the details of any restriction in an alert shown at the top of the record.

## Users’ feedback about the lack of a status summary

After the initial release to teacher supply agencies, several users told us that they were unsure if the new service included alerts for people prohibited from teaching.

> “I don't know if there are no alerts or if you just don't show the alerts? Is it actually going to show me an alert?”

This is because it’s very rare for users to see a record with an alert. Most people who are prohibited from teaching do not apply for teaching jobs.

Users were used to seeing an indication in Employer Access that a teacher had no alerts. They found this reassuring and it helped them feel confident when making decisions.

> “We have used the new service but there is no reference to any sanctions/alerts section on the result page, is this correct? The previous checks included an alerts section which evidenced that this check had been carried out and that there were none or details were provided.”

In the new service, we did not explicitly say that there was no alert. We just did not show an alert.

Some users also told us they wanted to see to something on screen which they could print or include in a screenshot for their records. They said that it would be useful to have an indication of restrictions and other status information in one place.

> “I want a status like the old service, with alerts equals none, QTS and induction status. This is what we screenshot.”

We know that Ofsted do not ask for evidence that a record was checked but many users have said that they believe they need such evidence.

We decided to revisit the idea of including a status summary. We wanted to find out whether we could give a summary in a way which is helpful and also accurate in different situations.

## Our design for summary tags

We decided to test using [tags](https://design-system.service.gov.uk/components/tag/) to give a summary covering three categories:

- restrictions
- teaching status
- induction

Each teacher’s record has one tag from each of these categories.

Our aim is for each tag to be understandable based only on the words used. However we’ve also used the colour of tags to give an indication of the teacher’s status.

A tag can be:

- green for a status which does not prevent a teacher from being employed
- red for a teaching restriction
- blue for anything that may need more attention depending on the role which the teacher has applied for

The tags appear under the heading “summary” in the [one-third column](https://design-system.service.gov.uk/styles/layout/) to the right of the main content. This helps distinguish the tags from the rest of the text on the page.

We put the tags in a [borderless summary list](https://design-system.service.gov.uk/components/summary-list/) with a single column. Each tag should make sense on its own and relate to a more detailed piece of information within the record. We therefore did not give each category a heading label.

### Restrictions tags

The tags for restrictions are:

- no restrictions (green)
- restricted (red)
- check with DBS (blue)

This is the only place where we use a red tag. It’s important that a user knows that there’s a restriction so that they can check the details. These appear in an alert, which uses red inset text at the top of the record.

The “check with DBS” tag appears if there’s a possible match with the children’s barred list. We do not use a red tag because we are not certain that it’s a match. The alert at the top of the record tells the user to contact the DBS to check.

If the teacher has been found guilty of misconduct but not restricted from teaching then we show a green “no restrictions” tag. Details appear in the alert at the top of the record, with a link to the misconduct hearing findings on GOV.UK.

### Teaching status tags

The tags for teaching status are:

- QTS (green)
- EYTS (green)
- no QTS (blue) - this appears if the teacher does not have QTS or EYTS

If the teacher has both QTS and EYTS then we only show the QTS tag. This is because QTS can be used to teach in an early years setting.

Additional teaching statuses are shown within the record including:

- trainee - for testing we decided to show “no QTS” for this
- partial QTS - for testing we decided to show “QTS” for this

### Induction status tags

The tags for induction status are:

- passed induction (green)
- induction exempt (green) - there are many reasons why a teacher may be exempt from induction
- no induction (blue)

The teacher could have no induction because:

- they have not started induction yet or are in their induction period
- they’ve failed induction - they’ll be able to work in some places, such as colleges, so we use a blue tag

If someone fails induction then they are also given a restriction by the TRA. This means that they will have both:

- a blue “no induction” tag
- a red “restricted” tag

This is not consistent with the other categories, where each situation has a single tag. We decided that this was fine for testing but that we may change it later.

## Moving the teacher’s personal details

Previously we did not use the one-third column in a teacher’s record. Since we’re now using it we decided to also put personal details in it.

We did this because:

- personal details are a different type of information to the qualifications which make up most of the record
- users will already have seen the personal details on the previous search results page, so they do not need to be highlighted at the top of the record

Putting the personal details in the right hand column is also consistent with [Access your teaching qualifications](https://tra-digital-design-history.herokuapp.com/qualifications-service/qualification-service/) which teachers use to check their records.

However, to make the design fit better with the rest of the record in this service we’ve used:

- a standard 1 pixel [section break](https://design-system.service.gov.uk/styles/section-break/) dividing line in [govuk border colour](https://design-system.service.gov.uk/styles/colour/)
- `<h3>` and `<h4>` headings

## Testing the new design

We didn’t know if the combination of tags in the 3 categories would make sense as an overall status in different situations.

We wanted to see if the tags would help users to:

- understand a teacher’s record
- get the evidence they need for their own records
- make a decision about whether to employ a teacher

We also wanted to make sure that the tags did not confuse or distract users.

We decided to test the design by creating a series of scenarios in the prototype. Each scenario asked the user to make a hiring decision about a teacher with a different set of status tags.
