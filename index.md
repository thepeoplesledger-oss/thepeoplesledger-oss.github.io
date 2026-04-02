---
layout: single
classes: wide
title: "The People’s Ledger"
---

<!-- Featured Story (Optional) -->
{% assign featured = site.posts | first %}
{% if featured %}
## Featured Story
[{{ featured.title }}]({{ featured.url }})
{: .text-large }

{{ featured.excerpt }}

[Read more →]({{ featured.url }})
{: .btn .btn--primary }
{% endif %}

---

## Ledger File
{% assign ledger = site.categories.ledger-file | first %}
{% if ledger %}
### [{{ ledger.title }}]({{ ledger.url }})
{{ ledger.excerpt }}

[View all Ledger File →](/ledger-file/)
{% endif %}

---

## People’s Brief
{% assign brief = site.categories.peoples-brief | first %}
{% if brief %}
### [{{ brief.title }}]({{ brief.url }})
{{ brief.excerpt }}

[View all People’s Brief →](/peoples-brief/)
{% endif %}

---

## Investigations
{% assign investigations = site.categories.investigations | first %}
{% if investigations %}
### [{{ investigations.title }}]({{ investigations.url }})
{{ investigations.excerpt }}

[View all Investigations →](/investigations/)
{% endif %}

---

## Editorials
{% assign editorials = site.categories.editorials | first %}
{% if editorials %}
### [{{ editorials.title }}]({{ editorials.url }})
{{ editorials.excerpt }}

[View all Editorials →](/editorials/)
{% endif %}

---

## Projects
{% assign projects = site.categories.projects | first %}
{% if projects %}
### [{{ projects.title }}]({{ projects.url }})
{{ projects.excerpt }}

[View all Projects →](/projects/)
{% endif %}
