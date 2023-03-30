---
  title: Sharing data with consuming services
  date: 2023-03-30
  related:
    sections:
      - title: Links
        items:
          - text: QTS journey (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com/qts/personal-information/name-and-dob
          - text: Access your teaching qualifications (password, qs)
            href: https://qualifications-prototype.herokuapp.com/user-research/mvp/
---
### Sharing user data with consuming services

We can share the data points we collect in DfE Identity account (DIA) with the consuming services we’re integrating with. We can pre-populate the consuming service’s personal details (name and date of birth) section, so the user does not have to enter them each time they use a teacher service. This data is available to consuming services but is read-only.

If their personal details have changed or are wrong, they can correct them in the DIA. By capturing name and date of birth centrally in DIA we’re reducing the chances of different services capturing different details


### Apply for QTS in England journey
{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('813138406') }}



### Access your teaching qualifications
We display the name held in DQT - this can be changed by accessing the DfE Identity account. This data is displayed as read-only.

![Showing DQT data (e.g official name) in the Access your teaching qualifications](quals.png "Showing DQT data (e.g official name)  in the Access your teaching qualifications")
