---
title: Showing teachers’ middle and previous last names
date: 2023-11-15
screenshots:
  items:
    - text: Search results for a teacher with a middle name and previous last names
      src: search-results.png
    - text: Record for a teacher with a middle name and previous last names
      src: teacher-record.png
---

In the Employer Access service, users search for teachers by their teacher reference number (TRN) and date of birth. Since the TRN is unique, a successful search gives only one result.

In the new service, [users search by last name and date of birth](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/only-allowing-users-to-search-by-name-and-date-of-birth/).

This means that a search will give multiple results if more than one teacher has the same last name and date of birth.

In addition, the search uses previous last names as well as current last names.

The database of qualified teachers has around 2.8 million records and about 25% of them have at least one name change. Most of these changes are to the last name.

This means that users will sometimes see unexpected results. For example, if a user searches for Patel then they’ll see teachers whose current or previous last name is Patel.

If a user knows the teacher’s TRN then they can easily choose the right search result.

Users who do not know the TRN should not need to click into several records to find the right one. This would be a waste of their time and mean that they see information which they do not need to see.

## What we changed

We’ve decided to show middle names and previous last names:

- in search results, to help a user choose the right teacher
- in teacher records, to reassure a user that they’re looking at the right record

Middle names appear as part of the teacher’s name.

Previous last names appear as the last item in the ‘personal details’ section. This means that if there are no previous last names, the other items in the section will still appear in the same order.

Each previous last name appears on a separate line to make them easy to read. We are not worried about using too much space, as very few records have more than 2 last name changes.

## Further considerations

The database of qualified teachers has around 6,000 records with changes of first or middle names.

We’ve decided not to show these changes because name changes can be sensitive. We think it’s important to show last name changes as they help explain the results of a search. We do not have evidence that it’s important to show other changes.

We could consider showing first and middle name changes if we find that users need more help to find the right teachers. We’d need to consider the effect on teachers’ privacy.

We’d also like to find out whether we could avoid showing minor changes, such as to correct spelling mistakes. We do not know whether we could do this using the information in the database of qualified teachers.