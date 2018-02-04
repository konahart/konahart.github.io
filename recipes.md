---
layout: default
---
## Recipes
<ul>
{% for recipe in site.recipes %}
<li><span><a href="{{ recipe.url }}" class="accent">{{ recipe.title }}</a></span></li>
{% endfor %}
</ul>
