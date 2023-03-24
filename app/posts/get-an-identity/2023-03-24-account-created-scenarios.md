---
  title: DfE Identity account scenarios for Access your teaching qualifications (AyTQ)
  date: 2023-03-24
  related:
    sections:
      - title: DfE Identity account prototype
        items:
          - text: Replica journey in prototype (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com
---

There are 3 possible scenarios when a person creates a DfE Identity account before using Access your teaching qualifications. They’re dependent on whether we can find the person’s details in the database of qualified teachers (DQT).

The result of the DQT check is presented to the user once they’ve created an account. It tells them whether or not they can continue to access their teaching qualifications. The scenarios for this page are:

- There is a matching record in the DQT
- There is no matching record in the DQT
- There is a record that potentially matches in the DQT



## Matching record in the DQT

When we’ve matched the user’s details to a record in the DQT, we tell them that they’ve created a DfE identity account and that they can move on to Access your teaching qualifications. We also tell them that they’ll only need to provide their email address the next time they sign in.

We also present this page to users when they’ve just gone through the basic authentication process (email, mobile phone number, name and date of birth) for services that do not require DQT checks.

![When we've found a match in the DQT](dqt-matched.png "When we've found a match in the DQT")


## No matching record in the DQT

When there is no record in the DQT, the person cannot sign in to Access your teaching qualifications. At this point, not being on the DQT means they do not have any teaching qualifications to access.

We tell them they cannot get in to AyTQ yet and give them the reason why. We also tell them that they’ve created a DfE Identity account, and once they’re eligible for AyTQ, they can just use their email to sign in to the account.

They will need to answer the further questions so we can check if they are on the DQT.

![When there's no record in the DQT](no-dqt.png "When there's no record in the DQT")

## A record that potentially matches in the DQT

This scenario occurs when we think we have found a match in the DQT, from the details given, but support need to do manual checks.

We tell the user they cannot sign in to Access your teaching qualifications yet and that we’ll email them when we’ve done the checks. We also tell them that we may need more information.


Again, we tell them they’ve created a DfE Identity account and they can sign in using just their email in the future.

If we find their details doing the manual checks, we email them to say they can now sign in to AyTQ. If the checks are unsuccessful, we’ll email the person to tell them why and what they can do next.

![When we need to do manual checks on the DQT](dqt-pending.png "When we need to do manual checks on the DQT")
