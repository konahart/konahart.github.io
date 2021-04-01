---
layout: default
---

## Recipes

<ul>
{% for recipe in site.recipes %}
<li><h3><a href="{{ recipe.url }}" class="accent">{{ recipe.title }}</a></h3></li>
{% endfor %}
</ul>
