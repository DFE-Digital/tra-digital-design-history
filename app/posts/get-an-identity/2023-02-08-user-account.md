---
  title: TSA - User account details
  date: 2023-02-08
  related:
    sections:
      - title: User account details 
        items:
          - text: Replica journey in prototype (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com/account/account-details
          - text: Lucid board showing flow
            href: https://lucid.app/lucidspark/b88634d8-2452-4ed6-9c7c-010383770731/edit?view_items=KZDsx9Mr-.mh&invitationId=inv_9a36d007-204a-41ed-b8c3-1f49d5e63a05
---


We are testing alternative names for Get an Identity (GAI) now that it will be called out to users. The name we’re using in the prototype to describe GAI is, Teacher services Account (TSA).

When somebody creates a TSA, they can sign in and access their respective services, for example, Apply for QTS in England. 

We capture the data during account creation and hold it centrally in the TSA. These data points include name, date of birth, email and mobile number.

## What users would see

A video walkthrough of the user account details

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('797146588') }}


## Accessing a user’s account details 

A user can only edit their details once they ‘ve signed in to their service via the TSA. They can access their details via an account CTA located below the Apply for a QTS service header.  

![Account functionality built into QTS](2-apply-for-qts.png "Account functionality built into QTS")

## Account Interstitial page

When a user follows the ‘Account’ link in the header of the Apply for QTS service, we show an interstitial page. This tells them what the account is and that they are using a different service to edit their details.
The page also tells them what details they can change. This interstitial pattern was used by the Apprenticeships service when they integrated with GOV One.

![TSA account interstitial](3-account-interstitial.png "TSA account interstitial")


### Account details page 

Users can change their TSA name, date of birth, mobile number and email address from this page. The process of changing their mobile and email address is the same as account creation, with OTP required for validation.

There’s a back link which tells the user they can go ‘Back to Apply for QTS in England’.

![TSA user details](1-tsa-details.png "TSA user details")



### Sharing user data with consuming services 

We can share the data points we collect in TSA with the consuming services we are integrating with. We can pre-populate the consuming service’s personal details (name and date of birth) section, so the user does not have to enter them each time they use a teacher service. This data is available to consuming services but is read-only.

If their personal details have changed or are wrong, they can correct them in the TSA. By capturing name and date of birth centrally in TSA we’re reducing the chances of different services capturing different details

![Sharing user data with consuming services](4-sharing-data.png "Sharing user data with consuming services")