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

{% set options = { items: {'@page.children': '/react'}, 'limit': 5, 'order': {'by': 'date', 'dir': 'desc'}, 'pagination': true } %}
{% set my_collection = page.collection(options) %}

<ul>
{% for p in my_collection %}
<li>{{ p.title }}</li>
{% endfor %}
</ul>