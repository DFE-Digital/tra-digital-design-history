---
  title: "Fixes when recording unavailability"
  date: 2022-05-24
  screenshots:
    items:
      - text: "Calendar with save changes button"
        src: 01-new-design.png
      - text: "Warning message when removing unavailability"
        src: 02-existing-warning-message.png
        caption: We are removing this
---

Panellists can [use a calendar widget in the panellist portal](/teacher-misconduct/panellist-portal/#unavailability-for-tra-hearings-with-unavailable-days) to record their unavailability. The calendar uses the [Kendo UI Scheduler widget](https://docs.telerik.com/kendo-ui/api/javascript/ui/scheduler).

We know this calendar is not accessible and are working on a [long term alternative](/teacher-misconduct/tell-us-when-youre-unavailable/), starting first with research to determine the needs of our users.

The calendar also has issues that affect its own performance and usability. We can fix those first.

## The problem

Each time a date is clicked, or availability is changed, a request is sent to the server. When selecting a range of dates, or just clicking around, that's a lot of requests. Sometimes those requests can fail, especially if the server is acting as a bottleneck. This quickly degrades the user experience, and with the browser and server in different states, the unavailability a user intended to record may not be saved correctly by us.

When removing unavailability, users also have to confirm their deletion for each date. This makes selecting long date ranges easy, but removing them difficult.

## The fix

Instead of sending each change to the server, we will batch them up and send them when a user confirms their changes.

We will:

- add a save changes button to send the batch of changes as a single request
- include a warning that changes must be saved
- include [a javascript warning](https://developer.mozilla.org/en-US/docs/web/api/window/beforeunload_event) if they try to navigate away from the page without saving their changes (Chrome and Firefox have default messages they show for this dialogue – ‘Do you want to leave this site? Changes you made may not be saved.’)
- disable the deletion warning (the deletion is no longer immediate)
