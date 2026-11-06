---
layout: page
title: Accepted Papers
permalink: /papers/
toc: true
description: "Accepted papers at the AAAI Fall Symposium on Planning for a Better Planet: climate adaptation, disaster response, policy, environmental monitoring and energy."
---

{% for section in site.data.papers %}
<h3 id="{{ section.id }}">{{ section.heading }}</h3>
<ul class="paper-list">
  {%- for paper in section.papers %}
  <li id="paper-{{ paper.number }}">
    <strong>{{ paper.title | escape }}</strong>
    {%- if paper.pdf %}
    {%- if paper.pdf contains '://' %}{% assign pdf_url = paper.pdf %}{% else %}{% assign pdf_url = '/assets/papers/' | append: paper.pdf | relative_url %}{% endif %}
    <a class="paper-pdf" href="{{ pdf_url }}" target="_blank" rel="noopener noreferrer"><i class="fa-solid fa-file-lines" aria-hidden="true"></i> Preprint</a>
    {%- endif %}
    {%- if paper.related %}
    <a class="paper-pdf" href="{{ paper.related }}" target="_blank" rel="noopener noreferrer"><i class="fa-solid fa-link" aria-hidden="true"></i> Related paper</a>
    {%- endif %}<br>
    {{ paper.authors | escape }}
    {%- assign session = nil %}
    {%- for day in site.data.schedule %}{% for slot in day.slots %}{% for item in slot.items %}{% for scheduled in item.papers %}{% if scheduled.title == paper.title %}{% assign session = slot %}{% assign session_day = day %}{% endif %}{% endfor %}{% endfor %}{% endfor %}{% endfor %}
    {%- if session %}
    <a class="paper-session" href="{{ '/schedule/' | relative_url }}#{{ session_day.id }}-{{ session.time | split: '–' | first | remove: ':' }}">{{ session_day.date | split: ',' | first }}, {{ session.time }} · {{ session.title }}</a>
    {%- endif %}
    {%- if paper.abstract %}
    <details class="abstract paper-abstract">
      <summary>Abstract</summary>
      <blockquote>{{ paper.abstract | markdownify }}</blockquote>
    </details>
    {%- endif %}
  </li>
  {%- endfor %}
</ul>
{% endfor %}
