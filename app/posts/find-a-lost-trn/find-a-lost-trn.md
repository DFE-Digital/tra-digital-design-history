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
    parent: home
---
