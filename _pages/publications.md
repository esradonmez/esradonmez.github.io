---
layout: page
permalink: /publications/
title: Publications
description: publications in reversed chronological order.
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<style>
  .pub-toolbar {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.75rem;
    margin: 0 0 0.5rem;
  }
  .pub-toolbar .bibsearch-form-input {
    margin: 0;
  }
  .pub-toolbar .scholar-link {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    padding: 0.5rem 0.9rem;
    border: 1px solid var(--global-theme-color);
    border-radius: 6px;
    color: var(--global-theme-color);
    font-size: 0.95rem;
    white-space: nowrap;
    text-decoration: none;
  }
  .pub-toolbar .scholar-link:hover {
    background-color: var(--global-theme-color);
    color: var(--global-hover-text-color);
  }
  .pub-note {
    margin: 0 0 1rem;
    font-size: 0.85em;
  }
</style>

<div class="pub-toolbar">
  {% include bib_search.liquid %}
  <a class="scholar-link" href="https://scholar.google.com/citations?user=2WZpzhoAAAAJ"><i class="ai ai-google-scholar"></i> Google Scholar</a>
</div>

<p class="pub-note text-muted"><sup>*</sup> denotes equal contribution.</p>

<div class="publications">

{% bibliography %}

</div>
