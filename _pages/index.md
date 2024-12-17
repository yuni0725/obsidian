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
  {% for note in notes.select { |item| item.include?("1학년") } %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
  <strong>2학년</strong>
{% for note in notes.select { |item| item.include?("2학년") } %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
  <strong>3학년</strong>
{% for note in notes.select { |item| item.include?("3학년") } %}
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
