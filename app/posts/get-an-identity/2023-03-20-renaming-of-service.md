---
  title: Naming the identity service
  date: 2023-03-20
  related:
    sections:
      - title: DfE Identity account
        items:
          - text: Replica journey in prototype (password, gai)
            href: https://get-an-identity-prototype.herokuapp.com
---


## At the beginning

The identity service started as Get an Identity to access Teacher Services (GAI). This was when it was intended to replace the signing-in process for the various teacher services but not be called out in the interface as a separate service.  

GAI was an internal name for those working on it - not to be surfaced to users. The idea was to seamlessly integrate with the Apply for an NPQ service first - the user wouldn’t know they were crossing service boundaries.


## Problems

We’d identified some potential problems around this approach. First, each service needs its own cookie, privacy and accessibility notices. For the NPQ integration, we redesigned the privacy notice and accessibility statement to include both services. But this wasn’t possible for the cookie policy because cookies are tied to a domain. We couldn’t call out both services’ cookies on one page and ask a user to accept or reject them.

We had to keep these separate so a user would see the different cookie policies according to what page they were on, but we didn’t tell them that there were two services.

Another problem we identified early was that managing a single design between 2 services would take a lot of work. For example, if they start using different versions of the GOV.UK design system.

While testing the GAI and Apply for an NPQ integration, we saw users needing clarification about the questions we were asking. Trying to integrate GAI seamlessly meant that we did not tell users that they were creating an account or that we were trying to find their details in the database of qualified teachers.

## Teaching service account

At this point, we decided to call the service out to the user - we’d tell them they were creating an account and what this meant for them. This would help solve some of the issues highlighted.

The next service we planned to integrate with was Apply for QTS in England, so we planned to test a new name with the research participants. The drawbacks to this were that the users of this service are predominantly based overseas and may not have English as a first language. Also, the account is for more than just the users of one service - it’s for any user of DfE’s teacher services with the identity solution at the start.

We did an asynchronous service naming session within the team and decided to use ‘Teaching services account’ for the Apply for QTS testing. Given the limitations we’d identified with testing the Apply for QTS integration, we also looked at other potential ways of getting user feedback on the name.

We had the idea of running a poll on Twitter using DfE’s account, but we didn’t receive an encouraging response from the comms team, so we put it in front of Apply for QTS users. During testing, participants all expected to create an account but Teaching Services account didn’t appear to resonate with them. One said, ‘I don’t know what this is’.

## DfE Identity account

Teaching services doesn’t mean much to our users - they identify more with ‘DfE’ when using our services. We decided to anchor the account to ‘DfE’ and to use ‘Identity’ as it’s unique to each user.

We were conscious about DfE Sign-in being a similar-sounding name - but it’s a different user base so we’re confident we can avoid confusion. We’ll see how it lands in future research sessions and act upon any overwhelming feedback, but with it being quite difficult to test in this particular context, we don’t want to keep changing the name.

So, there it is - the DfE Identity account.
