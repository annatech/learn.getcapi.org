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

## React PHP

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}