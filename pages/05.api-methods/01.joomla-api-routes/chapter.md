---
title: 'Joomla API Routes'
taxonomy:
    category:
        - docs
content:
    items: '@self.children'
    order:
        by: title
        dir: desc
    limit: 99
    pagination: false
---

## Joomla API Routes

### [User](/api-methods/joomla-api-routes/user) ####
### [Content](/api-methods/joomla-api-routes/content) ####
### [Tags](/api-methods/joomla-api-routes/tags) Coming soon! ####
### [Token](/api-methods/joomla-api-routes/token) ####
### [CMS](/api-methods/joomla-api-routes/cms) ####
### [ARS](/api-methods/joomla-api-routes/ars) ####

{% for p in page.collection %}
<h2>{{ p.title }}</h2>
{{ p.summary }}
{% endfor %}