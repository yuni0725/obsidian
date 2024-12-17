---
layout: page
title: Home
id: home
permalink: /
---

<strong>All Notes</strong>

{% assign notes = site.notes %}

<ul>
  <strong>1학년</strong>
  {% assign first_notes = notes | where: "grade", "1학년" %}
  {% for note in first_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
  <strong>2학년</strong>
{% assign second_notes = notes | where: "grade", "2학년" %}
  {% for note in second_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
  <strong>3학년</strong>
{% assign third_notes = notes | where: "grade", "3학년" %}
  {% for note in third_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
