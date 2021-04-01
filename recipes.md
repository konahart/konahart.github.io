---
layout: default
permalink: /recipes/
---

## Recipes

<ul>
{% for recipe in site.recipes %}
    {% if recipe.external_url %}
      <li><h3><a href="{{ recipe.external_url }}" class="accent">{{ recipe.title }}</a></h3></li>
    {% else %}
      <li><h3><a href="{{ recipe.url }}" class="accent">{{ recipe.title }}</a></h3></li>
      {% endif %}
{% endfor %}

</ul>
