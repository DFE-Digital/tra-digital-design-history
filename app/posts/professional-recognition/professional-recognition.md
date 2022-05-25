---
layout: collection
title: Professional recognition
description: The professional recognition of overseas trained teachers with English QTS
pagination:
  data: collections.professional-recognition
  reverse: true
  size: 50
permalink: "professional-recognition/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
---
