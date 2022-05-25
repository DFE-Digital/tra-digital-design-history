---
  title: Testing ideas on the application form – round 2
  date: 2022-05-03
  screenshots:
    items:
      - text: "Task list from before"
        src: task-list.png
      - text: "Task list after changes"
        src: task-list-before.png
      - text: "Question to understand if teacher training was done as part of a degree from before"
        src: education-qualifications-degree-separate-together.png
      - text: "Question to understand if teacher training was done as part of a degree after changes"
        src: was-teacher-training-a-degree.png
      - text: "Example of study period questions from before"
        src:  education-qualifications-degree-study-dates.png
      - text: "Example of study period questions after changes"
        src: teacher-training-study-period.png
      - text: "Age range question from before"
        src: education-qualifications-teacher-training-age-range.png
      - text: "Age range question after changes"
        src: teacher-training-age-range.png
      - text: "Professional standing – registration number screen"
        src: registration-number-example.png
      - text: "Professional standing – Letter of professional standing example screen"
        src: letter-of-professional-standing-example.png
      - text: "Professional standing – No letter of professional standing available example"
        src: no-professional-standing-example.png
---

Prioritised changes, based on the previous round of user testing of the application for [the first version of the application form](/professional-recognition/application-v2): were

## Overall

- Split the form and document upload tasks to reduce feelings of being overwhelmed / lost
- Professional standing spoke: amended the flow of questions and customised information to be country specific
- Qualifications: split out teacher qualifications from degree tasks, this reduces the questions for teachers who have a degree level teaching qualification
- We asked users for translations of official documents where needed


## Qualifications section

- Split the teacher training qualification from degree
- Adjusted size of ‘subject’ text input field to give users a better sense of the amount of detail needed
- Removed ‘day’ from the date
- Changed ages qualified to teach to free text input


## Professional standing

- Replaced the ‘how will you prove this’ picker with logic (which would be driven by the country they picked in ‘where are you recognised to teach’). This will require a database of countries/sources of proof.
- Added ‘where you would get this from’ reveal that shows where users would get evidence of their professional standing.

This was tested with 11 teachers from 7 countries.
We also tested with 2 proxy users with accessibility challenges.

## Key learnings

- Overall users understood and were able to use the hub and spoke application pattern however they were confused with the “not needed” for undergraduate degree. Many were able to complete the form quickly and relatively easily.
- Teachers still do not understand what ‘professional standing’ is and what is being asked for, even when shown the content of where to obtain a letter of professional standing.
- Splitting the teacher training qualifications and degree works well for teachers with a simple training degree like a B.Ed, but does not work well for teachers with multiple teacher qualifications because they do not know which one to provide information about. The problem with multiple qualifications affects all the questions in the task including institution and dates.
- Some users are anxious about the ‘have you completed this section’ radio button - they were not sure if they could return to this section. This is a GDS pattern, and used for the related Apply for initial teacher training service - we have shared this feedback with them.
- We need to consider how to handle multiple doc uploads. We have ideas which we did not get the chance to test this round.
- Some users struggle with the first name / surname pattern. We expected this but are constrained by data integration at present.
- Some users misinterpreted why we ask for their date of birth.
