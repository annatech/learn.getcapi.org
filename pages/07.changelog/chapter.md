---
title: Changelog
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
        dir: desc
    limit: 99
    pagination: false
---

### Chapter 6

# Changelog

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}