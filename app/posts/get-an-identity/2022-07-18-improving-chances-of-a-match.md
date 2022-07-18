---
  title: Knowing if someone has a TRN
  date: 2022-07-18
  related:
  sections:
    - title: Related content
      items:
        - text: Trello ticket
          href: https://trello.com/c/eQlJf1kR/543-design-to-determine-whether-users-should-have-a-trn-or-not
---

If we don’t match a user to a DQT record we need to be confident about whether they have a TRN or not.

We need to determine if they should proceed without a DQT match, or be referred to support.

## Users who tell us they have a TRN

Our [no match journey](/get-an-identity/no-match-journey/) is designed to minimise the case where we don’t find a match.

If a user tells us they have a TRN, but their answers do not match, we will:

- present a ‘No match’ page after 'Check your answers'
- give examples of why they might not have matched our records
- playback their answers and give them an opportunity to change them
- let them continue with the answers they’ve given
- create a support ticket in the background so a support agent can manually match the records

A false positive, someone who thinks they have a TRN but does not (for example QTLS users), will get referred to support.

## Users who tell us they do not have a&nbsp;TRN

We will try to identify false negatives – people who tell us they don’t have a TRN, but actually they do.

We know TRNs are confusing and some people don’t know they have one.

If a user tells us they do not have a TRN, we will:

- still ask them their previous name
- ask if they have QTS

We’ll use all information to attempt to match to DQT.

If they told us they do not have a TRN but contradicted this by telling us they have QTS, and further – if there is no match, we will create a support ticket to investigate.

Otherwise, if there is no match, we will not defer to support or show the No match page – they are a user for which we have no record in DQT.

They might be a new user, or a user that is already in Get an identity.

### Users without TRNs that match a record in Get an identity

It's possible that a user who does not match a record in DQT will still match someone who has previously used Get an identity. This can happen if the answers given match an identity record, but they used a different email address.

## Users who get a TRN later

We haven't thought about a user who transitions from a "no TRN" state to a "I have a TRN" one. For example someone who begins teacher training, or an international user who gains QTS.

These users would be in Get an identity and DQT, but the accounts might not be linked together.

## Asking about previous names

As we now always ask about previous names, we've made this design more inclusive and clearer that they do not need to give a previous name if they don’t want to.
