---
layout: page
permalink: /service/
title: Service
description: Events organized, reviewing, awards & grants, and supervision.
nav: true
nav_order: 7
---

<style>
  .service-section + .service-section {
    margin-top: 2.5rem;
  }
  .service-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .service-list > li {
    padding: 0.6rem 0;
    border-bottom: 1px solid var(--global-divider-color);
  }
  .service-list > li:last-child {
    border-bottom: none;
  }
  .service-entry {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 0.4rem 0.6rem;
  }
  .service-entry .service-title {
    font-weight: 500;
  }
  .service-entry .service-meta {
    color: var(--global-text-color-light);
  }
  .service-entry .service-year {
    margin-left: auto;
    color: var(--global-text-color-light);
    font-variant-numeric: tabular-nums;
    white-space: nowrap;
  }
  .service-note {
    margin: 0.25rem 0 0;
    color: var(--global-text-color-light);
    font-size: 0.9rem;
  }
  .service-note p {
    margin: 0;
  }
  .service-group {
    margin-bottom: 1rem;
  }
  .service-group:last-child {
    margin-bottom: 0;
  }
  .service-group h5 {
    margin-bottom: 0.3rem;
  }
  @media (max-width: 576px) {
    .service-entry .service-year {
      margin-left: 0;
    }
  }
</style>

{% assign events = site.data.service.events_organized %}
{% assign reviewing = site.data.service.reviewing %}
{% assign awards = site.data.service.awards %}
{% assign supervision = site.data.service.supervision %}

{% if events and events.size > 0 %}

<div class="service-section">
  <h3>Events Organized</h3>
  <ul class="service-list">
    {% for event in events %}
      <li>
        <div class="service-entry">
          <span class="service-title">
            {% if event.url %}<a href="{{ event.url }}">{{ event.title }}</a>{% else %}{{ event.title }}{% endif %}
          </span>
          {% if event.role %}<span class="service-meta">{{ event.role }}</span>{% endif %}
          {% if event.venue %}<span class="service-meta">{{ event.venue }}</span>{% endif %}
          {% if event.year %}<span class="service-year">{{ event.year }}</span>{% endif %}
        </div>
        {% if event.description %}<div class="service-note">{{ event.description | markdownify }}</div>{% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if reviewing and reviewing.size > 0 %}

<div class="service-section">
  <h3>Reviewing</h3>
  {% for group in reviewing %}
    {% if group.venues and group.venues.size > 0 %}
      <div class="service-group">
        <h5>{{ group.category }}</h5>
        <p>
          {% for venue in group.venues %}
            {{ venue.name }}{% if venue.abbr or venue.years %} (
              {%- if venue.abbr %}<strong>{{ venue.abbr }}</strong>{% endif -%}
              {%- if venue.abbr and venue.years %}, {% endif -%}
              {{- venue.years -}}
            ){% endif %}{% unless forloop.last %} &middot; {% endunless %}
          {% endfor %}
        </p>
      </div>
    {% endif %}
  {% endfor %}
</div>
{% endif %}

{% if awards and awards.size > 0 %}

<div class="service-section">
  <h3>Awards &amp; Grants</h3>
  <ul class="service-list">
    {% for award in awards %}
      <li>
        <div class="service-entry">
          <span class="service-title">{{ award.title }}</span>
          {% if award.awarder %}
            <span class="service-meta">
              {%- if award.awarder_url -%}<a href="{{ award.awarder_url }}">{{ award.awarder }}</a>{%- else -%}{{ award.awarder }}{%- endif -%}
            </span>
          {% endif %}
          {% if award.certificate %}<span class="service-meta"><a href="{{ award.certificate | relative_url }}">certificate</a></span>{% endif %}
          {% if award.year %}<span class="service-year">{{ award.year }}</span>{% endif %}
        </div>
        {% if award.description %}<div class="service-note">{{ award.description | markdownify }}</div>{% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if supervision and supervision.size > 0 %}

<div class="service-section">
  <h3>Supervision</h3>
  <ul class="service-list">
    {% for item in supervision %}
      <li>
        <div class="service-entry">
          <span class="service-title">
            {% if item.paper %}<a href="{{ item.paper | relative_url }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}
          </span>
          {% if item.year %}<span class="service-year">{{ item.year }}</span>{% endif %}
        </div>
        {% if item.students or item.type or item.description %}
          <div class="service-note">
            {{ item.students }}{% if item.students and item.type %} &middot; {% endif %}{{ item.type }}{% if item.description %} &middot; {{ item.description }}{% endif %}
          </div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
{% endif %}
