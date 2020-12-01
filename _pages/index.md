---
layout: default
title: Home
id: home
permalink: /
---

# Kumusta?

Hi! I’m Manu, working in health technology and on human rights.

My work at [University of the Philippines Manila](https://www.up.edu.ph) focuses on improving healthcare access and systems through telehealth. After hours I volunteer for [Amnesty International Philippines](https://www.amnesty.org.ph).

This website is a work in progress: it consists of notes (a few of them long, most are half-baked) on health tech, queer and youth rights, or anything that's of personal interest. Maybe we share some of them - feel free to explore!

Say hi over [Twitter](https://twitter.com/mnugaspar) or [m[at]mnugaspar.com](mailto:m@mnugaspar.com) 👋🏽 I go by he/him.

<br>

<div class="grid-element">
<p><b>Recent work</b></p>

  {% assign project_limit = 3 %}
  {% for project in site.data.projects limit: project_limit %}
  <div class="list-entry">
    <div><a target="_blank" rel="noopener" href="{{ project.url }}">{{ project.name }}</a> <span class="faded">({{ project.date | date: "%Y" }})</span></div>
    <div>{{ project.description_html }}</div>
  </div>
  {% endfor %}

  {% assign additional_projects = site.data.projects.size | minus: project_limit %}
  {% if additional_projects > 0 %}
  <div>
    <p>
      <a class="internal-link" href="/projects">
        I joined {{ additional_projects }} more projects.</a>
    </p>
  </div>
  {% endif %}
</div>

<br>

<div class="grid-element">
  <p><b>Recent notes</b></p>

  {% assign post_limit = 3 %}
  {% for post in site.notes limit: post_limit %}
    <div class="list-entry">
      <div><a class="internal-link" href="{{ post.url }}">{{ post.title }}</a> <span class="faded">({{ page.last_modified_at | date: "%Y-%m-%d" }})</span></div>
      <div>{{ post.excerpt }}</div>
  {% endfor %}

  <p>
     <a class="internal-link" href="/notes">
       I wrote {{ site.notes.size | minus: post_limit }} more notes.</a>
  </p>
</div>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
