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
---

{% from "vimeo/macro.njk" import appVimeo with context %}

Panellists can [use a calendar widget in the panellist portal](/teacher-misconduct/panellist-portal/#unavailability-for-tra-hearings-with-unavailable-days) to record their unavailability. This calendar is not accessible and is difficult to use, even [after our fixes](/teacher-misconduct/recording-unavailability-fixes/).

## A new service

We are experimenting with a new service for displaying and editing panellist unavailability, in the style of GOV.UK, and using the GOV.UK design system.

The expectation is that this service:

- will be linked to from the current portal
- will not require users to sign in again (this is dependent on a tech spike to prove that it is possible)
- will make it easier for panellists to accurately and easily record their unavailability
- will record data into the existing CRM using an API

## Video walkthrough

{{ appVimeo('715529995') }}

## We need to research with users

This design has not been tested with users yet, but he have some hypotheses.

From analysis of existing usage we expect users will need to:

- record 1 or 2 days at a time, on an adhoc basis
- block out whole weeks or months at a time (for example holidays)
- tell us they are unavailable on certain days of the week (for example childcare or working patterns)

Users might want to print their calendars, or export them to other digital calendars.

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
