---
layout: page
title: Home
id: home
permalink: /
---

<strong>All Notes</strong>

{% assign notes = site.notes %}

<div class=final-wrapper>
  <div class="grade-wrapper">
    <strong class="title-text">1학년</strong>
    <ul>
      {% assign first_notes = notes | where: "grade", "1학년" %}
      {% for note in first_notes %}
        <li>
          <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
        </li>
      {% endfor %}
    </ul>
  </div>
  <div class="grade-wrapper">
    <strong class="title-text">2학년</strong>
    <ul>
      {% assign second_notes = notes | where: "grade", "2학년" %}
      {% for note in second_notes %}
        <li>
          <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
        </li>
      {% endfor %}
    </ul>

  </div>
  <div class="grade-wrapper">
    <strong class="title-text">3학년</strong>
    <ul>
      {% assign third_notes = notes | where: "grade", "3학년" %}
       {% for note in third_notes %}
          <li>
            <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
          </li>
      {% endfor %}
    </ul>
  </div>
</div>

<style>
  .wrapper {
    max-width: 46em;
  }
  .final-wrapper {
    display : flex;
    align-items : center;
    justify-content : center;
    gap : 30px;

  }
  .grade-wrapper {

  }
  .title-text {
    font-size : 16px;
  }
</style>
