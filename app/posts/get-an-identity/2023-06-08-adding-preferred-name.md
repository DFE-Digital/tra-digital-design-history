---
  title: Collecting a preferred name in addition to official name 
  date: 2023-06-08
  related:
    sections:
      - title: Links
        items:
          - text: Avoiding duplicate names
            href: /get-an-identity/avoiding-duplicate-names/
---

With our recent work on names, we’ve tried to reduce duplication of name and date of birth. Teaching ID will hold first, middle, and last names. If the teaching ID account is linked to DQT (Database of Qualified Teachers), we’ll defer to those names, so we’ll just have one set of names. The DQT names require documentation to change – as we need to make sure teaching certificates are issued in the correct name. For now, we’re calling that the ‘official name’.

In addition to the official name, we’re also going to add what we call ‘preferred name’. This will be a name that users can provide to tell us how they’d preferred to be called. Unlike the official name, they will not need to give any documentation for it – they can provide whatever they like.

We think this will be helpful where:

* the full official name is longer or is not how the user usually refers to themselves
* the user prefers a shortened form of their first name (Jess for Jessica, etc)
* services that do not need a full official name can defer to what the teacher has selected

For many users we anticipate their preferred name will be the same as the official name we hold. Our page asking about preferred name can help support this by including it as one of the suggestions. It will be a single field rather than separate fields. We’ll let users enter what they like but hope most will provide a full name. We’ll encourage this through hint text and the other suggested options being combinations of their full name.

Our new preferred name page:

![Form collecting a user’s preferred name.](1-Preferred-name.png)

If we do not hold a middle name for users, then there’ll be just one suggested preferred name – the concatenation of their first and last names.

If we hold a middle name for the user, we’ll also suggest that concatenated with their other names.

If the teacher does not like the suggested preferred names, they can choose ‘other’ and type a different name.

![Users can enter their own preferred name.](2-Other-preferred-name.png)

## Confirming teaching ID details

We’ve updated the teaching ID confirm page with preferred name. We’ve now split the details between ‘teaching record’ - those details stored on DQT and required to be validated with documentation – and ‘account details’ - those that relate to the teaching ID account.

![Users are shown the preferred name on the confirmation page.](3-Confirm-your-details.png)

## When users update their official name

We want to try to keep the preferred name in sync with official names. If users update their official name, we will prompt to see if they’d like to also update their preferred name. The prompt will give options that include the existing preferred name or other options that concatenate the new official name they’ve provided.

![After changing their official name, users are asked if they want to update their preferred name.](4-Update-preferred-name.png)

