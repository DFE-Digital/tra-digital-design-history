---
layout: collection
title: Check the Children’s Barred List
description: Where employers and agencies can check if someone appears on the Children’s Barred List
pagination:
  data: collections.check-the-childrens-barred-list
  reverse: true
  size: 50
permalink: "check-the-childrens-barred-list/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
---
