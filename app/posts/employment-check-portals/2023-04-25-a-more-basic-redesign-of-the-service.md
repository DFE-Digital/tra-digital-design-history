---
title: A more basic redesign of the service
date: 2023-04-25
---

We recently [redesigned the service](/check-the-record-of-a-teacher/first-redesign-of-the-service/).

But we’ve not been able to arrange research. And without research we're not confident to start development.

So in the meantime, we've designed a more basic version that works similarly to the existing service.

This allows us to start development while we run research.

## How it works

### Finding a teacher by teacher reference number (TRN)

When the user signs in, they'll see a search form.

![Search form](search.png)

If the TRN is valid it will take the user to the record.

![Record](record.png)

If the TRN is invalid it will take the user to a page saying the record was not found.

![Not found](notfound.png)

### Viewing teachers in your organisation

Teachers that have been added to the user's organisation are shown below the search form.

![Teachers in your organisation](your-teachers.png)

If the user clicks on a teacher, it’ll take the user to the record.

### Viewing teachers on restricted lists

4 restricted lists of teachers are shown at the bottom.

![List](list.png)

If the user clicks one of the restricted lists, they'll be taken to a page showing a list of teachers with that restriction. For example, if a teacher has failed their probation or induction.

![Teachers who have failed their probation or induction](list-induction.png)

We removed the 'Teachers sanctioned in other EEA member states' list because it's no longer needed.

We also renamed the lists to make them clearer.


