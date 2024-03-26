---
  title: GOV.UK One Login user journeys for changing personal details
  date: 2024-03-26
  related:
    sections:
      - title: Related content
        items:
          - text: Access your teaching qualifications prototype (password - qs)
            href: https://qualifications-prototype.herokuapp.com/
  screenshots:
    items:
      - text: "The qualificationslanding page where users can find a link to change personal details"
        src: aytq-quals-page.png
      - text: "A page to change your teaching record details"
        src: change-details.png
      - text: "A confirmation screen before submitting a change request"
        src: change-details-confirmation.png
      - text: "If the change requires evidence, there is a pending review tag until it's approved"
        src: change-details-pending-review.png
---
## Overview

We're using Access your teaching qualifications as the interface to details that a user can change in their teaching record.

The landing page for the service includes the user's qualifications and a details panel in the right hand one-thirds column.

The details panel shows name on certificates, date of birth and TRN. 

There is a link to change your details. It's possible that if users are arriving from a different related service, they will be taken straight to the change your details page and able to return to the service they were accessing.

## Change your details

This page contains personal details than can be changed in a teaching record. The `h1` header is "Change your teaching record details" to make it clear that this will not change details elsewhere.

We list:
- name on certificates
- preferred name
- mobile phone
- date of birth

This is because the TRA services we intend to use GOV.UK One Login and AYTQ for use these details in their services.

### Name on certificates

This is the name displayed if the user downloads a copy of their QTS certificate. It can be different to an official name that GOV.UK One Login uses. By default, it is the same as the name that's used when the account is created. The user is allowed to change it and needs to submit some proof to be reviewed.

This will create a [change request in the TRS console back end](https://tra-digital-design-history.herokuapp.com/trs-console/managing-change-requests/) for support staff to review.

While the request is being reviewed, there is a yellow 'pending review' tag instead of the change link for name on certificates.

### Preferred name

The preferred name is currenty used by the National Profressional Qualifications service. Users can choose a name to be used when contacting them. We want to understand more about how users use preferred names and what they expext to happen if they change it in our service.

We do not require any proof to change a preferred name.

The change is immediate and the user sees a success notification panel in the change details page after submitting.

### Mobile phone

The mobile phone change is the same as for preferred names. No evidence is required. This is used for contact. It may be different from the mobile phone used when signing in to GOV.UK One Login.

### Date of birth

We allow changes to dates of birth because there can be mistakes when creating a TRN. This would usually be if an initial teaching training provider sends a spreadsheet of a cohort for a year but it contains some errors.

We plan to use dates of birth from GOV.UK One Login in future because these will have been identity verified. For now, we've kept the process in for users to change it if there is a mistake.

The process is the same as for name on teaching certificates, they need to submit proof and will see a 'pending review' tag while waiting for the change to be approved.

## GOV.UK One Login details

We've based some content on content provided by GOV.UK One Login to say where users can change other personal details, such as email address, password and how they authenticate.

There is a link to their GOV.UK One Login.

## Prototype

We’ve made [a branch of the Access your teaching qualifications prototype](https://qualifications-prototype.herokuapp.com/landing-pages/v4/start) which includes signing in and changing personal details.

Password: `qs`

## User research

We’re going to use the prototype to test with users.

We’re using the personal details scenario to understand how and why users need to change things, including up to 3 versions of a name, and if it is clear what the changes mean when they are split between GOV.UK One Login and our service.