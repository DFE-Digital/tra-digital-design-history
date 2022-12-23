---
layout: collection
title: Manage teacher misconduct referrals
description: A service for caseworkers to manage referrals of serious misconduct by a teacher
pagination:
  data: collections.manage-teacher-misconduct-referrals
  reverse: true
  size: 50
permalink: "manage-teacher-misconduct-referrals/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
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
        - text: "Prototype (password: tms)"
          href: https://manage-referrals-prototype.herokuapp.com/
---
