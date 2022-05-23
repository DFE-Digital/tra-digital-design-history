---
layout: collection
title: Teacher self-service portal
description: Where teachers can change their personal details or download certificates
pagination:
  data: collections.teacher-self-service-portal
  reverse: true
  size: 50
permalink: "teacher-self-service-portal/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
related:
  items:
  - text: Live service
    href: https://teacherservices.education.gov.uk/SelfService/Login
  - text: GOV.UK start page
    href: https://www.gov.uk/guidance/teacher-self-service-portal
  - text: Wireframe prototype
    href: https://tssp-prototype.herokuapp.com/
---
