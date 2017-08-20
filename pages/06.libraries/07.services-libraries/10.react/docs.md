---
title: react
process:
    markdown: true
    twig: true
content:
    items: '@self.children'
    order:
        by: title
        dir: desc
    limit: 99
    pagination: false
---

{% for p in page.collection %}
<h2>[ {{ p.title }}]({{p.link}})</h2>
{% endfor %}