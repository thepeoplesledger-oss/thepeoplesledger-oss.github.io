---
layout: single
classes: wide
title: "The People’s Ledger"
author_profile: false
---

<!-- ========================= -->
<!--  PRIMARY FEATURED STORY   -->
<!-- ========================= -->

{% assign primary = site.posts | where: "featured", "primary" | first %}
{% if primary %}
<div class="featured-primary" style="margin-bottom: 3rem;">

  <!-- Responsive image: top on mobile, left on desktop -->
  <div style="display: flex; flex-wrap: wrap; gap: 2rem; align-items: flex-start;">
    
    <!-- Image -->
    <div style="flex: 1 1 350px; min-width: 300px;">
      <img src="{{ primary.header.image }}" alt="{{ primary.title }}" style="width: 100%; border-radius: 6px;">
    </div>

    <!-- Text -->
    <div style="flex: 2 1 400px; min-width: 300px;">
      <h2 style="margin-top: 0;">{{ primary.title }}</h2>
      <p>{{ primary.excerpt }}</p>
      <a href="{{ primary.url }}" class="btn btn--primary">Read Full Story →</a>
    </div>

  </div>
</div>
{% endif %}

---

<!-- ========================= -->
<!--  SECONDARY FEATURED STORIES -->
<!-- ========================= -->

{% assign secondary = site.posts | where: "featured", "secondary" | slice: 0, 2 %}
{% if secondary.size > 0 %}
<div class="secondary-stories" style="display: flex; flex-wrap: wrap; gap: 2rem; margin-bottom: 3rem;">

  {% for story in secondary %}
  <div style="flex: 1 1 300px; min-width: 280px;">

    <img src="{{ story.header.image }}" alt="{{ story.title }}" style="width: 100%; border-radius: 6px; margin-bottom: 1rem;">

    <h3 style="margin-top: 0;">{{ story.title }}</h3>
    <p>{{ story.excerpt }}</p>
    <a href="{{ story.url }}" class="btn btn--small">Read →</a>

  </div>
  {% endfor %}

</div>
{% endif %}

---

<!-- ========================= -->
<!--  SECTION BLOCKS           -->
<!-- ========================= -->

## Ledger File
{% assign ledger = site.categories.ledger-file | first %}
A structured, evidence‑driven breakdown of a single issue or public decision.  
{% if ledger %}
**Latest:** [{{ ledger.title }}]({{ ledger.url }})  
{% endif %}
[Visit Ledger File →](/ledger-file/)

---

## People’s Brief
{% assign brief = site.categories.peoples-brief | first %}
Concise, high‑signal summaries of what the public needs to know — fast.  
{% if brief %}
**Latest:** [{{ brief.title }}]({{ brief.url }})  
{% endif %}
[Visit People’s Brief →](/peoples-brief/)

---

## Investigations
{% assign investigations = site.categories.investigations | first %}
Deep, methodical reporting on systems, institutions, and public decisions.  
{% if investigations %}
**Latest:** [{{ investigations.title }}]({{ investigations.url }})  
{% endif %}
[Visit Investigations →](/investigations/)

---

## Editorials
{% assign editorials = site.categories.editorials | first %}
Considered viewpoints grounded in evidence and written to elevate public understanding.  
{% if editorials %}
**Latest:** [{{ editorials.title }}]({{ editorials.url }})  
{% endif %}
[Visit Editorials →](/editorials/)

---

## Projects
{% assign projects = site.categories.projects | first %}
Long‑term civic research, data work, and public‑interest initiatives.  
{% if projects %}
**Latest:** [{{ projects.title }}]({{ projects.url }})  
{% endif %}
[Visit Projects →](/projects/)
