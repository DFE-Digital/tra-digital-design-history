---
  title: "Find your TRN: initial design"
  date: 2021-11-25
  screenshots:
    items:
      - text: "Start page"
      - text: "Do you know if you have a TRN"
      - text: "Do any of the following apply to you"
      - text: "You dont have a TRN"
      - text: "You probably have a TRN"
      - text: "Email address"
      - text: "Check your email to continue"
      - text: "What is your name"
      - text: "What is your date of birth"
      - text: "National Insurance number"
      - text: "Have you ever trained as a teacher in England or Wales"
      - text: "Have you ever trained as a teacher in England or Wales (yes)"
      - text: "Your Teacher Reference Number"
      - text: "We didnt find a match for the details you provided"
      - text: "Thank you for requesting a TRN reminder"
---
## The high-level design

The transaction consists of 4 stages.

### 1. Determining whether the user has a TRN or not

This aims to:

- filter out users without TRNs, so they don’t waste their time.
- inform those without TRNs about why they might want one, and how to get it

### 2. Authenticating the user’s email address

The email address is useful in a number of ways:

- to shorten the user’s journey if there’s an exact match to the email address on the Database of Qualified Teachers (DQT) record
- for auditing, insofar as capturing it prevents the transaction from being completely anonymous
- for emailing the TRN to the requester, if the transaction completes successfully
- for the fall-through to the helpdesk, if the transaction is unsuccessful

### 3. Matching the user’s responses to their DQT record

This step builds confidence that the requester is the TRN holder, while falling short of strict identity verification.

### 4. Displaying the TRN or handing-off to the helpdesk

If the user’s responses can be matched to an existing DQT record with enough confidence, the user’s TRN is shown. Otherwise, they can submit a helpdesk request to try to recover their journey.

[Screen flows PDF](Find_your_TRN_screen_flows.pdf)

[Screen flows in Google Draw](https://docs.google.com/drawings/d/1wMJEgs0q9GKduEQ2KvFTU6ZVu4FFg-bdyEAcebVWNzQ/edit)
