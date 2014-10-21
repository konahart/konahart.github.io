---
layout: default
---

## Blog Posts
<ul class="posts">
{% for post in site.posts %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
<li><a href="/feed.xml">RSS Feed</a></li>
</ul>

## Current Projects

<ul class="posts">
<li><span><a href="/promptbot">Promptbot</a></span> &raquo; An irc bot for writers</li>
</ul>

## About

<ul class="posts">
<li>Email &raquo; <span style="color:#59B34C">laurel.elise.hart</span>&#64;gmail&#46;com</li>
<li>Resume &raquo; <a href="resume.html">Online</a> | <a href="https://github.com/konahart/resume/blob/master/resume.pdf?raw=true">PDF</a></li>
<li>Github &raquo; <a href="http://github.com/konahart">konahart</a></li>
<li>LinkedIn &raquo; <a href="http://www.linkedin.com/in/laurelehart">laurelehart</a></li>
<li>IRC (Freenode) &raquo; <a href="https://freenode.net/">Kona</a></li>
</li>
</ul>
