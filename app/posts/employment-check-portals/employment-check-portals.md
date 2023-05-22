---
layout: collection
title: Check the record of a teacher
description: Where employers and agencies can check teacher details
pagination:
  data: collections.check-the-record-of-a-teacher
  reverse: true
  size: 50
permalink: "check-the-record-of-a-teacher/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
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
        - text: GOV.UK guidance
          href: https://www.gov.uk/guidance/teacher-status-checks-information-for-employers
---
