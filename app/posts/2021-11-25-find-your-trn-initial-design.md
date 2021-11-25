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

## When the TRN is shown to the user

In this design, the TRN is shown to the user if:

* the user’s verified email address matches one of the email addresses on a unique DQT record
* or if any 3 of the following attributes match:
  * exact match of first name and last name (these count as one match)
  * date of birth
  * National Insurance number
  * exact name match of the ITT provider on the DQT record

This design uses fewer attributes than the existing phone and email processes, in order to initially reduce scope and complexity.

[Process flow for the existing phone/email TRN reminder process](https://lucid.app/lucidchart/86d3de20-922a-4991-afae-d3cbbf63596c/edit?invitationId=inv_e740f043-2309-46d6-b8fe-c502c1f4c460&page=HhyoMBX25KE_#)
