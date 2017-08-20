---
title: joomla
taxonomy:
    category:
        - docs
content:
    items: '@self.children'
    order:
        by: title
        dir: asc
    limit: 99
    pagination: false
---

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}