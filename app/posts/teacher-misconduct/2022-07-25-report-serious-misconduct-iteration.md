---
  title: Report serious misconduct – iteration
  date: 2022-07-25
  screenshots:
    items:
      - text: "Updated start page"
        src: 01-start-page.png
      - text: "Jurisdiction: Were they teaching in England?"
        src: 02-were-they-teaching-in-england.png
      - text: "Save as you go"
        src: 03-save-as-you-go.png
      - text: "QTS: Do they have QTS?"
        src: 04-do-they-have-QTS.png
      - text: "QTS: Check answers with QTS"
        src: 05-check-answers-with-QTS.png
      - text: "Asking for personal email address"
        src: 06-persons-personal-email-address.png
      - text: "Role iteration: Are they still employed?"
        src: 07-are-they-still-employed.png
      - text: "Role iteration: Main duties"
        src: 08-main-duties.png
      - text: "Role iteration: Main duties (expanded)"
        src: 08-main-duties-expanded.png
      - text: "Role iteration: Are they teaching somewhere else?"
        src: 09-are-they-teaching-somewhere-else.png
      - text: "Role iteration: Where are they teaching now?"
        src: 10-where-are-they-teaching-now.png
      - text: "Role iteration: Check answers"
        src: 11-check-answers-for-role.png
      - text: "Summary: Allegation summary"
        src: 12-allegation-summary.png
      - text: "Summary: Previous allegations summary"
        src: 14-previous-allegations-summary.png
      - text: "Any previous allegations iteration"
        src: 13-any-previous-allegations.png
      - text: "Upload evidence: Evidence and supporting information"
        src: 15-evidence-and-supporting-information.png
      - text: "Upload evidence: Upload files"
        src: 16-upload-files.png
      - text: "Upload evidence: Confirmation"
        src: 17-uploaded-confirmation.png
      - text: "Upload evidence: Categorise files"
        src: 18-uploaded-categorisation.png
      - text: "Upload evidence: Check your answers"
        src: 19-check-your-answers-uploaded.png
      - text: "Delete draft: I don’t want to continue"
        src: 20-i-dont-want-to-continue.png
      - text: "Delete draft: Are you sure you want to delete?"
        src: 21-are-you-sure-you-want-to-delete.png
      - text: "Delete draft: Report deleted"
        src: 22-report-deleted.png
      - text: "Full report review"
        src: 23-full-report-review.png
      - text: "Returning to service: To continue"
        src: 24-returning-to-continue.png
      - text: "Returning to service: With multiple reports"
        src: 25-returning-with-multiple-reports.png
      - text: "Returning to service: With a completed report"
        src: 26-returning-with-a-completed-report.png
      - text: "Returning to service: Expanded to add new report"
        src: 27-returning-expanded.png
---

We have:

- tested the prototype with 6 teachers who’ve previously reported serious misconduct
- demo'd the designs to caseworkers and policy

Following research and demos we've made many small design changes. We made changes as we went, not all users saw the latest designs.

The overall form structure has tested very well.

## Walkthrough of changes

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('733213657') }}

## Saving as you go

