---
layout: default
---
## Posts
{% for post in site.posts %}
<li><span><a href="{{ post.url }}" class="accent">{{ post.title }}</a>  &raquo; {{ post.date | date_to_string }}</span></li>
{% endfor %}
