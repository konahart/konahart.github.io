---
layout: default
---
<ul>
{% for recipe in site.recipes %}
<li><span><a href="{{ recipe.url }}">{{ recipe.title }}</a></span></li>
{% endfor %}
</ul>
