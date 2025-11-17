---
layout: page
title: Contact
description: Get in touch with me
---

<div class="contact-intro">
  <p>
    I am always interested in discussing research collaborations, potential projects,
    or opportunities in {{ site.description | split: "," | first | downcase }}.
    Please feel free to reach out via any of the following channels:
  </p>
</div>

<div class="contact-methods">
  <div class="contact-item">
    <h3>Email</h3>
    <p>
      <a href="mailto:{{ site.email }}">{{ site.email }}</a>
    </p>
    <p class="contact-note">
      I typically respond within 24-48 hours on business days.
    </p>
  </div>

  {% if site.google_scholar %}
  <div class="contact-item">
    <h3>Google Scholar</h3>
    <p>
      <a href="https://scholar.google.com/citations?user={{ site.google_scholar }}" target="_blank" rel="noopener">
        View my research profile
      </a>
    </p>
    <p class="contact-note">
      See my latest publications and citation metrics.
    </p>
  </div>
  {% endif %}

  {% if site.linkedin %}
  <div class="contact-item">
    <h3>LinkedIn</h3>
    <p>
      <a href="https://linkedin.com/in/{{ site.linkedin }}" target="_blank" rel="noopener">
        Connect with me professionally
      </a>
    </p>
    <p class="contact-note">
      For professional networking and career updates.
    </p>
  </div>
  {% endif %}

  {% if site.github %}
  <div class="contact-item">
    <h3>GitHub</h3>
    <p>
      <a href="https://github.com/{{ site.github }}" target="_blank" rel="noopener">
        View my code repositories
      </a>
    </p>
    <p class="contact-note">
      Explore my open-source projects and contributions.
    </p>
  </div>
  {% endif %}

  {% if site.orcid %}
  <div class="contact-item">
    <h3>ORCID</h3>
    <p>
      <a href="https://orcid.org/{{ site.orcid }}" target="_blank" rel="noopener">
        {{ site.orcid }}
      </a>
    </p>
    <p class="contact-note">
      My unique researcher identifier.
    </p>
  </div>
  {% endif %}
</div>

<hr class="decorative-divider">

<div class="office-info">
  <h3>Office Location</h3>
  <p>
    [Your Department Name]<br>
    [Your University/Institution]<br>
    [Building Name, Room Number]<br>
    [Street Address]<br>
    [City, State ZIP]
  </p>
  <p class="contact-note">
    Please email to schedule an in-person meeting or office hours.
  </p>
</div>
