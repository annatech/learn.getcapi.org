---
title: react
process:
    markdown: true
    twig: true
content:
    items: '@self.children'
    order:
        by: date
        dir: desc
    limit: 10
    pagination: true
---

{% set default_collection = page.collection %}