Before research we highlighted the need to [complete the form gradually](/teacher-misconduct/report-serious-misconduct-by-a-teacher/#completing-gradually), to be able to save and return. While this is the case, we did not make it obvious enough.

We kept adding to the service, each step aiming to make it more obvious:

- added hint text about why we were asking for an email address
- added context to the start page, saying that sections are saved as you go
- added a page in the initial eligibility flow, pointing out that progress is saved as you go
- updated all buttons to say ‘Save and continue’ rather than just ‘Continue’

We still need to confirm this is enough to allay any fears.

![Saving as you go page](03-save-as-you-go.png)

## Uploading evidence

We’ve completed the designs of the upload section. Previously we were testing with a minimal version. It was a good straw-person design for highlighting needs.

We found that:

- users wanted to see a list of files first, as a sort of checklist for what to upload
- users want to upload multiple files at once
- we needed to tweak wording when categorising files to make it clear you can select multiple categories

The new flow:

- gives a list of suggested files at the beginning
- allows users to upload multiples
- shows a screen for categorising each uploaded file
- lists files and their categories on the check your answers page
- adds actions for changing categories, deleting files and adding more evidence

![Evidence and supporting information](15-evidence-and-supporting-information.png "Evidence and supporting information")

![Upload files](16-upload-files.png "Upload files")

![Uploaded confirmation](17-uploaded-confirmation.png "Uploaded confirmation")

![Uploaded categorisation](18-uploaded-categorisation.png "Uploaded categorisation")

![Check your answers – uploaded](19-check-your-answers-uploaded.png "Check your answers – uploaded")

## Deleting a report

Some users will not want to continue. Perhaps they no longer wish to submit a report, someone else is reporting, or they are submitting using the Word document.

They might want to delete sensitive information they have given.

We have designed a feature to allow them to delete their draft report, and highlighted our data retention policy for draft reports (6 months, but this isn’t finalised).

![I don’t want to continue](20-i-dont-want-to-continue.png "I don’t want to continue")

![Are you sure?](21-are-you-sure-you-want-to-delete.png "Are you sure?")

![Report deleted](22-report-deleted.png "Report deleted")

## Summaries of allegations

Case workers told us they found it difficult to quickly gauge what a case is about. The allegation and previous allegation sections contain a long and detailed account of what has happened, it is difficult to extract the essentials from this report.

We’ve added two new fields:

- allegation summary
- previous allegations summary

The hope is that users will give 2 or 3 sentences to explain what has happened, and case workers can easily get an idea of the case (what it relates to, severity, complexity) before continuing.

Research so far shows that some users would still put in too much information here. We need to make it clearer.

![Asking for allegation summary](12-allegation-summary.png "Asking for an allegation summary")

# Asking if the person has QTS

We could determine QTS status from a TRN, if given. But there's a chance that the TRN is incorrect – the wrong one is given or there is a typo.

Instead we will explicitly ask about QTS, and employers will know this.

![Do they have QTS?](04-do-they-have-QTS.png)

## Asking for the person’s email address

We made it explicit we wanted their personal email address. Users defaulted to giving us work email addresses, even if the person had left their job.

Users told us they would usually have a personal email address on a job application form.

Some were concerned about how we would use the email, they wanted assurances about when the person would be contacted.

Others questioned if they could share this information with us, they were concerned about GDPR.

## Asking if they are still employed

Previously we asked:

> "[Have they left this job?](/report-serious-misconduct-by-a-teacher/#previous-misconduct-any-previous-misconduct)"

This caused confusion – what does "leaving a job" mean – has a suspended teacher left their job? They are still employed but they are not teaching.

We added an option to help with suspended teachers, and changed the question to:

> "Are they still employed?"

This still wasn’t quite right, someone that has left their job but has started teaching elsewhere is "employed". We tweaked the question again to say:

> "Are they still employed in that job?"

![Are they still employed in that job?](07-are-they-still-employed.png "Are they still employed in that job?")

## Asking about onward employment

If a user tells us the person has left that job, we now ask two further questions:

- do they know if they are still teaching
- if so, do they know where

We believe this information would be helpful to case workers that need to serve interim prohibition orders (IPOs). But we still need to determine how useful this information would be.

## Giving main duties in a file

One user highlighted a problem with out design – we asked for a teacher’s main duties, and hinted that they could upload this in a file. The issue here was that the file upload was in another section. This led to confusion – at the end, when marking a section as complete – is this section complete? They haven't uploaded the file yet.

To solve this we moved the job description file upload into the same section. The old design remains available as a choice, and a third option has been added, "I’ll do this later", if they do not have the file to upload.

If they tell us they’ll do this later, then the section cannot be marked as completed until they’ve changed that answer.

We expect to reuse this pattern for allegations and previous allegations.

![Asking for a job description upload](08-main-duties.png "Asking for a job description upload")

## Jurisdiction in England

Technically it matters that they were a teacher in England during the allegation. We've made that clearer, and because of the increased complexity of the question we’ve added an "I don't know" option, to encourage reports.

![Were they a teacher in England?](02-were-they-teaching-in-england.png "Updated question text")

### Previous allegations

A user misinterpreted our [original design](/report-serious-misconduct-by-a-teacher/#previous-misconduct-any-previous-misconduct), they incorrectly determined that we did not want to know about complaints and disciplinary action at their school.

We’ve made it explicit that we do want to know this.

![Updated hint text for previous allegations](13-any-previous-allegations.png "Updated hint text for previous allegations")

## Returning to the service

We’ve begun experimenting with designs that allow users to:

- return to a draft report
- check updates on a completed report
- see multiple reports
- start a new report, to report something new
