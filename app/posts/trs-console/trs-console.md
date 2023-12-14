---
layout: collection
title: Teaching record system (TRS) console
description: A digital service for DfE staff to manage data in the teaching record system.
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
---