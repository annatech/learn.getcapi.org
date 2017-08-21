---
title: Libraries
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

### Chapter 5

# Libraries

Overview of libraries included in cAPI Core Package.

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}