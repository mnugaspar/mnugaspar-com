---
layout: default
title: Projects
permalink: /projects
---

# Work

I try to learn much from the initiatives I'm lucky to be a part of. I'm motivated by projects that recognise the complex and often interdependent nature of our problems - and so require interdisciplinary teams and solutions.

<br>

<p>

<div class="row">
{% assign projects = site.data.projects | sort: "date" | reverse %}
  {% for project in projects %}
  <div class="column left faded">{{ project.duration }}</div>
  <div class="column middle"></div>
  <div class="list-entry column right">
    <div style="font-weight:500">{{ project.role }}, <a target="_blank" rel="noopener" href="{{ project.url }}">{{ project.name }}</a></div>
    <div><span class="badge badge-secondary">{{ project.tags }}</span></div>
    <div>{{ project.description_html }}</div>
  </div>
  {% endfor %}
</div>

</p>

<style>
  .wrapper {
    max-width: 46em
  }
</style>
