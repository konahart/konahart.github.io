---
layout: default
---

## Blog Posts
<ul class="posts">
{% for post in site.posts limit:5 %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
<li><a href="/posts.html">All Posts</a></li>
<li><a href="/feed.xml">RSS Feed</a></li>
</ul>

## Current Projects

<ul class="posts">
<li><a href="/promptbot">Promptbot</a> &raquo; An irc bot for writers</li>
<li>Studying  &raquo; <a href="https://www.coursera.org/course/algo">Algorithms: Design and Analysis, Part 1</a></li>
</ul>

## About

<ul class="posts">
<li>Email &raquo; <span style="color:#59B34C">laurel.elise.hart</span>&#64;gmail&#46;com</li>
<li>Resume &raquo; <a href="resume">Online</a> | <a href="resume/resume.pdf">PDF</a> | <a href="resume/resume.txt">TXT</a></li>
<li>Github &raquo; <a href="http://github.com/konahart">konahart</a></li>
<li>LinkedIn &raquo; <a href="http://www.linkedin.com/in/laurelehart">laurelehart</a></li>
<li>IRC (Freenode) &raquo; <a href="https://freenode.net/">Kona</a></li>
<li>Twitter &raquo; <a href="https://twitter.com/konahart"><span style="color:#000000">@</span>konahart</a></li>
</li>
</ul>
