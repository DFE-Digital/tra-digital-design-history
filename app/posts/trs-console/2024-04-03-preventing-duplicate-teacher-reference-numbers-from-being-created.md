---
title: Preventing duplicate teacher reference numbers from being created
date: 2024-04-03
description: Checking potential duplications before a new TRN is created.
screenshots:
  items:
    - text: Support tasks landing page
      src: support-tasks-landing-page.png
    - text: Check if the request is a duplicate
      src: check-duplicate.png
    - text: Check a request where there is a teaching restriction
      src: check-alert.png
    - text: Confirm allocating a new TRN
      src: confirm-new-trn.png
    - text: Choose which details to merge
      src: choose-details.png
    - text: Request and record successfully merged
      src: record-merged.png
---

Teacher reference numbers (TRNs) are generated when:

- an initial teacher training provider requests one for a new teacher using the Register trainee teachers service
- an international teacher is given qualified teacher status (QTS) after using the Apply for QTS in England service
- a teacher starts employment and is registered for a pension

We try to avoid duplicates by:

- using a different range of numbers for each of the 3 ways in which TRNs are created
- synchronising data daily

However, it’s still possible for a TRN to be requested for someone who already has one.

The most common situation is that a trainee is registered on a training course and for a pension at around the same time.

Usually this happens at the start of the academic year, when 2 members of support staff focus full time on fixing duplication. There are approximately 6,000 de-duplication tasks each year.

## Avoiding duplication rather than fixing it

Instead of fixing duplicates after a second TRN has been issued, we now try to avoid the creation of the second TRN.

When a request is made for a new TRN, the system automatically checks if the details provided already exist in a teaching record.

If there’s a possible match then the new TRN request is not fulfilled. It instead enters a pending status and a support task is generated to check if the new request is a duplicate.

## Support task

For support tasks we follow a pattern where we use:

- a summary list for data which has been submitted but is not part of a record
- a summary card for data which forms a teaching record

That means that for this task:

- the new TRN request is shown in a summary list
- any existing records which are possible matches are shown in summary cards

Some records have a restriction such as a prohibition order. If one of the possible matches has a restriction then we show a notification banner. The support user will ask the teacher misconduct team to review the new TRN request.

### Deciding whether to use an existing TRN or allocate a new one

The support user must choose between:

- using an existing TRN - if the new TRN request is a duplicate
- allocating a new TRN - if the new TRN request is not a duplicate

If there are multiple possible matches then we display them and the user can choose which TRN to use.

### Merging personal details

If the support user chooses to use the existing TRN then we show a screen where they can select which personal details to keep. This includes:

- first name
- middle name
- last name
- previous names
- date of birth
- gender
- email address
- National Insurance number

We do not show ITT or other qualifications because the new TRN request should not include them.

We only show details which are different between the new TRN request and the selected record. If a detail is the same in both then we assume that the support user wants to keep it.

We do not show the screen if there are no differences at all between the new TRN request and the selected record.

#### How we display the choice of personal details

The design uses a 3 column table. We show the personal detail for the new request and existing record, with an input for each.

For each personal detail which we show, we have the new TRN request on the left and the existing record on the right. There’s an option to select all, which has no validation so that it can be skipped.

Radio buttons are used to choose between sources of data. We use [inline small radio buttons](https://design-system.service.gov.uk/components/radios/#:~:text=in%20services.-,Smaller%20radios,-Use%20standard%2Dsized) because this is a frequent use interface. We do not need to make the buttons more prominent.

We use checkboxes instead for previous names because users may want to keep both sources. We need to:

- test if it’s confusing to mix checkboxes and radio buttons
- find out if we need to use checkboxes for any other fields where users may need to use both sources

We may decide to split the decisions so that there’s one screen with radios and another screen with checkboxes. This would avoid mixing input types but there may sometimes be only one choice on one of the screens.

### Checking answers

After the support user chooses which personal details to keep, they’re taken to a check answers page.

We show the new record in a summary card so that the support user can see how it will appear with the selected personal details.

In the initial design, the change links on the check answers page return to the previous screen. We may decide to add a way to manually change fields, for example if both sources have different spellings of a name that are slightly wrong.

For now support users will need to use the ‘make manual PII changes’ feature of the TRS console after completing the de-duplication task.

### Updating the change history

If the request and record are merged then we add a change history event to say they were merged.

If any data is deleted then we include a reveal for ‘previous data’. This will allow support users to check what was deleted and fix any mistakes.
