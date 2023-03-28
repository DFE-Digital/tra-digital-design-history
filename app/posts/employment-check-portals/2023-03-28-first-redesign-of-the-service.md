---
  title: First redesign of the service
  date: 2023-03-28
  screenshots:
    items:
      - text: 
        src: 
     
---

Before employing a teacher, employers need to check their record for:

- qualified teacher status (QTS)
- completion of teacher induction
- any prohibitions, sanctions and restrictions that might prevent the teacher from teaching
- any additional qualifications, including relevant mandatory qualifications

At the moment, schools, local authorities, teacher supply agencies and other employers can check a teacher’s record.

But the current system is complicated and not user-centred. It also causes potential accessibility issues, for example by not using clear page fields and headers.

So we’ve created a new design to make it clearer and simpler to use.

## What we changed

### Naming the service

At the moment, the name of the service is [Employer Access](https://teacherservices.education.gov.uk/).

Following [GDS guidelines](https://www.gov.uk/service-manual/design/naming-your-service), we need a name that:

- helps users to understand what the service does
- makes the service easy to search for

So we named the service ‘Check the record of a teacher in England’.

### Searching by teacher reference number (TRN)

At the moment, users can search for a teacher using their:

- teacher reference number (TRN)
- date of birth

We want to make it easy for a user to find the teacher’s record they’re looking for.

So we’ve allowed users to search using a single unique identifier - the TRN. Searches initially return a teacher’s name and organisation. This will help users check they’ve found the right teacher before they access their full record.

### Filtering by teachers who have restrictions

At the moment, users need to search 4 different lists of prohibitions, sanctions and restrictions. This puts the burden on the user. It also causes potential accessibility issues, for example by using dropdown menus when users select from a list.

So we’ve created filters to search for:

- restrictions
- no restrictions

The user can then click on a teacher’s record for more details of the specific restriction. For example:

- the date the restriction was applied
- the date the restriction will be reviewed (if applicable)
- how the restriction affects the teacher’s ability to teach, for example if they can only work at certain types of school

### Filtering by  organisation

At the moment, users need to carry out various searches to find out where a teacher is employed.

So to make this simpler, we’ve created filters to search for teachers who are:

- part of the user’s organisation (‘your organisation’)
- part of a different organisation (‘another organisation’)
- not currently part of any organisation (‘no organisation’)


### Adding a teacher to an organisation

At the moment, users can ‘Claim a teacher’. This adds a teacher to their organisation, so they have easy access to their record.

We’ve made this simpler by adding a link within a teacher’s record: ‘Add to your organisation’.

### Simplifying the content

At the moment, the service uses a range of complicated terminology.

We’ve made this simpler by:

- writing out acronyms in full on first use, for example ‘teacher reference number (TRN)’
- combining similar terminology (‘prohibitions’, ‘alerts’) into a single term: ‘restrictions’
- making labels clearer, for example changing ‘date of partial recognition’ to ‘date partial QTS awarded’

### Changing the layout of the record page

We’ve grouped the information so it’s in a logical order that’s easier for users to scan.

For example, we’ve flagged any restrictions at the very top of a teacher’s record. We’ve also kept qualifications close together, as well as personal and organisation details.

## Further considerations

We’re planning to test these designs to understands the user needs for:

- what different users need to see and do, for example features and permissions
- finding banned or restricted teachers
- doing a ‘light’ DBS check
- reviewing 1 of the 4 ‘restricted’ lists of users
- employer ID, name and address
- if ‘Yes’ is a clear enough answer to ‘Are they eligible to complete a one-year induction period?’
- any legislation checks

We also want to consider if there are other ways to improve data security. This includes:

- monitoring if users attempt to view multiple TRNs in a single session
- investigating how we might allow teachers to grant employers access to their record

