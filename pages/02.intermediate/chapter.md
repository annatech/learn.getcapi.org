---
title: Intermediate
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

### Chapter 2

# Intermediate

How to configure the API and make ***simple*** REST calls

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}
