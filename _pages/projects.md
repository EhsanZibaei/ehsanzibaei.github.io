---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-page">
  <header class="projects-intro">
    <p class="projects-eyebrow">Selected work</p>
    <h1>Projects &amp; experience</h1>
    <p>A selection of research and engineering work across robotics, autonomous systems, and applied AI.</p>
  </header>

  {% for career in site.data.career %}
    {% assign career_projects = site.projects | where: "listing_period", career.project_period %}
    <section class="project-period">
      <h2>{{ career.heading }}</h2>
      {% if career.description %}
        <p class="project-period-description">{{ career.description }}</p>
      {% endif %}
      {% if career.highlights %}
        <ul class="career-highlights">
          {% for highlight in career.highlights %}
            <li>{{ highlight }}</li>
          {% endfor %}
        </ul>
      {% endif %}
      {% if career_projects.size > 0 %}
        {% include project-cards.html period=career.project_period %}
      {% endif %}
    </section>
  {% endfor %}
</div>
