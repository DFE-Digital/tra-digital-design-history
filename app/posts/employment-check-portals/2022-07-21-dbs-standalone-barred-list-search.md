---
  title: DBS standalone barred list search
  date: 2022-07-21
---

## Background

Schools and other relevant employers (e.g. colleges) must conduct their recruitment practices in line with part three of the statutory safeguarding guidance [Keeping Children Safe in Education](https://www.gov.uk/government/publications/keeping-children-safe-in-education--2) (KCSIE). A requirement is to ensure an individual has no active barring imposed on them by the Disclosure and Barring service (DBS). In most cases, schools must conduct these checks directly with the DBS in the form of an enhanced check.

In specific circumstances a school, college, local authority or university can conduct a ‘standalone check’ against the barred list, these circumstances being where a new starter:

* has a pending enhanced DBS check, or
* where an individual has worked in post in a school/college that brought them into regular contact with children/young persons (which ended not more than three months prior to that person’s appointment

The department delivered a standalone check service through an external supplier until 31 March 2021. TRA began delivering this service on behalf of the DfE from 1 April 2021, offering the ‘standalone check’ through the Employer Access service.

## Design of the current TRA standalone check service

### Access control

Not all users of Employer Access are allowed to conduct a standalone check. Whether a user can conduct a check depends on the organisation they are associated with when they log into Employer Access. The main categories of organisations that can conduct a check are:

* schools
* colleges
* universities
* local authorities

An internal yes/no flag controls whether a user can ‘see’ the standalone check within Employer Access. This is set at the organisation level as the ‘organisation types’ used within the database are not granular enough to allow for the access controls on the search the policy demands.

### Search

The standalone check service is available via Employer Access - Schools and Employer Access - Organisations. It is not available via ITT provider or Appropriate bodies.

The search is an additional function separate to the main teacher reference number and date of birth search on Employer Access. The TRA receives the data to inform the search directly from DBS.

The user must confirm they are eligible to ask an exempted question, and then searches using an exact match on ‘surname’ and ‘date of birth’ (red highlighted in image), and the result (blue highlighted in image) notes if:

* a match occurs to ≥1 record on both fields - the service reports a message of ‘possible match - please contact DBS using the above details’
* no match occurs - the service reports no match occurs

[![Searching the DBS standalone barred list](search.png)](search.png)

The primary change to the service since go live is the addition of the ‘You searched for …’ replay text (also in blue in the image) based on user feedback, as for auditing purposes they required a single screen that displayed the details of:

* ‘who’ they searched for (i.e., replay the searched for ‘surname’ and ‘date of birth’)
* ‘when’ they searched (i.e., replay the date the search was run)
* ‘the outcome’ of the search (i.e., replay ‘no match’ versus ‘possible match’)

### Potential improvements

The existing search form, using ‘surname’ and ‘date of birth’, mirrors the predecessor service. Adding extra personal identifiers could help avoid inaccurate ‘no match’ outcomes e.g. for someone whose surname has changed and no longer matches the surname on record.

Future analysis and design could explore:

#### Adding extra attributes to increase confidence in matching

For example, if we used TRN (teacher reference number) and/or National Insurance number, could we match solely against these items to produce a ‘possible match’?

#### Fuzzy matching

As we do not report exact matches (i.e., the ‘potential match’ message), there may be scope to make the search ‘looser’ than if we were having to identify someone robustly. For example, a match on date of birth and the initials (if we had full name) could count as a ‘possible match’ to account for misspelling of name data. This would likely lead to non-accurate matches, imposing a burden on users that may outweigh the potential strengthening of the search from a safeguarding stand point.

#### Improvements to the user journey

Currently the search is a static page the user interacts with. An alternative one-question-per-page journey could allow a user to gradually enter more information until they reach the point a match occurs/they run out of identifiers to search against.

We have had isolated feedback from the helpdesk that some users are not fully aware of the next steps if they find a ‘possible match’. The returned value in the search does advise them to ‘contact the DBS’, but as the phone number is contained within the descriptive text of the service it is not very clear for users.
