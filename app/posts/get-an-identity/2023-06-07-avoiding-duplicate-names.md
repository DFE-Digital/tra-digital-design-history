---
  title: Avoiding duplicate names
  date: 2023-06-07
  related:
    sections:
      - title: Links
        items:
          - text: DfE Identity account (password: dia)
            href: https://dfe-identity-account-prototype.herokuapp.com/
---
When newly qualified teachers download their qualified teacher status (QTS) they use the Access your teaching qualifications service by signing in through a DfE Identity account.  

On signing in for the first time to the new qualifications service, we were asking them to create a DfE Identity account – entering their name and date of birth.

This caused an issue because when a person exists in the database of qualified teachers (DQT) we already hold some details about them, like their name and date of birth.

Asking for their name and date of birth in creating a DfE Identity account meant that we then had the name they’d just given, and their name and date of birth as recorded in the DQT.

Playing these back to the user and trying to distinguish them led to a confusing details page – potentially 2 different names and dates of birth.

SCREENSHOT

For names, this could be a mistake but there are other scenarios, such as:

- name changes
- old preferred names
- typos
- names incorrectly split

These will often have been caused because third parties have typed in their names.

Another issue is that if the user needed to change their details as stored in DQT they must go through the process of supplying evidence for the changes. Changes to their DfE Identity account details could be made instantly – again, a confusing flow.

For the second iteration, we decided not to ask for name or date of birth to avoid this confusion. Instead, we play back the details held in the DQT and ask users to confirm they are correct.

 If they’re not, users can change them – we’ll update DQT and the account but may need evidence for the change. It’s a timely opportunity for the user to give us their correct name.

The main problem we identified with this was how the DQT records names. If there’s a space in a person’s first name, it attributes anything after the space as a middle name.

So, if somebody has the first name Sarah Jane – Jane is recorded as a middle name. To counter this in the DfE Identity account we introduced individual fields for first, middle and last names to help users spot if their name has been incorrectly split and to correct it.

SCREENSHOT

Presently, every change to a name must go through the process of providing evidence. We hope to change the policy around this to enable users to correct simple mistakes without providing evidence.
