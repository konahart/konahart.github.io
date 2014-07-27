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
<li><span>MultiR</span> &raquo; Generating training data for relation extraction.</li>
<li><span><a href="/promptbot">Promptbot</a></span> &raquo; An irc bot for writers.</li>
</ul>

## About

<ul class="posts">
<li><a href="/resume">Resume</a></li>
<li><a href="http://github.com/konayashi">Github</a></li>
<li><a href="http://www.linkedin.com/in/laurelehart">LinkedIn</a></li>
</li>
</ul>

