---
title: Changes to the form
date: 2022-12-23
screenshots:
  items:
    - text: Start page
      src: start.png
---

Based on user research and internal design reviews, we changed the end-to-end journey for both employers and members of the public to make it easier to refer serious misconduct by a teacher.

## What we changed

### Referring to the TRA

At the moment, we use ‘we’ when referring to the TRA to keep the tone conversational. However, this may create ambiguity for users when dealing with multiple government departments. For example, ‘we’ could mean DfE.

Following the [GOV.UK Style guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style), we decided to:

- write out the full name of the department when it’s first mentioned on every page - ‘the Teacher Regulation Agency (TRA)’
- abbreviate to ‘the TRA’ for all subsequent mentions
- use direct actions wherever possible to give the user clear instructions, for example ‘you’ll receive an email’

### Changing ‘person’ to ‘teacher’

At the moment, we use ‘person you’re referring’ when talking about who the allegation is about. This makes sense when asking if somebody is eligible to be referred, as we do not know yet if they’re a teacher or not.

Once we’ve confirmed that somebody was employed as a teacher, we’ve changed the content to refer to them as ‘the teacher’ throughout.

This is consistent with the name of the service.

### Other content changes

We also made some other small content changes. These included:

- using statements to be more concise and frontloaded, for example ‘Your name’ instead of ‘What is your name?’
- adding hint text for the user when providing the first name (‘or given name’) or last name (‘or given name’) of the teacher, making it more inclusive
- adding hint text to help users provide details of any other name for the teacher - ‘For example, if they’ve changed their name after getting married’
- making it clear what types of organisation can be referred by adding a clear definition on the ‘Your organisation’ page - for example, schools and sixth form colleges
- adding explanations about why we ask for certain information in the ‘Personal details’ after some participants showed some hesitation in testing - ‘This information is required by law. It’ll help us to identify the person you’re referring and decide if we need to investigate the case further’
- reducing the number of bullet points on the ‘Detailed account of previous allegations’ page to remove duplicate content and make it easier to read

### Removing negative contractions

At the moment, we use some negative contractions. For example, ‘I haven’t received an email’.

The [GOV.UK Style](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style) guide recommends avoiding these wherever possible. Some users can find them harder to read, or misread them as the opposite of what they say.

We’ve now spelled them out for clarity, for example ‘I do not want to continue’.

### Changing ‘I do not know’ to ‘I’m not sure’

At the moment, there’s some ambiguity between ‘No’ and ‘I do not know’ when giving a list of radio options - for example, when asking about any previous misconduct. For clarity, we changed the options to:

- Yes
- No
- I’m not sure

### Changing the referral confirmation page content

In user research, people said they wanted a clearer idea of dates and timeframes. For example, how long it’ll take the TRA to review their referral.

We added this information under the ‘What happens next’ section to make these next steps clearer. For example: ‘Your referral will be reviewed within 3 working days’.

We also:

- changed the h1 from ‘We have received your referral’ to ‘Referral sent’
- updated the TRA contact details to make it clear that the phone line is available Monday to Friday, 9am to 5pm

### Removing ‘I’ll do this later’ options

At the moment, we give users the option of returning to complete a task later. For example, when providing details of the allegation.

However, removing the ‘I’ll do this later’ option also raises some problems. It means we cannot show the ‘Have you completed this section?’ question at the end of a task. Users would need to remember that they need to return to answer the question later or be given a prompt.

Also, we include a task list. This allows users to track their progress using the status of task statuses (for example: ‘Not started yet’) and return to the form at any time. Breaking down tasks also means users should be able to complete them in one go for the most part.

Instead, we’re planning to split this into a separate task if we confirm it’s a valid user need.

### Changing ‘Are they teaching somewhere else?’ to ‘Are they employed somewhere else?’

At the moment, we ask ‘Are they teaching somewhere else?’ This was based on our assumption that it was only the person’s teaching status that needed to be captured.

However, caseworkers explained that they want to know where they’re working so they can notify the new employer of any serious misconduct.

We changed the question to ‘Are they employed somewhere else?’ to make it more precise.
### No longer hiding the definition of teaching work behind a toggle

At the moment, we give a definition of teaching work on the ‘Who the allegation is about’ page. This definition is contained in a Details component.

It’s unnecessary to hide content, so we’ve now made it visible to everybody.

### Asking employers if they know when the person left the job

At the moment, we ask users ‘When did they leave their job?’ But some users might not know this information.

We added a question - ‘Do you know when they left the job?’ - to check if the user knows this date. This means users will only be asked to enter the job end date if they know it.

### No longer conditionally revealing multiple questions or addresses

At the moment, we conditionally reveal fields like addresses or other questions made up of multiple inputs.

However, the GOV.UK Design System says: ‘Keep it simple. If the related question is complicated or has more than one part, show it on the next page in the process instead.’

We changed this to show the inputs on the next page instead.

### Reducing example evidence list

At the moment, we show a long list of different types of evidence.

However, we think this is unnecessary. It may also suggest it’s an exhaustive list.

We reduced the examples to some of the most commonly used.
### Changing the order of questions in the ‘About their role’ task

We re-ordered the questions to make them more logical and avoid moving back  around too much between different points in time.

For members of the public:

1. Their job title
2. How do you want to give details about their main duties?
3. Do you know the name and address of the organisation where the alleged misconduct took place?
4. Name and address of the organisation where the alleged misconduct took place (if the user selects ‘Yes’)
5. Check and confirm your answers (if the user selects ‘No’)

For employers:

1. Their job title
2. How do you want to give details about their main duties?
3. Were they employed at the same organisation as you at the time of the alleged misconduct?
4. Do you know the name and address of the organisation where the alleged misconduct took place? (if the user selects ‘No’)
5. Name and address of the organisation where the alleged misconduct took place (if the user selects ‘Yes’)
6. Do you know when they started the job?
7. Are they still employed at the organisation where the alleged misconduct took place?
8. Do you know when they left the job? (if the user selects ‘No’)
9. Reason they left the job (if the user selects ‘No’)
10.  Are they employed somewhere else?
11. Do you know the name and address of the organisation where they’re employed? (if the user selects ‘Yes’)
12.  Name and address of the organisation where they’re employed (if the user selects ‘Yes’)
13. Check and confirm your answers

### Asking additional questions about the teacher

We changed the content to ask about where the teacher:

- was employed at the time of the allegation
- is employed now

Based on the type of allegation and employer, caseworkers will then decide whether the new employer needs to be informed.
### Making all h1 headings the same size

At the moment, we have a mix of h1 heading sizes.

We changed all headings to ‘large’ for consistency. This allows for slightly longer questions to stay under 3 lines, which are easier to scan.
### Adding h1 heading captions that reflect the name of the task

We want to keep questions short but we also want to make them clear.

At the moment, we ask ‘What is the name of the person you’re referring?’ in the ‘About the teacher’ section.

We added the caption ‘Personal details’. This allowed us to shorten the question to ‘Their details’, making the page easier to read without losing clarity.

### Making the declaration page clearer

In user testing, some participants were unsure who counted as a ‘third party’ when making a declaration.

We added ‘for example the police or DBS’ to make it clearer.
## Further considerations

In the future, we’ll consider:

- splitting out ‘main duties’ into a separate task to account for ‘I’ll do this later being removed’
- providing a way to get back into a partially completed form
- what happens when a user doesn’t receive an email when first creating a referral
- what happens when a user deletes a draft referral
