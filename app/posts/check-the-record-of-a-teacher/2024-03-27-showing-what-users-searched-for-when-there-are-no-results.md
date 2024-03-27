---
  title: Showing what users searched for when there are no results
  date: 2024-03-27
  screenshots:
    items:
      - text: Search results page with no results, showing the last name and date of birth the user searched for
        src: no-results.png

---

After the initial private beta release we chose 3 themes to explore based on user feedback and analytics. The themes are:

- [providing a summary of a teacher’s status](/check-the-record-of-a-teacher/using-tags-to-summarise-a-teachers-status)
- [showing when a search was made](/check-the-record-of-a-teacher/showing-when-a-search-was-made)
- giving more useful information when there are no search results

We chose the last of these because we found that users sometimes expect to have no results.

## What users do when there are no results in Employer Access

Users of Employer Access can search for a teacher by last name and teacher reference number (TRN).

They can also check lists of people with restrictions. This includes people who have been:

- sanctioned by the General Teaching Council for England
- prohibited from teaching by the TRA
- sanctioned in EEA member states
- prevented from managing a school or being a governor - this is often known as the section 128 list

The intention is that users should check the lists if they cannot find a teacher’s record by searching. They can either view the lists online or download them.

The lists do not contain any information which is not available in a teacher’s record. If a teacher is on one of the lists then the restriction will also appear on their record.

However the record can contain more information than is available in the lists.

For example, the record will show if a teacher has a possible match on the children’s barred list. There is no list in Employer Access for this but some users can separately search the children’s barred list.

## Our design for the initial public beta release

The new service does not include lists of people with restrictions.

Instead we’ve made it easier for users to find teachers using the search function. They do not need a TRN, just the teacher’s last name and date of birth.

We do not want users to access lists of people with restrictions because:

- it’s inefficient - we know that some users check the lists in Employer Access even though they’ve already found a teacher’s record
- it means that all users can see details of everyone who has a restriction, even though they only need information about people they plan to employ

## Users’ feedback about what we show when there are no results

When we spoke to users we found that many of them use Employer Access even when they do not expect to get any results. For example they sometimes search for:

- non-teaching staff such as teaching assistants
- candidates for teacher training

These people will not usually be in the database of qualified teachers. They will therefore not appear in either Employer Access or the new service.

Users told us that they want to see what they searched for on the results page in the new service. This would allow them to keep evidence that they’d done the search.

> “It would be helpful to see who you searched for if you don't get a result. Then you could screenshot and send it to the school.”

## Our design for the results page when there are no results

We decided to show the last name and date of birth which a user searched for when they get no results.

### Using body text to show what the user searched for

The simplest way to show what a user searched for is to include the search terms as body text. This avoids introducing additional components that could confuse the design.

For example, we considered [inset text](https://design-system.service.gov.uk/components/inset-text) but it should only be used sparingly so that it stands out. We already use it to [highlight restrictions on a record](/check-the-record-of-a-teacher/removing-the-tag-showing-that-someone-has-teaching-restrictions).

We also considered adding a [summary list](https://design-system.service.gov.uk/components/summary-list/) showing the last name and date of birth. This is the approach which we took on the new service for checking the children’s barred list.

However, a summary list is more commonly used to replay answers at the end of a form. Often the answers can be changed or are grouped together in a card. We decided that the summary list was not any better than body text in this case.

### How the name and date of birth are presented

We decided against using bold for the name and date of birth. The [entry about bold in the style guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#bold) says not to use it for emphasis.

We decided to use an initial capital letter the last name, even if the user typed all lowercase or all uppercase when they searched.

We did this so that the name matches how it would appear on a record if there was one. We did not want a user to think that they might get a different result if they tried again with correct capitalisation.

The date of birth is displayed as described in the [entry about dates in the style guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#dates).

## Testing the new design

We believe that this is a straightforward change because:

- the user need has been consistently identified
- it’s common for search result pages to include the search terms
- we [show search results on Check the children's barred list](https://check-the-childrens-barred-list/making-search-results-clearer/)

We decided not to explicitly draw attention to this change in testing, since we were also testing [summary tags](/check-the-record-of-a-teacher/using-tags-to-summarise-a-teachers-status) and [time stamps](/check-the-record-of-a-teacher/showing-when-a-search-was-made).

However, we wanted to include the new feature in the prototype to see whether users noticed it. If they did we wanted to ask them about whether they:

- found the content clear
- thought that it would meet their needs as evidence of a search

## Further considerations

If we find that this new design works well, we may want to use it in Check the children’s barred list.
