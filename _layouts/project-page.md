---
layout: page
---

<div class="project-page container my-5">

  <h1>{{ page.title }}</h1>

  {% if page.subtitle %}
    <h3 class="text-muted mb-4">{{ page.subtitle }}</h3>
  {% endif %}

  {% if page.image %}
    <img src="{{ page.image | relative_url }}" alt="{{ page.title }}" class="img-fluid rounded mb-4">
  {% endif %}

  <div class="project-content">
    {{ content }}
  </div>

</div>
