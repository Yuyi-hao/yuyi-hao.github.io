---
layout: page
title: Projects
icon: fas fa-briefcase
order: 1
---

Everything I've built, grouped by type. Jump to:
{% for cat in site.data.project_categories -%}
{%- assign count = site.data.projects_list | where: "category", cat.id | size -%}
{%- if count > 0 %} [{{ cat.name }}](#{{ cat.id }}){% unless forloop.last %} ·{% endunless %}{% endif -%}
{%- endfor %} · [Learning & Practice](#learning)

{% for cat in site.data.project_categories %}
{% assign items = site.data.projects_list | where: "category", cat.id %}
{% if items.size > 0 %}
<h2 id="{{ cat.id }}" class="mt-5"><i class="{{ cat.icon }} fa-fw me-1"></i> {{ cat.name }}</h2>
<p class="text-muted">{{ cat.description }}{% if cat.id == "extensions" %} <a href="{{ '/extensions/' | relative_url }}">Go to downloads →</a>{% endif %}</p>

<div class="row row-cols-1 row-cols-md-2 g-4 mb-4">
  {% for project in items %}
  <div class="col">
    {% include project_card.html project=project %}
  </div>
  {% endfor %}
</div>
{% endif %}
{% endfor %}

<h2 id="learning" class="mt-5"><i class="fas fa-book fa-fw me-1"></i> Learning &amp; Practice</h2>
<p class="text-muted">Coursework, exercises and problem sets.</p>

<ul>
{% for r in site.data.learning_repos %}
  <li><a href="{{ r.repo }}" target="_blank" rel="noopener noreferrer">{{ r.name }}</a> <span class="text-muted small">· {{ r.note }}</span></li>
{% endfor %}
</ul>

<p class="mt-4">
  More on <a href="https://github.com/yuyi-hao?tab=repositories" target="_blank" rel="noopener noreferrer">GitHub →</a>
</p>
