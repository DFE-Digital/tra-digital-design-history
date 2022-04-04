---
layout: collection
title: Employment checks portal
description: Where employers can check teacher details
pagination:
  data: collections.employment-checks-portal
  reverse: true
  size: 50
permalink: "employment-checks-portal/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: home
---
