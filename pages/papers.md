---
layout: page
title: Accepted Papers
permalink: /papers/
toc: true
---

{% for section in site.data.papers %}
<h3 id="{{ section.id }}">{{ section.heading }}</h3>
<ul class="paper-list">
  {%- for paper in section.papers %}
  <li id="paper-{{ paper.number }}">
    <strong>{{ paper.title | escape }}</strong><br>
    {{ paper.authors | escape }}
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
