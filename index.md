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
<li><span>MultiR</span> &raquo; <a href="/promptbot">Generating training data for relation extraction.</a></li>
<li><span>Promptbot</span> &raquo; <a href="/promptbot">An irc bot for writers.</a></li>
</ul>

## About

<ul class="posts">
<li><a href="/resume">Resume</a></li>
<li><a href="http://github.com/konayashi">Github</a></li>
<li><a href="http://www.linkedin.com/in/laurelehart">LinkedIn</a></li>
</li>
</ul>

