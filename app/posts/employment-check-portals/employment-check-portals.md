---
layout: collection
title: Employment check portals
description: Where employers and agencies can check teacher details
pagination:
  data: collections.employment-check-portals
  reverse: true
  size: 50
permalink: "employment-check-portals/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: home
---
