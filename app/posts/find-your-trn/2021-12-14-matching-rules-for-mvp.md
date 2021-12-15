---
  title: Matching rules for MVP
  date: 2021-12-14
---
<style>
.app-prose table {
  margin-top: 0;
}

.app-prose table th:first-child {
  width: 150px;
}
</style>

The Find your TRN service provides the TRN when:

1. service users provide some personal data
2. that data is successfully matched against records in the Database of Qualified Teachers (DQT).

This post documents how success or failure of the match is determined.

## What identifiers are used

Our current designs prompt the TRN holder for the following identifiers, in this order:

* name (current and previous, if applicable)
* date of birth
* National Insurance number (NINO)
* the name of their initial teacher training (ITT) university, school or provider

Our early designs used the DQT email addresses for data matching, but [we moved away from that for now](#).

The service stops asking for more information once 3 matches have occurred against a single record in DQT. There aren’t any mandatory identifiers -- any combination of 3 matching identifiers releases the TRN to the user.

A successful match is defined differently for each identifier.

## Name

Users must provide their given and family names, which are used to match against the names in DQT. Middle names aren’t used for matching. A name match is successful if both given and family names match case-insensitively. Fuzzy matching (e.g. Fred vs Frederick) isn’t supported for MVP.

### Name changes

From our observation of the TRA helpdesk, we learned about TRN holders who have changed their name since their TRN was issued, e.g. as a result of marriage or divorce. For those users, it’s likely that their DQT record doesn’t match their current name.

For this reason, our designs allow users to provide one of their previous given and family names. The user’s previous name is only matched against their current name in DQT, so these cases can lead to a successful name match:

* user-supplied current name matches DQT current name, or
* user-supplied previous name matches DQT current name

If the user provides a previous family name but omits the previous given name, we assume the previous given name matches the current given name. Similarly, we assume the previous family name matches the current family name when omitted.

### Illustrative examples

Assuming the DQT contains:

| First name | Last name |
|--|--|
| Jane | Smith |

Then matching works as follows on user-supplied input:

|First name|Last name|Previous first name|Previous last name|Match?|
|--|--|--|--|--|
|Jane|Smith |||✅|
|Jane|Taylor|||❌|
|Jan |Smith |||❌|
|jane|SMITH |||✅|
|Jane|Smith-Taylor|Jane|Smith|✅|
|Jane|Smith-Taylor||Smith|✅|
|Mary-Jane|Smith|Jane||✅|

## Date of birth

A match is counted when the DQT date of birth exactly matches the user-specified date of birth.

## NINO

A match is counted if there is a NINO on the DQT record and it matches what the user supplied exactly, ignoring case and whitespace differences.

A match isn’t counted whenever:

* there isn’t a NINO on the DQT record
* the user-supplied NINO doesn’t match the NINO on the DQT record
* any time the user says they don’t have a NINO, or they’ve forgotten it

## ITT provider

A match is counted if the DQT ITT provider name exactly matches the user-supplied ITT provider name. Users will be assisted in getting this right with an auto-complete populated with all ITT provider names from DQT.

A match isn’t counted if there isn’t an ITT provider on the DQT record, or it hasn’t been supplied by the user.
