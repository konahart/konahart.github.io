---
layout: default
title: Laurel "Kona" Hart, Computational Linguist
---

<div class="top section">
<h3>Blog Posts</h3>

<ul>
{% for post in site.categories.posts limit:5 %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
<li><a href="/posts.html">All Posts</a></li>
<li><a href="/feed.xml">RSS Feed</a></li>
</ul>
</div>

<div class="section">
<h3>Projects</h3>

<ul>
<li><a href="/promptbot">Promptbot</a> &raquo; An irc bot for writers</li>
<li><a href="/constellations">Constellations</a> &raquo; Creative writing software UI concept</li>
</li>
</ul>
</div>

<div class="section">
<h3>About</h3>
<ul>
<li>Email &raquo; <span style="color:#59B34C">laurel.elise.hart</span>&#64;gmail&#46;com</li>
<li>Resume &raquo; <a href="resume">Interactive</a> | <a href="resume/resume.pdf">PDF</a> | <a href="resume/resume.txt">TXT</a></li>
<li>Github &raquo; <a href="http://github.com/konahart">konahart</a></li>
<li>LinkedIn &raquo; <a href="http://www.linkedin.com/in/laurelehart">laurelehart</a></li>
<li>IRC (Freenode) &raquo; <a href="https://freenode.net/">Kona</a></li>
<li>Twitter &raquo; <a href="https://twitter.com/konahart"><span style="color:#000000">@</span>konahart</a></li>
</li>
</ul>
</div>
