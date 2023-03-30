---
layout: collection
title: DfE Identity account
description: A way for teachers and would-be teachers to access many DfE services with one login, and be able to inform DfE only once whenever their details change. Formerly Get an Identity, we’re now asking users to actively create an account so we're testing the name, Teaching services account. 
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
        - text: "DIA Prototype (password: gai)"
          href: https://get-an-identity-prototype.herokuapp.com/
        - text: Prototype repository
          href: https://github.com/DFE-Digital/get-an-identity-prototype
        - text: Video guide for ID - basic auth (no-dqt)
          href: https://vimeo.com/813107414
        - text: Video guide for ID - auth and DQT look-up
          href: https://vimeo.com/813107498
        - text: "Service design for DfE Identity account and qualification service (Lucid)"
          href: https://lucid.app/lucidspark/60528544-3d4f-4b37-a0cd-078d59d95e88/edit?view_items=GAqE2sfBl.eU&invitationId=inv_60a47740-05d2-4d85-acc1-a742b955fd86
        - text: "DfE Identity account Problem definition (Lucid)"
          href: https://lucid.app/lucidspark/4cd25e29-f5b4-48ae-b583-ee5b8364d0ec/edit?invitationId=inv_1050e41c-9998-4899-b0c0-0fd7d1907221#
        - text: "DfE Identity account design concepts (Lucid)"
          href: https://lucid.app/lucidspark/7c097684-3e9c-422f-b218-1aa0e9f70648/edit#
        - text: "DfE Identity account integrations with services (lucid)"
          href: https://lucid.app/lucidspark/7c097684-3e9c-422f-b218-1aa0e9f70648/edit#
        - text: "DfE Identity account mapped out against different services (lucid)"
          href: https://lucid.app/lucidspark/b88634d8-2452-4ed6-9c7c-010383770731/edit?invitationId=inv_9a36d007-204a-41ed-b8c3-1f49d5e63a05#
---

<h2 class="govuk-heading-m">DfE Identity account</h2>

We’re testing alternative names for Get an Identity (GAI) now that we’re asking users to create an account. For the first round of user testing we’re using the name, <b>DfE Identity account</b> (DIA).
<h2 class="govuk-heading-m">Posts</h2>
