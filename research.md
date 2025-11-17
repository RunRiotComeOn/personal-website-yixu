---
layout: page
title: Research Experience
description: My research positions and contributions
---

<div class="research-list">
  {% for exp in site.data.research %}
    <div class="research-item">
      <h3 class="position-title">{{ exp.position }}</h3>
      <p class="institution">{{ exp.institution }} &mdash; {{ exp.group | markdownify | remove: '<p>' | remove: '</p>' | strip }}</p>
      {% if exp.location %}
        <p class="location">{{ exp.location }}</p>
      {% endif %}
      <p class="dates">{{ exp.start_year }} &ndash; {{ exp.end_year }}</p>

      <div class="research-description">
        {{ exp.description | markdownify }}
      </div>
    </div>

    {% unless forloop.last %}
      <hr class="research-divider">
    {% endunless %}
  {% endfor %}
</div>
