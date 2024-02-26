---
  title: Testing showing what users searched for on the no results page
  date: 2024-02-26
  screenshots:
    items:
      - text: A search results page with no results, including the last name and date of birth the user searched for.
        src: no-results.png

---

A third theme that we identified in feedback from private beta round one was users looking for no results. The other two themes were [timestamps](/testing-timestamps-to-show-when-a-check-was-done) and [summary information](testing-summary-tags-to-show-the-status-of-a-teacher).

In Employer Access, users would download a list of all the teachers with restrictions or sanctions and screenshot the point where their applicant's name would be, as evidence they're not on it. Some users, such as providers of initial teacher training, would check the database to make sure that someone who was applying for a new traning course hadn't previously been a teacher and been sanctioned.

We do not want users to access full lists of teachers because it is an inefficient way to do the check and it unneccessarily reveals data about lots of people each time it's done. We wanted to understand how and why users look for no results, and how we could better meet that need.

On [Check the children's barred list](https://tra-digital-design-history.herokuapp.com/check-the-childrens-barred-list/making-search-results-clearer), we show what users search for on the results page. This makes it clear what the possible match, or no match result relates to and can be used for record keeping. It also helps the user to see if an unexpected result was due to a mistake, such as misspelling a name.

## User research

Discovery research found that all the agencies we spoke with were checking that applicants for non-teacher roles such as teaching asisstants were not on prohibtied lists. For audit purposes, they wanted proof that they had checked and not found the person.

In alpha research, some users highlighted there was no longer a 'print this page' button. They told us that without this they would either screenshot, print via the browser, or right click and save. They would use this for their record keeping, to add to a single central record, and show to governing bodies when they get inspected.

In private beta research, we explored this further with teacher supply agencies. All told us that they keep digital copies as evidence of searches for audits by the Recruitment and Employment Confederation, who maintain agency standards ina  similar way to Ofsted with schools. They would screenshot either:

- the TRN section
- the status box in Employer Access
- a list showing that someone's name is not on it

When we showed them the search results page, they told us they also search non teaching staff and it would be helpful to see the name they search on the no 'results' page to prove the check had been done and screenshot for record keeping.

> "it would be helpful to see who you searched for if you don't get a result. Then you could screenshot and send it to the school."

A recomendation from this research was to test including the search terms.

## Design

We decided that the simplest way was to include the search terms as part of the body content. This avoids introducing additional components that could confuse the design or detract from their usability in other contexts. 

For example, [inset text](https://design-system.service.gov.uk/components/inset-text) should only be used sparingly so it is noticed more and we already use this to [highlight restrictions on a record](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/removing-the-tag-showing-that-someone-has-teaching-restrictions). [Summary lists](https://design-system.service.gov.uk/components/summary-list/) are more commonly used to replay answers at the end of a form that can be changed, or grouped together in a card.

We decided against using [bold](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#bold) to emphasise the terms because it should be used sparingly and to highlight elements that are telling the user what to to, such as **start**.

We decided to capitalise the last name even if the user typed all lowercase. This is so it matches how it appears on the record and the user is not prompted to change this if they get an enexpected result. The result will be the same if they enter capitals or lower case.

We format the date input to display in the [GOV.UK date standard](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#dates).

In the prototype, we do this for no results pages using:

`No result found for`
```javascript
    data.lastName [0].toUpperCase() + data.lastName.slice(1) 
```
`born on`
```javascript
    data | isoDateFromDateInput("date") | govukDate
```

We do not do this when there are positive search results. This is because if users find a match, the evidence they need to capture is on the record page for the person.

## Testing

We believe this a low risk iteration because:

- the user need has been consistently identified
- it is common for search result pages to include the search terms
- we do this on the related service to [Check the children's barred list](https://tra-digital-design-history.herokuapp.com/check-the-childrens-barred-list/making-search-results-clearer/)

Therefore, we didn't want to explicitly draw attention to this in private beta round two testing, as we were also testing summary information and timestamps.

However, we wanted to make sure:

- users notice and understand the terms are included, without being highlighted in some way
- the screen will meet audit requirements for governing bodies

## Considerations

The decision to include the terms in the body content is different to Check the children's barred list, which uses a summary list component. If we find that this design is suitable, we may want to update the other service for consistency. 
