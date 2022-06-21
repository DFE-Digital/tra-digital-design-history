---
  title: Private beta updates
  date: 2022-05-27
  screenshots:
    items:
      - text: "Check eligibility"
        src: check-eligibility_country-australia.png
      - text: "Not eligible"
        src: not-eligible.png
---

The first sprint of private beta mainly looked at the immediate content changes that we could make to the eligibility checker.

Many would-be applicants simply aren’t eligible, so there’s a huge benefit to having an eligibility checker that lets people know within a few questions whether or not QTS is for them.

We began by making the first page of the eligibility checker more akin to the standard GOV.UK start page, although this depends on a larger piece of work to understand how people are finding their way to QTS.

We added a ‘state/territory’ question after ‘In which country are you currently recognised as a teacher?’ to cater for countries that have more than one competent authority. This applies to some countries that are currently eligible, but will also apply to some of the new ones.

It helps us to understand more about the applicants, but also helps us to narrow down exactly what they need to send us.

##Kick-out screens

The most noticeable change this time was the combined ‘kick-out’ screen that replaces the individual screens we’ve used until now.

With the exception of the ‘Which country’ question, which gives users a ‘Not eligible’ screen if their country isn’t eligible yet, each question used to have a ‘Not eligible’ screen associated with it.

We now have a single dynamic screen that plays back all the reasons that someone isn’t eligible, which could be a single reason, or up to 4 (and could be any combination).

The screen also surfaces directions on other ways to explore teaching in England, but omits this where users answer ‘Yes’ to having sanctions on their record.

The main reason for this change is that we’re currently lacking quantitative data about users. While making them go through the questions even if their first answer makes them ineligible is a slight hindrance, the process is very quick and the trade-off is that we get to understand much more about our users.

‘Are you recognised as a teacher in the country where you trained?’

We’ve temporarily removed this question as we need to re-evaluate how useful it is. For some users, this and Question 1 will be essentially the same thing. We need to look at this question in more detail, so we've left the ability to reinstate it if need be.
