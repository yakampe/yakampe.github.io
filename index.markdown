---
layout: default
---

<div class="timeline">
  {% for job in site.data.work_history %}
  <div class="timeline-item">
    <div class="timeline-date">
      <img src="{{ job.logo }}" alt="{{ job.company }} logo" class="company-logo">
    </div>
    <div class="timeline-content">
      <div class="details">
        <span>{{ job.start_date }}</span> - <span>{{ job.end_date }}</span>
        <h3>{{ job.role }}</h3>
        <h4>{{ job.company }}</h4>
        <p>{{ job.description }}</p>
      </div>
    </div>
  </div>
  {% endfor %}
</div>