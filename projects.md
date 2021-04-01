---
layout: default
---

## Projects

<ul>
    {% for project in site.data.projects %}
    <li><h3 style="display: inline-block;"><a href="{{ project.url }}" class="accent">{{ project.name }}</a></h3>{{ project.description }}
    {% if project.tags.size > 0 %}<br />
    {% for tag in project.tags%}
        {% if forloop.last %}
            <span style="color: #777777;">{{tag}}</span>
        {% else %}
            <span style="color: #777777;">{{tag}}</span>,
        {% endif %}
    {% endfor %}
    {% endif %}
    </li>
    {% endfor %}
</ul>
