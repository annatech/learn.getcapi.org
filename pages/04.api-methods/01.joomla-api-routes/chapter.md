---
title: 'Joomla API Routes'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: true
content:
    items: '@self.children'
    order:
        by: title
        dir: asc
    limit: 99
    pagination: false
---

## Joomla API Routes

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}