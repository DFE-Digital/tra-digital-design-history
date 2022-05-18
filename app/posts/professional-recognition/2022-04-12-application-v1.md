---
  title: Testing ideas on the application form – round 1
  date: 2022-04-12
  screenshots:
    items:
      - text: "Start page"
        src: start-page.png
      - text: "Task list"
        src: task-list.png
      - text: "Personal details example page"
        src: personal-details-names-dob.png
      - text: "Personal details file upload example"
        src: personal-details-upload-identification-document-before.png
      - text: "Question to understand if teacher training was done as part of a degree"
        src: education-qualifications-degree-separate-together.png
      - text: "Teacher training qualification example question"
        src: education-qualifications-teacher-training-title.png
      - text: "Teacher training file upload example"
        src: education-qualifications-teacher-training-upload-certificate-before.png
      - text: "Degree details example question"
        src: education-qualifications-degree-title.png
      - text: "Degree file upload example"
        src: education-qualifications-degree-upload-1-before.png
      - text: " Education and qualifications – check your answers"
        src: education-qualifications-teacher-training-check-answers.png
      - text: "Professional standing start page"
        src: professional-standing-start.png
      - text: "Registration number page"
        src: professional-standing-online-portal-enter-registration-number.png
      - text: "Letter of professional standing page"
        src: professional-standing-lops-upload-before.png
---

We prototyped the ‘apply’  element of our new service, as this was the next priority area of focus for us during alpha. 

There are a host of basic usability challenges with the current application form, detailed in discovery. These stimulate a high number of support queries, so we have a good understanding of these problems to supplement our user research.

How might we create an application form that is usable, accessible and inclusive?

## Insights that helped to inform the design 

- It is time consuming for many users to prepare an application. 
- There are many pieces of information and documents that are needed - some users know/have to hand, others that need to be sourced from a range of places.
- Users need help understanding where they can source some information, particularly around professional standing as a teacher.

## Our hypotheses

- Enabling users to save and return to an application form would improve the experience of applying for QTS, because it does not need to be completed in one session or require a user to have all documents to hand at once.
- Using a task list format will clearly break down the different required sections of the application, in turn, enabling a user to more clearly view the progress of their application and complete it for assessing.
- There is a significant enough commonality of users and user needs with other related live services (Apply for initial teacher training) to reuse some of their application/task list patterns. 

In line with our private beta approach to release the application form to currently-eligible users initially, we focussed the prototype on current eligibility criteria. There will be further work to do to later add the new criteria. 

We tested these iterations with 12 users. Of those participants, 6 were teachers from currently eligible countries, 2 more teachers were from to-be-eligible countries, and 4 were proxy users with accessibility challenges. 


## Research goals

- Hub and spoke model of task list - how does it help teachers work through application form?
- Qualifications section - how well does the flow help teachers understand what’s needed? (The information we need could vary depending on if teacher training was done alone or as part of a degree)
- Professional standing section - how does the question help teachers understand what’s needed?
- File upload - How accessible and usable is it?
- Are there any accessibility issues with the application form design?

## Key learnings

- Teachers liked the simple structure of the task list. They all followed it in sequential order. They understood the status indicators - not started, in progress, completed.
- Some teachers would want to tackle the application form in chunks, particularly if they have a mobility condition, so would welcome a save and return function. (there was no explicit save and return functionality in this iteration). 
- Some teachers want to print a full summary page to check before they submit. Without this they would be anxious and feel reluctant to submit (we had not yet added a ‘check your answers’ summary). 
- Some users struggled with the way the design asked about their teaching qualification and degree details. They didn’t understand the initial question and found the flow of questions lengthy and confusing.
- Most still did not understand  “professional status” and how they might demonstrate it.
- Most teachers were familiar with the file formats (for document upload) but some were confused because their documents were stored in Google drive so they thought of them as google docs.
- Some teachers found the ‘legal name’ question straightforward and inclusive. But others were confused because of how they used their married name or for example, in Spain and Portugal people have two official last names but only use one day-to-day (we have a current  data integration constraint around using the standard single-field name pattern).
- Long scrolls as required can be tiring and painful for teachers with mobility conditions. For example long lists of countries in drop downs, and the summary page.
