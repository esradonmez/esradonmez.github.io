---
layout: page
permalink: /teaching/
title: Teaching
description: Courses taught at the Institute for Natural Language Processing (IMS), University of Stuttgart.
nav: true
nav_order: 4
---

<style>
  .teaching-year {
    margin-top: 2rem;
  }
  .teaching-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .teaching-list > li {
    padding: 0.6rem 0;
    border-bottom: 1px solid var(--global-divider-color);
  }
  .teaching-list > li:last-child {
    border-bottom: none;
  }
  .teaching-entry {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 0.4rem 0.6rem;
  }
  .teaching-entry .teaching-title {
    font-weight: 500;
  }
  .teaching-entry .teaching-meta {
    color: var(--global-text-color-light);
  }
  .teaching-entry .teaching-term {
    margin-left: auto;
    color: var(--global-text-color-light);
    white-space: nowrap;
  }
  @media (max-width: 576px) {
    .teaching-entry .teaching-term {
      margin-left: 0;
    }
  }
</style>

{% assign courses_by_year = site.teachings | sort: 'year' | reverse | group_by: 'year' %}
{% for year_group in courses_by_year %}

<h3 class="teaching-year">{{ year_group.name }}</h3>
<ul class="teaching-list">
  {% for course in year_group.items %}
    {% assign body = course.content | strip %}
    <li>
      <div class="teaching-entry">
        <span class="teaching-title">
          {% if body != "" %}<a href="{{ course.url | relative_url }}">{{ course.title }}</a>{% else %}{{ course.title }}{% endif %}
        </span>
        {% if course.instructor %}<span class="teaching-meta">{{ course.instructor | replace: "Esra Dönmez (", "" | replace: ")", "" }}</span>{% endif %}
        {% if course.term %}<span class="teaching-term">{{ course.term }}</span>{% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
{% endfor %}
