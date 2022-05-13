---
  title: Performance analysis in private beta
  date: 2022-05-06
  related:
    items:
    - text: Performance dashboard
      href: https://find-a-lost-trn.education.gov.uk/performance
---

In private beta we will collect data to report on the four mandatory KPIs, as well as additional data that will help us to understand our users and iterate the service.

## 1. Completion rate

Initially, we will monitor the completion rate and the success rate of the Find a lost TRN service by transaction, within the boundary of the digital service. In the future, we plan to monitor it by distinct user and include interactions with the TRA help desk.

In the initial phase we will record:
- number of requests started
- number of TRNs found
- number of help desk tickets created
- number of requests abandoned without finishing, of which:
    - number of requests abandoned at each screen

The completion rate is calculated as:
(number of TRNs found + number of help desk tickets created) / number of requests started

The success rate is calculated as:
number of TRNs found / number of requests started

## 2. User satisfaction

We will measure user satisfaction by counting the ratings (1-5) chosen by users who submit a feedback form.

## 3. Cost per transaction

For the private beta phase, we will measure cost per transaction as:
total cost to provide service / number of completed transactions

where total cost to provide service is the sum of:
- development costs of alpha and private beta phase
- TRA help desk running costs * fraction of overall queries relating to find a lost TRN
- hosting costs

## 4. Digital take-up

We will baseline the number of historic TRN requests that the TRA help desk have received via email and phone as the average number of zendesk tickets created per day with the enquiry type "TRN".

As zendesk has only been in use for a few months, this approach can not fully represent the number of TRN requests throughout the academic year. Due to the time of year, we expect the number of TRN requests shown through this approach to be an underestimate.

Over time, we will compare this number to the number of TRN requests submitted through the digital service to show digital take-up for the service.

## Additional performance metrics

### For successful matches

- time to completion: time elapsed between the start of the transaction and the TRN being sent by email
- attributes which did and did not match the DQT record found
- when we are able to identify distinct users of the service, we will extend this to include number of times (if any) a user changed an answer to a particular question to try to get a match

### For requests which require help desk intervention

- time to completion: time elapsed between zendesk ticket creation and the TRN being sent by email
- time to first contact (if different): time elapsed between zendesk ticket creation and the first email sent
- number of contacts required to resolve
- number of tickets not resulting in a TRN being found (although it may not be possible to determine within this group, how many of these did not have a TRN at all and how many simply chose not to respond to a follow up email)
- number of requests sent to the help desk due to multiple DQT matches
- attributes which did and did not match the DQT record that was ultimately matched by the help desk
- additional attributes requested by help desk via email in order to find a match

## User segmentation

For each successful transaction, we will also capture the following data from matched DQT records, to enable segmentation of the above metrics by user group.

### QTS route

This will tell us how many successful users of the service are, for example, international teachers or do not hold QTS; two user groups who may be less likely to be able to answer some of the questions. It will help us to pinpoint any specific issues affecting these user groups.

### TRN allocation year
This will break down successful use of the service by age of DQT record, and allow us to understand which attributes are more likely to go stale over time.

Although it would be valuable, it will not be possible to perform user segmentation on transactions which are not matched to a DQT record. This means, for example, that we will be unable to determine how the overall completion and success rates differ between these user groups.

## Performance dashboard

[![Performance dashboard](performance-dashboard.png "Performance dashboard for Find a lost TRN")](performance-dashboard.png)
