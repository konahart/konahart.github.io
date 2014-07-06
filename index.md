---
layout: default
---

<h1><a href="/">Georgia Reh</a></h1>
I'm a mathematician. Sometimes I build robots.


----------

## Blog Posts
<ul class="posts">
{% for post in site.posts %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## Current Projects
Cockroaches:  
http://georgiareh.com/cockroaches  
Math in python:  
https://github.com/Greh/coconuts  



