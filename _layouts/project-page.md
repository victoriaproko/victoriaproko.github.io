---
layout: page
---

<div class="project-hero container my-5">

  <!-- Title + Subtitle -->
  <h1 class="display-4">{{ page.title }}</h1>

  {% if page.short_description %}
    <p class="lead text-muted">{{ page.short_description }}</p>
  {% endif %}

  <!-- Optional metadata row -->
  <div class="row my-4">
    {% if page.role %}
    <div class="col-md-4">
      <h6 class="text-uppercase text-muted mb-1">Role</h6>
      <p>{{ page.role }}</p>
    </div>
    {% endif %}

    {% if page.tools %}
    <div class="col-md-4">
      <h6 class="text-uppercase text-muted mb-1">Tools</h6>
      <p>{{ page.tools }}</p>
    </div>
    {% endif %}

    {% if page.timeline %}
    <div class="col-md-4">
      <h6 class="text-uppercase text-muted mb-1">Timeline</h6>
      <p>{{ page.timeline }}</p>
    </div>
    {% endif %}
  </div>

  <!-- Featured Image -->
  {% if page.image %}
    <img src="{{ page.image | relative_url }}" alt="{{ page.title }}" class="img-fluid rounded shadow-sm mb-5">
  {% endif %}
</div>


<!-- CONTENT BODY -->
<div class="project-body container">

  <div class="project-content mb-5">
    {{ content }}
  </div>

  <!-- Back to Projects -->
  <div class="text-center my-5">
    <a href="/projects/" class="btn btn-outline-primary px-4 py-2">
      ← Back to Projects
    </a>
  </div>

</div>
