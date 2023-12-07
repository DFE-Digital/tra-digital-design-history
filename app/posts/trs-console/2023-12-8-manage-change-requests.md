---
title: Manage change requests
date: 2023-12-8
description: Managing requests from teacher's to change their personal information
screenshots:
  items:
    - text: The homepage has a chronological list of requests as individual cases
      src: 1-mq-change-requests-home.png

    - text: A change of name requests shows the data that will be changed and evidence the user had uploaded
      src: 2-mq-change-request-name.png

    - text: A change of data of birth shows the data that will be changed and the evidence needed
      src: 3-mq-change-requests-dob.png

    - text: A confirm screen shows how the data will change
      src: 4-mq-change-request-confirm.png

    - text: If they reject the request the user selects a reason
      src: 5-mq-change-request-reject-reason.png

    - text: A success screen shows if the change was made and whether the user was notified
      src: 6-mq-change-request-success.png
--- 

DfE users need to verify requests and make changes to personally identifiable information, such as names and dates of birth, so that they keep teachers’ records updated. Requests may come from teachers who contact DfE because something has changed, or they notice a mistake on their record.

## Change requests

In the old DQT, DfE users get a list of change requests in Dynamics which are generated as “open cases” for them to review. We’ve changed this terminology to ‘change requests’ because it is more descriptive and not associated to a particular technology.

The landing screen features a case reference which links to the request and the name, request type, and date it was requested.

This allows them to see the order they need to complete the tasks and what they are for.

## Home page

The request screen features a heading with caption, which is consistent with other related Teaching Regulation Agency (TRA) designs such as [access your teaching qualifications] (https://tra-digital-design-history.herokuapp.com/qualifications-service/qualification-service/), [refer serious misconduct] (https://tra-digital-design-history.herokuapp.com/refer-serious-misconduct-by-a-teacher-in-england/), [manage teacher misconduct referrals] (https://tra-digital-design-history.herokuapp.com/manage-teacher-misconduct-referrals/), and [register trainee teachers] (https://becoming-a-teacher.design-history.education.gov.uk/register-trainee-teachers/). This gives context of the record being worked on and the type of request.

We use a table with current and new columns to show the requested change. We decided to only show the part of the name that’s being changed, such as the first name, instead of the full name. This is to focus on the data that’s changing.

## Proof

We used a [details component] (https://design-system.service.gov.uk/components/details/) to contain a list of documents that are accepted for the change request type. This is because users are frequent professional users and will usually not need to see this, but it can be helpful to check as a remainder. As the content is hidden when it isn’t needed, there is more focus on the change and the proof.

We included images that the teacher has uploaded as evidence for their change request. These keep the two-thirds layout, as they can be from large portrait documents, such as a certificate.

We decided to rename the “view larger” link to “open in new tab”, as sometimes the original image would not be larger than it appears on this page.

The user has a confirmative accept change button, and a destructive reject change button to progress.

## Rejecting

If the change request is rejected, the person who asked for it will be notified with the reason.