---
layout: collection
title: Qualifications service
description: Where teachers check their qualifications, teacher induction status and download certificates. Formally known as the teacher self-service portal (TSSP)
pagination:
  data: collections.qualifications-service
  reverse: true
  size: 50
permalink: "qualifications-service/{% if pagination.pageNumber > 0 %}page/{{ pagination.pageNumber + 1 }}{% endif %}/"
override:tags:
  - post
eleventyComputed:
  eleventyNavigation:
    key: "{{ title }}"
    excerpt: "{{ description }}"
    parent: Home
related:
  sections:
    - title: Related content
      items:
        - text: Qualifications service prototype (QS)
          href: https://qualifications-prototype.herokuapp.com/  
        - text: GitHub - Qualifications service
          href: https://github.com/DFE-Digital/qualifications-service-prototype            
        - text: Old TSSP
          href: https://teacherservices.education.gov.uk/SelfService/Login     
---
