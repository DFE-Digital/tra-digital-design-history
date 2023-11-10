---
title: Removing the tag showing that someone has teaching restrictions
date: 2023-11-10
screenshots:
  items:
    - text: Search results without the restrictions tag
      src: search-results.png
    - text: Teacher record without the restrictions tag
      src: record.png
---

In earlier designs every search result and record had a tag. It said ‘restrictions’ if the teacher:

- failed their induction or probation
- was found guilty of serious misconduct
- was sanctioned by the General Teaching Council for England (GTCE)
- was on the children’s barred list

Otherwise the tag said ‘no restrictions’.

We already [removed the no restrictions tag](https://tra-digital-design-history.herokuapp.com/check-the-record-of-a-teacher/removing-the-tag-showing-that-someone-has-no-teaching-restrictions/) because:

- someone might not have a restriction but still be prevented from teaching, for example if they have not yet completed their induction
- removing it made the restrictions tag stand out more

Following this we’ve decided to also remove the restrictions tag.

One reason to do this is that the tag could be misleading. For example it would appear when a teacher has been found guilty of serious misconduct but has not been prevented from teaching.

We considered adding another type of tag for this kind of situation. However we found that there were other advantages to removing the restrictions tag from the search results and record pages.

## Search results page

The purpose of the search results page is to help the user identify the record for the teacher they’re interested in.

We know from research that users will always need to click through once they find the right record. We would not expect them to reject a teacher just because there’s a restrictions tag in the search results.

This means that the tag is unnecessary on the search results page and could be a distraction.

Removing the tag also means that we are reducing the amount of sensitive information we show. The search results may include other teachers in addition to the one the user is interested in. There is no need to tell the user that one of these other teachers has a restriction.

## Record page

We highlight restrictions by listing them at the top of the record and using inset text with a red vertical line. It is not necessary to also have a restrictions tag next to the teacher’s name.

As well as removing the tag we made some other changes.

We removed the h2 heading saying ‘restrictions’ and instead now give the restriction type in the h2 heading. This gives more prominence to the restriction type.

We removed the date when a restriction was given. We do not think that the date will affect a user’s decision whether or not to give a job to a teacher.

We also changed the text style of the restriction details from hint text to normal body text. This makes the text darker and more prominent.

## Further considerations

We plan to look at whether users can easily find and understand the information they need to make a decision about a teacher. We may decide to include more content at the top of the record.

We also want to find out whether the new design for restrictions in the record is enough to make sure that users don’t miss this information.

If research shows that we need to emphasise restrictions more, we could consider:

- putting a tag back on the record page but not in the search results
- introducing different tags for different scenarios
- using a different design component to highlight the information instead of the inset text
