---
layout: default
---

{% for recipe in site.recipes %}
<li><span><a href="{{ recipe.url }}">{{ recipe.title }}</a></li>
{% endfor %}
