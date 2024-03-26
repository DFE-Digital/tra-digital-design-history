---
title: Showing when a search was made
date: 2024-03-26
screenshots:
  items:
    - text: Time stamp on a search results page with no results
      src: no-records-found.png
    - text: Time stamp on a record page
      src: record-page.png
---

After the initial private beta release we chose 3 themes to explore based on user feedback and analytics. The themes are:

- [providing a summary of a teacher’s status](/check-the-record-of-a-teacher/using-tags-to-summarise-a-teachers-status)
- showing when a search was made
- giving more useful information when there are no search results

We decided to explore showing when a search was made because we got feedback from users about how they keep evidence.

## How users keep evidence from Employer Access

When we launched the private beta we knew that users of Employer Access often want to keep evidence of searches they’ve made. They can do this by:

- taking a screenshot
- using the print function to save a PDF
- printing

Taking a screenshot or saving a PDF means that the date and time is in the metadata for the file. It can also be included in the file name.

Many browsers print a date and time at the top of a page by default.

## Our design for the initial private beta release

Employer Access has a print button which opens a browser’s print dialogue box but has no other effect.

We did not include a print button in the new service because:

- users can still take a screenshot or print from their browser using the file menu or a keyboard shortcut
- we were not sure that Ofsted and other organisations require printed evidence of a search
- we do not want to encourage the use of ink and paper unless we know users need to print
- printing records may be more likely to lead to personal information being stored insecurely

## Users’ feedback about keeping evidence and the lack of a print button

Since we launched the service in public beta, several users have contacted us to ask whether we plan to add a print button. We decided to find out more about their needs.

In research, users from teaching supply agencies told us that they need to show evidence to:

- the schools where they’re providing teachers
- organisations which audit their work, such as the Recruitment and Employment Confederation (REC)

> “Schools just want to know the check is done, when it was done and the recruitment policy.”

Some users told us that they take screenshots in Employer Access. A screenshot can include both the teacher reference number and the status box showing:

- if the teacher has any alerts, for example if they failed their induction or have been prohibited from teaching for serious misconduct
- the date when they got qualified teacher status (QTS) or early years teacher status (EYTS)
- their induction status, for example if they’re currently in their induction period

Other users told us that they print the record.

> “There isn't a ‘print’ link to be able to print or download the checks. That’s a requirement for an employer to hold time-stamped proof.”

We asked these users what they would do without a print button. Some tried using the `File > Print` browser commmand and were satisfied with the outcome.

Other users said that they would change their processes and take a screenshot instead of printing.

## Our design for showing when a search was made

We do not think that a print button is the best way to meet users’ needs.

Instead we’ve added a ‘time stamp’ to the service showing the date and time when:

- a search with no results was carried out
- a teacher’s record was accessed

We follow the GOV.UK style guide for the format of the [date](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#dates) and [time](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#times).

The text appears as a medium size [caption](https://design-system.service.gov.uk/styles/headings/#headings-with-captions). It uses [govuk-border-colour](https://design-system.service.gov.uk/styles/colour) grey, which helps to seperate it from the rest of the content.

As this time stamp is secondary to the main page content we do not want it to distract users from the record.

We think that the time stamp is not closely related to the `h1` headings of the pages on which it appears. So we’ve placed the caption in the `block beforeContent` section, which means it sits close to the breadcrumbs at the top of the pages.

We also considered placing the text within the breadcrumbs. For example it could say “Search results (2:53pm on 23 February 2024)”.

We were concerned that this could be confusing for users as it is not a standard use of the breadcrumb component.

### Time stamp when a search has no results

The time stamp at the top of the page showing no results says “Records searched at”.

We found through research that a significant number of users do searches when they expect to have no results.

For example they may want to check that someone applying for teacher training has not previously been prohibited from teaching.

Users may therefore need to keep evidence showing the date and time when they did a search which had no results.

We did not add the time stamp to a search page which does have results. We have not found that users need to store that page as evidence that they did a search. Instead they will print or take a screenshot of the teacher’s record once they reach it.

### Time stamp on a teacher’s record

The time stamp at the top of a teacher’s record page says “Record checked at”.

Adding the date and time to a teacher’s record means that users who print or take screenshots will be able to keep evidence of when they did the check.

It also makes it clearer that the data shown is correct at a particular time. It’s possible that something will change immediately after the record was checked.

## Testing the new design

We added this feature to the prototype so that we could test it with users. We wanted to make sure that:

- it’s useful for evidence
- users can use it to take a screenshot instead of printing the page
- it does not distract users from the rest of the page

## Further considerations

It would be better for users if they did not have to worry about keeping evidence.

Inspectors from Ofsted and REC have told us that they do not need as much evidence as many users believe. We could clarify this in guidance and communications.

We could also consider improving the way data is shared between services. For example there would be less need for users to keep evidence if we could share data between:

- our service
- the DfE teaching vacancies service
- inspecting bodies such as Ofsted and REC
