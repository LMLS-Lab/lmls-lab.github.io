---
layout: default
title: People
permalink: /people/
---
<section class="section">
  <div class="wrap">
    <div class="section__head">
      <h1>People</h1>
    </div>

    {% comment %}
      Underlying data has 7 group values: faculty | postdoc | phd | ms | undergrad | external | alumni.
      On this page, "phd" and "ms" are displayed together under one "Graduate Students"
      section — the "grad" key below is a display-only bucket, not a real group value.
    {% endcomment %}
    {% assign groups = "faculty|postdoc|grad|undergrad|external|alumni" | split: "|" %}
    {% assign group_labels = "Faculty|Postdoctoral Researchers|Graduate Students|Undergraduate Students|External Researchers|Alumni" | split: "|" %}

    {% assign has_any = false %}
    {% for person in site.people %}{% assign has_any = true %}{% endfor %}

    {% if has_any %}
      {% for group in groups %}
        {% assign label = group_labels[forloop.index0] %}
        {% if group == "grad" %}
        {% assign phd_members = site.people | where: "group", "phd" %}
        {% assign ms_members = site.people | where: "group", "ms" %}
        {% assign members = phd_members | concat: ms_members | sort: "order" %}
        {% else %}
        {% assign members = site.people | where: "group", group | sort: "order" %}
        {% endif %}
        {% if members.size > 0 %}
        <div class="people-group">
          <h2>{{ label }}</h2>
          <div class="grid grid--4 people-grid">
            {% for person in members %}
            <a class="person-card" href="{{ person.url | relative_url }}">
              <div class="person-card__photo">
                {% if person.photo and person.photo != "" %}
                  <img src="{{ person.photo | relative_url }}" alt="Photo of {{ person.name }}">
                {% else %}
                  <span class="person-card__photo-placeholder">{{ person.name | slice: 0, 1 }}</span>
                {% endif %}
              </div>
              <div class="person-card__body">
                <div class="person-card__name">{{ person.name }}</div>
                <div class="person-card__role">{{ person.role }}</div>
              </div>
            </a>
            {% endfor %}
          </div>
        </div>
        {% endif %}
      {% endfor %}
    {% else %}
      <p class="prose">No members listed yet.</p>
    {% endif %}

    <div class="prose">
      <h2>Join the Lab</h2>
      <p>We're always happy to hear from motivated prospective students. See the
      <a href="/contact/">Contact</a> page for how to reach us.</p>
    </div>
  </div>
</section>
