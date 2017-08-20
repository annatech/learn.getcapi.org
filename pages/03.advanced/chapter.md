---
title: Advanced
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

### Chapter 3

# Advanced

How to ***secure*** the API, ***configure*** your server and more!

{% for p in page.collection %}
#### [ {{ p.title }}]({{p.link}})
{% endfor %}

### Additional Resources

http://seregazhuk.github.io

[Event-Driven PHP with ReactPHP: Event Loop And Timers](http://seregazhuk.github.io/2017/06/06/phpreact-event-loop/)