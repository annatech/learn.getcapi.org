---
title: Methods
published: true
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

### Chapter 4

# Methods

API methods inventory for core plugins and API extentions.

**Check out the new API Docs and Developer Sandbox!**

<span style="text-align:center" class="fa fa-arrow-down fa-3x"></span>

### [Swagger API Doc](/swagger-api-doc)
### [getcapi.io](http://getcapi.io)

{% for p in page.collection %}
- [ {{ p.title }}]({{p.link}})
{% endfor %}
