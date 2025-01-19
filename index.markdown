---
layout: default
---

<div class="timeline">
  {% for job in site.data.work_history %}
  <div class="timeline-item" id="job-{{job.id}}">
    <div class="timeline-date">
      <img src="{{ job.logo }}" alt="{{ job.company }} logo" class="company-logo">
    </div>
    <div class="timeline-content">
      <div class="details">
        <span>{{ job.start_date }}</span> - <span>{{ job.end_date }}</span>
        <h3>{{ job.role }}</h3>
        <h4>{{ job.company }}</h4>
      </div>
    </div>
  </div>
  <div class="further-details" id="job-{{job.id}}">
    {{ job.description }}
  </div>
  {% endfor %}
</div>

<script>
  const timelineItems = document.querySelectorAll('.timeline-item');
const furtherDetails = document.querySelectorAll('.further-details');

let activeItem = null;

timelineItems.forEach((item) => {
  item.addEventListener('click', () => {
    // If the clicked item is the same as the active one, reset everything
    if (activeItem === item.id) {
      activeItem = null; // Clear the active item
      furtherDetails.forEach((otherItem) => {
        otherItem.classList.remove('show'); // Hide the further details
        otherItem.style.opacity = '0'; // Fade out
        otherItem.style.visibility = 'hidden'; // Hide element
      });

      timelineItems.forEach((otherItem) => {
        otherItem.style.opacity = '1'; // Reset opacity of all timeline items
      });
    } else {
      // If the clicked item is different, set it as active and show its details
      activeItem = item.id;

      furtherDetails.forEach((otherItem) => {
        if (otherItem.id !== item.id) {
          otherItem.classList.remove('show'); // Hide details of other items
          otherItem.style.opacity = '0'; // Fade out
          otherItem.style.visibility = 'hidden'; // Hide element
        } else {
          otherItem.classList.add('show'); // Show the clicked item's details
          otherItem.style.opacity = '1'; // Ensure it's visible
          otherItem.style.visibility = 'visible'; // Make it visible
        }
      });

      timelineItems.forEach((otherItem) => {
        if (otherItem.id !== item.id) {
          otherItem.style.opacity = '0.35'; // Dim other items
        } else {
          otherItem.style.opacity = '1'; // Keep the clicked item at full opacity
        }
      });
    }
  });
});

</script>