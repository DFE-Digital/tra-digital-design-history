---
  title: When the API is unavailable (iteration)
  date: 2022-03-01
  related:
    items:
    - text: Prototype PR
      href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/42
  screenshots:
    items:
      - text: "Start page"
        src: 01-start-page.png
      - text: "Taking longer than normal"
        src: 02-taking-longer-than-normal.png
---

Following on from the [original design](/find-a-lost-trn/api-down), we’ve made small changes to the flow.

The notification banner has been removed from the start page and replaced with a dedicated page. We changed this because:

- users are more likely to read a page, versus a banner which can often be skipped due to banner blindess
- putting the notification banner first obstructs the context setting of the service, and can be confusing to first time users

We’ve placed the ‘It’s taking us longer than usual’ page before the first information is gathered, but after the ‘Check if you have a TRN’ page, we do not need to show it to anyone who does not have a TRN.

The page also refers to ‘the information we need’, which is outlined in the page before, ‘We’ll ask you some questions’.

## Video walkthrough

{% from "embed/macro.njk" import appEmbed with context %}
{{ appEmbed({
  youtubeId: '5XU9mHiyaw0',
  title: 'Video of journey when the API is unavailable'
}) }}
