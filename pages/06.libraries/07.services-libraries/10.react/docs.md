---
title: react
process:
    markdown: true
    twig: true
content:
    items: '@root.libraries.services.libraries.react'
---

{% for p in page.collection %}
<h2>{{ p.title }}</h2>
{{ p.summary }}
{% endfor %}