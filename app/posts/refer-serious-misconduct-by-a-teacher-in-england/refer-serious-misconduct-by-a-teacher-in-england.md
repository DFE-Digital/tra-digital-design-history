---
layout: collection
title: Refer serious misconduct by a teacher in England
description: Regulating the teaching profession and the process for dealing with cases of serious misconduct
pagination:
  data: collections.refer-serious-misconduct-by-a-teacher-in-england
  reverse: true
  size: 50
permalink: "refer-serious-misconduct-by-a-teacher-in-england/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
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
          href: https://refer-misconduct-prototype.herokuapp.com/
        - text: "Old prototype (password: tms)"
          href: https://teacher-misconduct.herokuapp.com/
---
