---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default

---
<div class="timeline">
  {% for job in site.data.work_history %}
  <div class="timeline-item">
    <div class="timeline-date">
      <span>{{ job.start_date }}</span> - <span>{{ job.end_date }}</span>
    </div>
    <div class="timeline-content">
      <img src="{{ job.logo }}" alt="{{ job.company }} logo" class="company-logo">
      <div class="details">
        <h3>{{ job.role }}</h3>
        <h4>{{ job.company }}</h4>
        <p>{{ job.description }}</p>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
