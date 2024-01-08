---
layout: collection
title: Teaching record system (TRS) console
description: A service allowing DfE and TRA staff to manage data in the teaching record system.
pagination:
  data: collections.trs-console
  reverse: true
  size: 50
permalink: "trs-console/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
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
        - text: "TRS console prototype (password: tra)"
          href: https://trs-console-prototype-5326609a06da.herokuapp.com/
---