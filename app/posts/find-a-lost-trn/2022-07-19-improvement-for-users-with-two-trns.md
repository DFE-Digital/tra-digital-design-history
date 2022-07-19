---
  title: Better matching for users with two TRNs
  date: 2022-07-19
---

The TRA allocates around 40,000 TRNs each year, mostly to people who are pursuing teaching qualifiations. 

TRNs are also used as part of the Teachers Pension Service (TPS). TPS allocates a TRN to any new pension holder who doesn't already have one, currently around 30,000 people a year. 

This process can sometimes go wrong, and someone can be given a TRN by both the TRA and TPS. In this case, their qualifications and misconduct record will be associated with one TRN, but their pension will be associated with another.

This happens because when either the TRA or TPS (depending on the order the TRNs were minted) tries to check if someone already has a TRN, they don't find their existing record or don't have enough information to be sure it's the same person, so they create a new TRN. 

Creating an additional TRN is the safest option in cases where you can't be sure of a match - accidentally giving the same TRN to two different people causes problems that are much harder to resolve.

## Helpdesk resolution

When it is identified that someone has two TRNs, either by TRA, TPS, or the individual themself, the TRN associated with their qualifications is kept active and the other TRN is made inactive. This is updated in both the DQT and TPS's database, and the TRN holder is notified.

## What happens in Find a Lost TRN now?

Records created by TPS always have National Insurance Number populated. An increasing number of records created by the TRA don't. 

Find a Lost TRN requires three matching values to confirm a TRN match, and the first combination we try is Name, DOB and NI Number. When someone has two TRNs, we are therefore likely to find their TPS TRN, but not their TRA TRN. 

This is a problem for users because a) the TRN we give them doesn't have any qualifications associated to it, which is typically why someone needs their TRN, and b) we aren't identifying that they have 2 TRNs, telling them about it, or fixing it.

We identified this issue because we saw that 4 of the TRNs find has found over the last 3 months have since been made inactive.


## An improvement for these users

Given that people with two TRNs often only have two because one of the records contains typos or other inaccurate data, it would be very difficult to build a service which can always identify that someone has two TRNs.

However, we can identify the majority of these cases with a simple follow up question. When we get a match to a TRN which doesn't have a QTS date (either by Name + DOB + NINO, or by Email + two other attributes when email matching is enabled), we can follow up with the question "Do you have QTS?". 

If the user says no, we have found the right TRN and can end the flowe there.

If they say yes, there is likely a duplicate TRN somewhere, and we can continue to ask questions in order to find it, then route the case to the helpdesk to resolve the duplicate.
