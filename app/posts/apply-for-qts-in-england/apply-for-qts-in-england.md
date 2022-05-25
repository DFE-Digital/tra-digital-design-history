---
layout: collection
title: Apply for qualified teacher status in England
description: The professional recognition of overseas trained teachers with English QTS
pagination:
  data: collections.apply-for-qts-in-england
  reverse: true
  size: 50
permalink: "apply-for-qts-in-england/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
---
