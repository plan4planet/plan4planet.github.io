---
layout: page
title: Tentative Schedule
permalink: /schedule/
toc: true
description: "The three-day program for Planning for a Better Planet, AAAI Fall Symposium 2026 (Nov 5–7, Arlington, VA): invited talks, paper sessions and community discussions."
---

<p class="schedule-note">Draft program, subject to change. Invited talks run 30 minutes plus 10 minutes of questions; accepted-paper talks run 10 minutes each. Speaker bios are on the <a href="{{ '/speakers/' | relative_url }}">speakers page</a> and paper authors on the <a href="{{ '/papers/' | relative_url }}">papers page</a>.</p>

{% for day in site.data.schedule %}
<h3 id="{{ day.id }}"><span class="schedule-day">{{ day.day }}:</span> {{ day.date }}</h3>
<ol class="schedule">
  {%- for slot in day.slots %}
  <li class="schedule-slot{% unless slot.items %} schedule-break{% endunless %}" id="{{ day.id }}-{{ slot.time | split: '–' | first | remove: ':' }}">
    <span class="schedule-time">{{ slot.time }}</span>
    <div class="schedule-session">
      <h4>{{ slot.title }}</h4>
      {%- if slot.subtitle %}
      <p class="schedule-subtitle">{{ slot.subtitle }}</p>
      {%- endif %}
      {%- if slot.items %}
      <ul class="schedule-items">
        {%- for item in slot.items %}
        <li>
          {{ item.label }}{% if item.speaker %}: <a href="{{ '/speakers/' | relative_url }}">{{ item.speaker }}</a>{% endif %}
          {%- if item.talk %}
          <span class="schedule-talk">“{{ item.talk }}”</span>
          {%- endif %}
          {%- if item.papers %}
          <ul class="schedule-papers">
            {%- for paper in item.papers %}
            {%- assign paper_number = nil %}
            {%- for section in site.data.papers %}{% for accepted in section.papers %}{% if accepted.title == paper.title %}{% assign paper_number = accepted.number %}{% endif %}{% endfor %}{% endfor %}
            <li><span class="schedule-paper-title">{% if paper_number %}<a href="{{ '/papers/' | relative_url }}#paper-{{ paper_number }}">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</span> <span class="schedule-paper-authors">{{ paper.authors }}</span></li>
            {%- endfor %}
          </ul>
          {%- endif %}
        </li>
        {%- endfor %}
      </ul>
      {%- endif %}
      {%- if slot.prompts %}
      <details class="schedule-prompts">
        <summary>Example discussion questions</summary>
        <ul>
          {%- for prompt in slot.prompts %}
          <li>{{ prompt }}</li>
          {%- endfor %}
        </ul>
      </details>
      {%- endif %}
    </div>
  </li>
  {%- endfor %}
</ol>
{% endfor %}
