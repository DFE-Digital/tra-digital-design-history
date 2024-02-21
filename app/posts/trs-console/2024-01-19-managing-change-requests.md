---
title: Managing change requests
date: 2024-01-18
description: Giving users a way to respond to a teacher’s request to change their name or date of birth in the database.
screenshots:
  items:
    - text: List of change requests
      src: 1-mq-change-requests-home.png

    - text: Request for a change of first name
      src: 2-mq-change-request-name.png

    - text: Request for a change of data of birth
      src: 3-mq-change-request-dob.png

    - text: Confirmation screen shown after a user clicks to accept a change
      src: 4-mq-change-request-confirm.png

    - text: Reason selection screen shown after a user clicks to reject a change
      src: 5-mq-change-request-reject-reason.png

    - text: Success screen shows if the change was made and if the user was notified
      src: 6-mq-change-request-success.png
---

When teachers [access their teaching qualifications](/qualifications-service) they can change their:

- name
- date of birth
- email address
- mobile phone number

They might do this because something has changed or they notice a mistake.

To change their name or date of birth they need to send a request with proof to support the change. The proof will be photographs or scans of documents such as a birth certificate or passport.

A member of TRA staff needs to check the request and either approve or reject it.

## What we did

We designed a way for TRA staff to deal with requests in the TRS console. It lets users:

- choose a change request from a list
- view the request including proof
- accept or reject the request

In the Microsoft Dynamics system which is being replaced, change requests appear in a list of ‘open cases’ for users to review. This is a standard term used in Dynamics.

We’ve decided to use the term ‘change requests’ because it’s a clearer description.

### List of change requests

In the initial design, the list of change requests appears on a user’s ‘home’ tab. We may change this as we add more features to the TRS console.

All users see the same list of change requests. There is no way to assign a request to a user.

The list appears as a table. Each change request appears on a row and there are columns for:

- case reference
- name
- case type
- created on

The oldest change request is displayed first. A user can choose a case by clicking on the case reference.

### Request details

The heading on the request page has a caption which includes:

- case type, for example change of name
- name of the person making the request

Using a caption to give context in this way is consistent with a number of related DfE and TRA services such as [access your teaching qualifications](/qualifications-service/qualification-service/) and [refer serious misconduct](https://tra-digital-design-history.herokuapp.com/refer-serious-misconduct-by-a-teacher-in-england/).

The request is shown in a table with columns for:

- what is being changed, for example the first name
- what it currently is
- what the teacher wants to change it to

For name changes we decided to only show the part of the name that’s being changed instead of the full name. This is to help users focus on the data which is changing.

### Proof

The proof section of the request page includes a list of documents which are accepted. This is intended to help TRA staff make sure that the teacher has sent appropriate proof.

We used a [details component](https://design-system.service.gov.uk/components/details/) so that the list of documents is only shown if a user clicks to reveal it. This is because users may already know what proof is accepted. Hiding the list when it is not needed means that a user can focus on the change request and the proof.

The images uploaded by the teacher appear within the main column, which takes up two thirds of the total page width. They are either shrunk or expanded to fill the width of the column.

Teachers are not asked to say what type of documents are in the images. We therefore cannot display this information.

Users can click a link to open an image in a new tab. The image will appear at its original size. This may be larger or smaller than the version shown on the request page.

### Accepting or rejecting a change

At the bottom of the request page there are two buttons. A green button lets the user accept the change while a red button lets them reject it.

If the user clicks to reject the change request, they’re taken to a page where they must choose a reason using radio buttons. The reasons are:

- request and proof don’t match
- wrong type of document
- image quality
- change no longer required

In the initial design there is no way to give more information, for example to say which document was the wrong type.

### After accepting or rejecting a change

After the user accepts a change or gives reasons why they’re rejecting it, they’re taken back to the list of change requests.

The change they’ve just responded to will no longer be on the list. A success message appears at the top of the page, with 3 possible messages:

- the request was accepted and the teacher has been notified
- the request was rejected and the teacher has been notified
- the request was rejected and the teacher has not been notified - this appears if the rejection reason was ‘change no longer required’

If the teacher is notified that their request was rejected, the email includes the reason for rejection.
