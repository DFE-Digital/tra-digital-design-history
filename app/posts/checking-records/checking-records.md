---
layout: collection
title: Checking records
description: Checking teacher records as a service
pagination:
  data: collections.checking-records
  reverse: true
  size: 50
permalink: "checking-records/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: home
---
