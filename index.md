---
layout: default
---

## Blog Posts
<ul class="posts">
{% for post in site.posts %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## Current Projects

<ul class="posts">
<li><span>Hardware</span> &raquo; <a href="http://georgiareh.com/cockroaches">Cockroaches</a></li>
<li><span>Software</span> &raquo; <a href="http://github.com/greh/coconuts">Math in Python</a></li>
</ul> 



