---
  title: User research – March 2022
  date: 2022-03-11
  screenshots:
    items:
      - text: "Taking longer than normal"
        src: 01-taking-longer-than-normal.png
      - text: "Asking about QTS"
        src: 02-asking-about-qts.png
      - text: "Iterated helpdesk page"
        src: 03-iterated-helpdesk-page.png
      - text: "Iterated success page"
        src: 04-iterated-success-page.png
      - text: "Iterated no match page"
        src: 05-iterated-no-match-page.png
  related:
    items:
    - text: Airtable of research findings
      href: https://airtable.com/appaL0YraqvBm3f9f/
    - text: Research videos
      href: https://drive.google.com/drive/u/1/folders/1-8H9zzuASJW8k8F7vHzYC2TunONjaIU9
---

In March 2022 we researched the Find a lost TRN service with teachers, covering the scenarios:

- setting the context of applying for a job
- finding a TRN while the API is unavailable
- successfully finding a TRN when the API is up
- not finding a TRN because the details didn’t match

## Walkthrough and research summary

{% from "embed/macro.njk" import appEmbed with context %}
{{ appEmbed({
  youtubeId: 'ZtiiMAbYvkg',
  title: 'Video of journey when the API is unavailable'
}) }}

This can be compared with [the previous walkthrough](/find-a-lost-trn/api-down-iteration/#video-walkthrough).

## Initial teacher training

Initial teacher training  was a confusing term – one user didn't recognise that this meant their PGCE, and chose the wrong answer. Another didn’t know which of the places they trained at and was confused about whether to give a university or school.

We changed the question to be about QTS, if they have QTS and where they got it. This has removed the confusion.

We still need to consider the edge case where a QTS was awarded another way, for example by professional recognition.

## No match page

We iterated from [the previous design](/find-a-lost-trn/no-match/). After reading about not finding their TRN, and the possible reasons for this – users have a choice – to try again with new information or to continue with a support request. In the old design this was masked by a default journey that was ‘try again’ and a hidden journey, behind a disclosure, for continuing to support.

In the new design the question is explicit, essentially, what do you want to do next?

Details about the phone line have also been removed, they are on the end page and do not need to be repeated here. Submitting a support request and then calling the support number is a better outcome – as their information will be available to the agents.

## Smaller design changes

We:

- replaced ‘Information received’ with ‘We’ve received your request’
- replaced ‘Success’ with ‘We’ve found your TRN’
- removed the full-stop from the end of the TRN in the email, so it is not interpreted as part of the TRN
- gave context about what normal is on the ‘taking longer than normal’ page, so users understand their is a technical problem and that normally TRNs are available right away
- added the feedback link to the failure page as well as the success one
- gave more detail about the support time, 2 days being normal with a maximum of 5 (we’re still testing this and need to check it’s accurate)
- added a section about how to get a TRN to the guidance page
