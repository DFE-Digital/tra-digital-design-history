---
  title: Changing personal details after signing in through GOV.UK One Login
  date: 2024-04-03
  related:
    sections:
      - title: Related content
        items:
          - text: Access your teaching qualifications prototype (password - qs)
            href: https://qualifications-prototype.herokuapp.com/
  screenshots:
    items:
      - text: "Teacher record where users can find a link to change their details"
        src: aytq-quals-page.png
      - text: "Change details page"
        src: change-details.png
      - text: "Confirmation screen after requesting to change name on certificates"
        src: change-details-confirmation.png
      - text: "Success message after changing mobile phone number"
        src: aytq-quals-page-success.png
      - text: "‘In review’ tag shown until a change which requires evidence has been approved"
        src: change-details-in-review.png
---

Teachers can currently use the DfE Identity service to change some of the personal details on their teaching record.

We intend to [replace DfE Identity with GOV.UK One Login](/qualifications-service/using-govuk-one-login-with-tra-online-services). Once we do this, we’ll need to give users another way to change their personal details.

## How a user currently changes their personal details

A user can change their personal details from either:

- Access your teaching qualifications (AYTQ)
- Register for a National Professional Qualification

To do this the user clicks a link which takes them to DfE Identity. In AYTQ the wording of this link is “View and update details”.

The user is first taken to an [interruption page](https://github.com/alphagov/govuk-design-system-backlog/issues/27). It tells them that they’re going to the DfE Identity service.

After they click to continue the user is taken to a page with the heading “Confirm your details”. The page lists teaching record details which are:

- first names
- middle names
- last names
- date of birth

It also lists account details which are:

- preferred name
- email
- mobile phone

There’s a change link for each detail which can be changed.

Usually each detail can be changed except for the date of birth. It can only be changed if the date of birth which the user entered during DfE Identity registration is different to the one in their teaching record.

This would usually only happen if an initial teaching training provider sends the wrong date of birth for a trainee.

Each change link takes the user into a journey in which they either make or request the change.

The user is shown:

- a confirmation screen after requesting a change to teaching record details
- a success notification on the teacher record page after making a change to account details

## What we changed

The h1 heading is now “Change your details”. This is more appropriate than “confirm” as the user does not need to confirm that the details are correct.

We’ve split the details into 3 sections, which are:

- teaching record personal details
- GOV.UK One Login personal details
- GOV.UK One Login security details

Some details have change links. These lead to the same journeys as in the current service.

### Teaching record personal details

The teaching record personal details include:

- name on certificates
- preferred name
- mobile phone
- date of birth

These are details which are used by TRA services in addition to the details kept by GOV.UK One Login.

#### Name on certificates

The main use of AYTQ is for users to download their teaching certificates, for example to show that they have qualified teacher status.

We’ll store the name to be used on certificates separately from the GOV.UK One Login name. In most cases it should be the same, but some people use one name professionally and have another on their identity documents.

The user is allowed to change the name on their certificates. After clicking the change link they’re asked to submit proof of the change.

Once they submit proof, the user is taken to a confirmation screen.

This also creates a [change request in the TRS console](https://tra-digital-design-history.herokuapp.com/trs-console/managing-change-requests/) for support staff to review.

While the request is being reviewed a yellow 'pending review' tag replaces the change link.

#### Preferred name

The preferred name is currently used only by the Register for a National Professional Qualification service.

Users can choose a name to be used when contacting them. We do not require any proof to change a preferred name and the change is immediate.

The user is taken back to the teacher record and shown a success message.

#### Mobile phone

We keep a mobile phone number in case we need to contact users.

It may be different from the number which is used when signing in to GOV.UK One Login. Our services do not have access to that number.

No evidence is required to change the mobile phone number and the change is immediate.

The user is taken back to the teacher record and shown a success message.

#### Date of birth

This is the date of birth on the user’s teaching record.

There’s also a GOV.UK One Login date of birth which may be different. If so then a change link is shown for the date of birth on the teaching record.

The process for changing the date of birth is the same as for the name on teaching certificates. The user needs to submit proof and is then taken to a confirmation screen.

A change request is created in the TRS console for support staff to review.

A ‘pending review’ tag is displayed on the change details page until the change has been approved or rejected.

### GOV.UK One Login personal details

The GOV.UK One Login personal details are:

- name
- date of birth

We decided to show these separately from the teaching record personal details because:

- they may be different
- they cannot be changed within our service

These details are usually updated automatically, for example if a user changes the name on their bank accounts. The change will be picked up by the credit reference agency Experian and then made in GOV.UK One Login.

If the user wants to update these details then they must contact the GOV.UK One Login support team. We give a link for them to do this.

### GOV.UK One Login security details

The GOV.UK One Login security details are:

- email address
- password
- how the user gets security codes to sign in - by text message or authenticator app

We link to GOV.UK One Login, where the user can change these details. They appear in a tab called ‘security’ but the email address and password are also referred to as ‘sign in details’.

## User research

We created this user journey in a prototype to test with users.

We wanted to test the change of personal details help us understand:

- why users need to change things
- whether it’s confusing to have 3 names and 2 dates of birth in the details
- how users make use of preferred names and what they expect to happen if they change them
- if it’s clear how to change things, since there are 3 ways depending on the type of detail being changed

## Further considerations

We expect to make changes after analysing the results of research. We already know that some things may need to be considered further or may change as GOV.UK One Login is developed.

### Preferred names

The GOV.UK One Login team is planning to do research about whether they should handle preferred names in their service. If they do so then we may want to remove preferred names from our service.

### Improving the ‘your details’ section of a teacher’s record

A teacher’s record in AYTQ has some details in the one-third page width column. It shows:

- name on certificates
- date of birth
- TRN

There’s a link to the change page. In the live service it says “View and update details” but in the prototype we’ve changed it to “View and change details”. This matches the new h1 heading of the change page.

The details shown are only some of those which can be changed. The TRN cannot be changed. We should look at whether:

- other details should be shown
- it should be made clearer that other details can be changed if a user clicked the link

### Date of birth

We may decide in future to only use the GOV.UK One Login date of birth.

It should almost always be the same as the date in the teaching record. But if it is not then the GOV.UK One Login date should be more reliable since it will have been verified.

### Name of the service

We may want to [reconsider the name of the service again](https://tra-digital-design-history.herokuapp.com/qualifications-service/renaming-of-service/).

It already does more than just allowing a user to access their qualifications. In future it may also include details of a user’s employment history, so it may be better to refer to the teacher’s record in the service name.

### Mobile number

We’ll store a mobile number which users can change themselves. We may be able to get this from GOV.UK One Login in future, but only if the teacher used a mobile phone to authenticate their sign in.
