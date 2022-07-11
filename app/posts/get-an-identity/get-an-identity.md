---
layout: collection
title: Get an identity to access Teacher Services
description: Getting a central record for a user to use in your service
pagination:
  data: collections.get-an-identity
  reverse: true
  size: 50
permalink: "get-an-identity/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
---
