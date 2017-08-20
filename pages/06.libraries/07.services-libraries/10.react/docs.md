---
title: react
process:
    markdown: true
    twig: true
content:
    items: '@page./libraries/services-libraries/react'
---

{{ dump(page.collection[libraries/services-libraries/react]) }}

{% for p in page.collection %}
<h2>{{ p.title }}</h2>
{{ p.summary }}
{% endfor %}