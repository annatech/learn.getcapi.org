---
title: react
process:
    markdown: true
    twig: true
---

{{ dump(page.collection[libraries/services-libraries/react]) }}

{% for p in page.collection %}
<h2>{{ p.title }}</h2>
{{ p.summary }}
{% endfor %}