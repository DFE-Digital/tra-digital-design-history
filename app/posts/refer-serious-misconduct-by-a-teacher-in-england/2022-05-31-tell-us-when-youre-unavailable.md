---
  title: Improving the recording of unavailability
  date: 2022-05-31
  screenshots:
    items:
      - text: "Home page with calendar"
        src: 01-home-page-with-calendar.png
      - text: "Month view"
        src: 02-month-view.png
      - text: "Month view with unavailability"
        src: 03-month-view-with-unavailability.png
      - text: "Changes saved"
        src: 04-changes-saved.png
  related:
    sections:
      - title: Related content
        items:
          - text: Unavailability prototype
            href: https://teacher-misconduct.herokuapp.com/
          - text: User research findings
            href: https://airtable.com/appYuEB9JEC4x2zh6/tbl64BgEPFCtBw5G1/viwCCH1okgzFZZ9e7?blocks=biprlopaojCsFJFFo
---

{% from "vimeo/macro.njk" import appVimeo with context %}

Panellists can [use a calendar widget in the panellist portal](/refer-serious-misconduct-by-a-teacher-in-england/panellist-portal/#unavailability-for-tra-hearings-with-unavailable-days) to record their unavailability. This calendar is not accessible and is difficult to use, even [after our fixes](/refer-serious-misconduct-by-a-teacher-in-england/recording-unavailability-fixes/).

## A new service

We are experimenting with a new service for displaying and editing panellist unavailability, in the style of GOV.UK, and using the GOV.UK design system.

The expectation is that this service:

- will be linked to from the current portal
- will not require users to sign in again (this is dependent on a tech spike to prove that it is possible)
- will make it easier for panellists to accurately and easily record their unavailability
- will record data into the existing CRM using an API

## Video walkthrough

{{ appVimeo('715529995') }}

## User research

We tested this design with 5 panellist users:

- 2 lay panellists
- 3 teachers

### Calendar usability

It tested very well, was easy to use and preferred to the portal.

> "This is much, much easier than the current portal"

Users could easily:

- record 1 or 2 days at a time, on an adhoc basis
- block out whole weeks or months at a time (for example holidays)
- tell us they are unavailable on certain days of the week (for example childcare or working patterns)

Selecting days of the week, all week, or all month was seen as useful, easy and quick.

We found that:

- the date range of the current year plus one year was sufficient, users tended to plan up to about 6 months in advance
- selection of one or multiple days was intuitive and easy for all users, so too was removing dates
- users understand without a key that dates highlighted in orange (or ‘salmon’ as one user described it) meant they were unavailable, a key would be needed if we add more things to the calendar
- clicking "Save" is intuitive behaviour after changing dates (users did not try to leave the page without saving)
- selecting unavailability is preferred to availability
- weekend selection is necessary if panelists need to travel on a weekend
- when we asked about printing calendars, they would not print because paper calendars breach data safety regulations
- there's some interest in using the calendar on their mobile, but it remains unclear if they could or would sign in using Azure on their phones
- when entering dates that span two months, being able to show next or previous months could be useful

There's a nuance around showing dates at the start and end of a month, for example when looking at July, we might show June 30 at the beginning and 1 August at the end, depending on the days of the week. This is to make it easier to select a whole week. But the side effect is that they are also selected when using the "every Monday" or "all month" features – which might be unintended. We could limit those features to only select days within a month.

### Additions to the calendar

When prompted, panellists noted they would like to see hearings in a calendar, and they'd like to be able to export them to their personal calendar apps (Google, Outlook, Apple).

The calendar should differentiate between in-person and virtual hearings.

### Other information they need

Panelists are expected to sit for roughly 12-20 days a year. It would be useful for them to keep track of their participation. There may be other intrinsic rewards to seeing how much time they have given.

Users want to see summary data of their participation to date. helps panelists see if they meeting their attendance-target.

### Other findings

As expected, scheduling needs are complex and vary greatly between panellists.

Unavailability is sometimes tentative and users will take different approaches to recording this – for example proactively blocking out, or alternatively waiting until something is confirmed. We will not introduce a ‘I might be unavailable’ state, as it would only complicate the service.

## Accessibility

There are accessibility improvements we need to make to this design.

- It is not obvious that an orange box means the day is unavailable, we probably need a key and/or descriptive text
- Sighted users can get an overview of the year by scanning the months, a text summary of unavailable days might work better for anyone who cannot see this. We also expect there to be existing accessible calendar patterns we can draw from
- On the month view, the text 'All week' is repeated – these need date ranges to make them unique, both for screen readers and speech recognition users (for example Week 1 or June 20 to June 24)
- Changes to the month view using the helper links must be appropriately announced for assistive tech, the challenge will be to avoid being too verbose
- Table markup needs appropriate captions and headings

The prototype already incorporates some accessibility features:

- The calendar and month views can be used with only a keyboard
- The views render appropriately without any styles
- Labels for each checkbox are unique, so that speech recognition users can trigger them first time (for example 30 May and 30 June being shown on the same month, if the label was only ‘30’ this wouldn't be possible)

## Earlier iterations of the calendar

{{ appVimeo('715544205') }}
