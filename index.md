---
layout: default
title: Kona Goodhart, Software engineer &mdash; Computational linguist
---

<div class="contents">
<div class="top section" id="Projects">
  <h2>Projects</h2>
  <ul>
    {% for project in site.data.projects limit:3 %}
    <li><h3><a href="{{ project.url }}" class="accent">{{ project.name }}</a></h3> &raquo; {{ project.description }}</li>
    {% endfor %}
    <li><a href="/projects.html">More...</a></li>
  </ul>
</div>
<hr>
<div class="section" id="More">
  <h2>Etcetera</h2>
  <ul>
    <li><h3><a href="https://darlingbat.com">Games</a></h3> &raquo; Role-playing tabletop games</li>
    <li><h3><a href="/design.html">Design</a></h3> &raquo; Sometimes I make logos</li>
    <li><h3><a href="/recipes.html">Recipes</a></h3> &raquo; Adventures in baked goods and mixed drinks</li>
  </ul>
</div>
<hr>
<div class="section" id="Contact">
  <h2>Contact</h2>
  <ul>
    <li><h3>Email</h3> &raquo; hi&#64;<span class="accent">konahart</span>&#46;com</li>
    <li><h3>Resume</h3> &raquo; <a href="resume" class="accent">Interactive</a> | <a href="resume/resume.pdf" class="accent">PDF</a> | <a href="resume/resume.txt" class="accent">TXT</a></li>
    <li><h3>Github</h3> &raquo; <a href="http://github.com/konahart" class="accent">konahart</a></li>
    <li><h3>LinkedIn</h3> &raquo; <a href="http://www.linkedin.com/in/konahart" class="accent">konahart</a></li>
    <li><h3>Twitter</h3> &raquo; <a href="https://twitter.com/konahart" class="accent"><span style="color:#000000; font-weight: normal;">@</span>konahart</a></li>
  </ul>
</div>
</div>
