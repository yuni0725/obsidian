---
layout: page
title: Home
id: home
permalink: /
---

# 생기부

<strong>All Notes</strong>

<ul>
  {% assign recent_notes = site.notes %}
  {% for note in recent_notes %}
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
