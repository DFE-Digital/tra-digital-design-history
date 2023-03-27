---
  title: DQT data in DfE identity account
  date: 2023-03-27
  related:
    sections:
      - title: Prototype of scenarios
        items:
          - text: Replica journey in prototype (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com
---

Part of replacing the teacher self-service portal (TSSP) was moving the qualifications into the new Access your teaching qualifications (AyTq) service. The second part was deciding where with the editable database of qualified teachers (DQT) data points held in TSSP should live. 

The DQT editable data points held in the TSSP are:
- Email 
- Contact number
- Name 
- Date of birth
- National insurance 

We decided that the DfE identity account (DIA) should be the location for all user data, including DQT data.

![When we've found a match in the DQT](1-name.png "When we've found a match in the DQT")


## DQT data in the DfE identity account

### Email and Contact number
When creating an ID account, we ask users to enter and verify their email address and mobile number. These fields will overwrite any existing DQT email and contact numbers. All communications from services integrated with DIA  will use the email address & mobile held in the DIA when in communication with the user.

### National insurance (NI)
Providers do not routinely provide NI data in the DQT so we decided to leave this data point out of the DIA. This may change if providers begin to provide the users’ national insurance again.

### Date of birth (DOB)
#### Scenario 1
To reduce confusion, DQT date of birth will be hidden if it matches the DOB entered by the user when they created their DIA. Because this DOB has been verified by DQT and by the user when creating their account. This field will not be editable. 

{% from "vimeo/macro.njk" import appVimeo with context %}
{{ appVimeo('811947180') }}


#### Scenario 2
If the DQT and DIA date of birth are different, we display both to the user. A message will be displayed instructing them to amend the DOB that is incorrect.

{{ appVimeo('811946928') }}

#### Scenario 2A
If the user amends their DIA DOB to match DQT, then only the DIA DOB will be displayed. See scenario 1

#### Scenario 2B
If a user amends their DQT to match their ID DOB, they will need to submit evidence for this change. On submission, a pending change lozenge is displayed in both the DIA & DQT DOB rows that states ‘Pending review’. The change links are hidden until this request is processed. The user will receive an email if this change has been successful or not.
Possible outcomes of scenario 2B:

- If DQT DOB change is successful and matches DIA then only the ID DOB is displayed. (see scenario 1)
- If DQT DOB change is successful and does not match DIA then scenario 2 occurs. 
- If DQT DOB change is unsuccessful (e.g wrong evidence submitted) then scenario 2 occurs

#### Scenario 3
If a DIA has been created that did not include a DQT check, then only the DIA DOB will be shown to the user. The DOB change link functionality remains editable until the account has been matched against a DQT record. Scenarios 1 or 2 will occur if or when a user’s account is matched against a DQT record.

{{ appVimeo('811947131') }}


### Name
Both the DIA and DQT name are displayed back to the user on the DIA ‘my account’ page. The title, Official name, is used to describe the DQT instance. A text hint informs that official name is displayed on their teaching certificates. To make changes to this name requires evidence to be submitted and a TRA review to take place. This can take up 5 days. During this review period, a ‘pending review’ lozenge is displayed and the change link is removed. The user will receive an email if the change has been successful or not.

The DIA instance is called ‘Name’ and is editable and does not require verification.

{{ appVimeo('811947148') }}


### TRN
A user’s TRN is displayed for accounts that have been matched against a DQT record. This field is non-editable.
