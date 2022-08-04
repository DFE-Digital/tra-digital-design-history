---
  title: Reporting misconduct, for members of the public
  date: 2022-08-04
  screenshots:
    items:
      - text: "Reporting as a member of the public"
        src: 01-reporting-as-member-of-the-public.png
      - text: "Have you already made a complaint?"
        src: 02-already-made-a-complaint.png
      - text: "No: You need to complain first"
        src: 03-you-need-to-complain.png
      - text: "Your report"
        src: 04-your-report.png
      - text: "Your details: Your details will not be shared"
        src: 05-your-details-will-not-be-shared.png
      - text: "Your details: Relationship to person"
        src: 06-relationship-to-person.png
      - text: "Your details: Check answers"
        src: 07-check-answers-for-your-details.png
      - text: "Person you are reporting details: Name"
        src: 08-teacher-name.png
      - text: "Person you are reporting details: Check answers"
        src: 09-teacher-details-check-answers.png
      - text: "Person you are reporting contact details: Email"
        src: 10-teacher-email.png
      - text: "Person you are reporting contact details: Check answers"
        src: 11-teacher-contact-details-check-answers.png
      - text: "About their role: Are they still in role?"
        src: 12-still-in-role.png
      - text: "About their role: Where did they work?"
        src: 13-where-did-they-work.png
      - text: "About their role: Describe their main duties"
        src: 14-describe-main-duties.png
      - text: "About their role: Check answers"
        src: 15-about-their-role-check-answers.png
      - text: "Allegation: Tell us how this complaint has been considered"
        src: 16-tell-us-how-this-complaint-has-been-considered.png
      - text: "Allegation: Tell us briefly what happened"
        src: 17-tell-us-briefly-what-hapened.png
      - text: "Allegation: Give a detailed account"
        src: 18-give-a-detailed-account.png
      - text: "Allegation: Check answers"
        src: 19-allegation-check-answers.png
      - text: "Evidence: Do you have evidence to upload?"
        src: 20-evidence-to-upload.png
      - text: "Evidence: Check answers with nothing to upload"
        src: 21-no-evidence-check-answers.png
      - text: "Evidence: Files uploaded"
        src: 22-files-uploaded.png
      - text: "Evidence: File types"
        src: 23-file-types.png
      - text: "Evidence: Check answers"
        src: 24-evidence-check-answers.png
      - text: "Review before sending"
        src: 25-review-before-sending.png
      - text: "Declaration"
        src: 26-declaration.png
  related:
    sections:
      - title: Related content
        items:
          - text: Prototype PR
            href: https://github.com/DFE-Digital/teacher-misconduct-prototype/pull/37
          - text: Content tweaks PR
            href: https://github.com/DFE-Digital/teacher-misconduct-prototype/pull/39
---

How the Report serious misconduct by a teacher service needs to change for members of the public, compared with the [current designs, which are for employers](/teacher-misconduct/report-serious-misconduct-iteration/).

## Changes for the public

### Eligibility screener

Add an initial question to see if the member of the public has already followed local procedures, by complaining to school, governors or local authority

If they haven’t, point them to a page on GOV.UK telling them how.

### Your details

State that your details will not be shared before filling in this section.

Do not ask for job title, instead ask for their relationship to the person being reported

### Person being report details

Do not ask if the person has changed their name.

Do not ask for National Insurance number, Teacher reference number (TRN) or Qualified teacher status (QTS). They are unlikely to know this.

### Teacher role

Do not ask for the date they started in the role, they will not know this. Instead ask for a job title first.

Ask if they are still working and include an 'I don’t know' option, but do not ask for when they stopped working, or how they left the job, as they are unlikely to know.

Do not ask for a job description file upload, they will not have this. And when asking about main duties, reduce the size of the field to make it less imposing – they will have much less to say about those duties.

Do not ask if they worked in the same organisation as the user, just ask which school they were in.

Continue to ask if they are teaching elsewhere if the person has left the job

### Contact details

Ask for any email address rather than a personal one, any will do.

Continue to ask for telephone numbers and addresses, they may know these. For example, if a teacher has been privately messaging a child, or a child has been to their house.

### Allegation

Ask first about existing complaints and how they were handled. (We may end up splitting this section into multiple parts)

Do not ask about whether they have referred to DBS.

Remove guidance about uploading an investigation report, it’s unlikely they will have this.

### Evidence and documentation

Use a different list of files, for example communication with schools and copies of complains (the prototype includes different examples for research)

### Tasks and review

Do not show the ‘Your organisation’ section, where they work isn’t relevant.

Do not ask about previous misconduct, they probably do not know about this.

Remove the clause about getting third party permission in the declaration, to match the current Word form.
