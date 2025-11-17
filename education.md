---
layout: page
title: Education
description: My academic background and qualifications
---

<div class="timeline">
  {% for edu in site.data.education %}
    <div class="timeline-item">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
        <h3 class="degree-title">{{ edu.degree }}</h3>
        <p class="institution">{{ edu.institution }}</p>
        {% if edu.location %}
          <p class="location">{{ edu.location }}</p>
        {% endif %}
        <p class="dates">{{ edu.start_year }} &ndash; {{ edu.end_year }}</p>

        {% if edu.notes %}
          <p class="notes">{{ edu.notes }}</p>
        {% endif %}

        {% if edu.gpa %}
          <p class="gpa"><strong>GPA:</strong> {{ edu.gpa }}</p>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>
