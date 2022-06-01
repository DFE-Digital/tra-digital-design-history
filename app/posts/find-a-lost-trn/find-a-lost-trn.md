---
layout: collection
title: Find a lost TRN
description: A service for TRN holders to securely retrieve their TRN if they’ve lost it
pagination:
  data: collections.find-a-lost-trn
  reverse: true
  size: 50
permalink: "find-a-lost-trn/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
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
        - text: Live service
          href: https://find-a-lost-trn.education.gov.uk/
        - text: Performance dashboard
          href: https://find-a-lost-trn.education.gov.uk/performance
        - text: Github repository
          href: https://github.com/DFE-Digital/find-a-lost-trn
        - text: Prototype
          href: https://find-a-lost-trn.herokuapp.com/
          description: |
            Username: trn
            Password: trn
        - text: Prototype repository
          href: https://github.com/DFE-Digital/find-a-lost-trn-prototype
---
