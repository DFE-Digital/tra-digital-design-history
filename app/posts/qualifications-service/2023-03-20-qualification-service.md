---
  title: Access your teaching qualifications
  date: 2023-03-20
---
## Overview

During the user testing of the redesigned [‘Teacher self-service portal (TSSP)](/qualifications-service/redesign/)’ several things became clear.

- Very few teachers had heard of the service 
- Those who had, accessed the service to download their qualification certificates 
- Others accessed it only to amend the name on their certificates 

Based on the primary need for users to access their qualifications, we chose to call the service Access your teaching qualifications (AyTQ).

This service will replace the TSSP as the single location for teachers to access their teaching qualifications. 

TSSP user details, such as name (displayed on certificates) and date of birth, will move into the [DfE Identity account (DIA)](/get-an-identity).

### Walkthrough of qualification service 

Demo shows service being accessed by the DfE Identity account (basic auth account creation plus a DQT lookup).

{% from "vimeo/macro.njk" import appVimeo with context %}

{{ appVimeo('809838131') }}


### Qualifications

The following qualifications will available to view within AyTQ 

- National professional qualifications (NPQs)
- Early years teacher status (EYTS)
- Induction + history 
- Mandatory qualification (MQ): specialist teacher
- Qualified teacher status (QTS)
- Initial teacher training (ITT)

We present the qualifications using the summary card component. This visually separates each qualification type, making it easier to locate the qualification by name. Users can download their certificates using the links in the relevant qualification cards.

![Overview of the qualifications service](1-overview.png "Overview of the qualifications service")

We chose to display the qualifications by the date they were attained. We hypothesized that a user would be coming to download their most recently attained qualification.

A teacher's induction qualification can include a history of a their induction experience (fields include: appropriate body, number of terms and dates). We chose to present the history within a details component inside the induction component. We don't believe this warrants being exposed to the user, as the primary of mosts users is downloading their certificates. 

![Induction history](2-induction.png "Induction history")


The TSSP shows all fields for every qualification, even if there’s no data to show. We’ve refined this so only relevant data shows in AyTQ - if there’s nothing to show, we hide it. We significantly reduced the amount of content on the qualifications page so the user only reads what they need. 


### Amending user data
Users visit the TSSP to amend their details such as their name (used on their certificate), date of birth, email and contact number. These data points are stored on the database of qualified teachers (DQT), which were added by third party providers (ITT) when the user first became a teacher or attained QTS.

We decided to move the editing of DQT data out of AyTQ and into it’s ID solution, the DfE identity account (DIA). Now, both DQT data and ID data are accessible from a single service.

DQT email and contact number will be updated to use DIA’s email and mobile. 


### DfE Identity account & Access your teaching qualifications.

When a user downloads a certificate, it will display the name held on DQT. If it’s incorrect or has changed (due to surname change), they will need to update it within the DfE Identity account. The ‘your details’ component displays their DQT name and includes a link to correct errors.

![Details component showing DQT name & TRN](3-details.png "Details component showing DQT name & TRN")



The DfE Identity account (DIA) is accessible via the ‘your details’ component or the page header’s account link. We display an interstitial page informing the user that they’ll be leaving AyTQ and accessing the DIA to change to their details

![DfE identity acccount interstitial](4-account-intersitial.png "DfE identity acccount interstitial")


![DfE identity acccount DQT data](5-Account.png "DfE identity acccount DQT data")
