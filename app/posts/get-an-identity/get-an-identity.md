---
layout: collection
title: Teacher Services Account
description: A way for teachers and would-be teachers to access many DfE services with one login, and be able to inform DfE only once whenever their details change. The name we’re using in the prototype to describe GAI is, Teacher services Account (TSA).
pagination:
  data: collections.get-an-identity
  reverse: true
  size: 50
permalink: "get-an-identity/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
related:
  sections:
    - title: Related content
      items:
        - text: "Prototype (password: trn)"
          href: https://find-a-lost-trn.herokuapp.com/
        - text: Prototype repository
          href: https://github.com/DFE-Digital/find-a-lost-trn-prototype
        - text: Latest video walkthrough (24 August 2022)
          href: https://vimeo.com/742598497
---

<!-- <h2 class="govuk-heading-m">Why we are doing this</h2>

A case study about Millie and her journey through DfE’s digital services. When something goes wrong, things get silly.

[View the PDF](/docs/when-things-got-silly-for-millie.pdf)
[View Google Slides](https://docs.google.com/presentation/d/e/2PACX-1vQqN02_5934OOMp0vx-5GREBmk88mXSz0OfklDh0VI6wMPFeQBHHnFro2mq7tSgks_89WQVgJ1OArUc/embed?start=false&loop=false&delayms=10000)

<div class="app-vimeo govuk-!-margin-bottom-9" style="padding-top: 62%">
  <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQqN02_5934OOMp0vx-5GREBmk88mXSz0OfklDh0VI6wMPFeQBHHnFro2mq7tSgks_89WQVgJ1OArUc/embed?start=false&loop=false&delayms=10000" frameborder="0" width="1440" height="839" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
</div>

<h2 class="govuk-heading-m">Who the users are</h2>

<h3 class="govuk-heading-s">Teachers and would-be teachers</h3>

Get an identity will allow teachers and would-be teachers to:

* access many teacher services with one login
* provide and update their data once across all teacher services, instead of maintaining it separately within each individual service

<h3 class="govuk-heading-s">Department for Education</h3>

The service aims to build a single view of teacher career paths for DfE policymakers, analysts and service teams.

<h3 class="govuk-heading-s">Teacher Services teams</h3>

Get an identity will provide drop-in journeys, APIs and processes for identity creation and management. This aims to reduce the costs of creating and maintaining public-facing teacher services. -->

<h2 class="govuk-heading-m">Posts</h2>
