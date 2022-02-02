---
layout: collection
title: Find your TRN
description: A service for TRN holders to securely retrieve their TRN if they’ve forgotten it
pagination:
  data: collections.find-your-trn
  reverse: true
  size: 50
permalink: "find-your-trn/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: home
---
