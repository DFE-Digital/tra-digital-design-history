---
layout: collection
title: Teacher misconduct
description: Regulating the teaching profession and the process for dealing with cases of serious misconduct
pagination:
  data: collections.teacher-misconduct
  reverse: true
  size: 50
permalink: "teacher-misconduct/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
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
        - text: Unavailability prototype
          href: https://teacher-misconduct.herokuapp.com/
---
