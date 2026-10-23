---
layout: default
title: Publications
permalink: /publications/
---
<section class="section">
  <div class="wrap">
    <div class="section__head">
      <h1>Publications</h1>
    </div>

    {% comment %}
      Grouped by year (newest first), then by the "type" front-matter field
      (conference | journal | workshop | preprint).
    {% endcomment %}
    {% assign types = "conference|journal|workshop|preprint" | split: "|" %}
    {% assign type_labels = "Conference Papers|Journal Articles|Workshop Papers|Preprints" | split: "|" %}
    {% assign years = site.publications | sort: "year" | reverse | group_by: "year" %}

    {% if site.publications.size > 0 %}
    <div class="pubs">
      {% for year in years %}
      <div class="pubs__year">
        <h2 class="pubs__year-label">{{ year.name }}</h2>
        <div class="pubs__groups">
          {% for type in types %}
            {% assign group = year.items | where: "type", type %}
            {% if group.size > 0 %}
          <section class="pubs__group">
            <h3 class="pubs__group-title">{{ type_labels[forloop.index0] }}</h3>
            <ul class="pubs__list">
              {% for pub in group %}
              <li class="pub">
                <h4 class="pub__title">
                  <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>{% if pub.note and pub.note != "" %} <span class="pub-note">{{ pub.note }}</span>{% endif %}
                </h4>
                <p class="pub__authors">{{ pub.authors | replace: "Sunwoo Lee", "<strong>Sunwoo Lee</strong>" }}</p>
                <p class="pub__venue">{{ pub.venue }} · {{ pub.year }}</p>
                {% capture links %}
                  {% if pub.arxiv %}<li><a href="{{ pub.arxiv }}" target="_blank" rel="noopener">arXiv</a></li>{% endif %}
                  {% if pub.openreview %}<li><a href="{{ pub.openreview }}" target="_blank" rel="noopener">OpenReview</a></li>{% endif %}
                  {% if pub.pdf %}<li><a href="{{ pub.pdf }}" target="_blank" rel="noopener">PDF</a></li>{% endif %}
                  {% if pub.doi %}<li><a href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">DOI</a></li>{% endif %}
                  {% if pub.project %}<li><a href="{{ pub.project }}" target="_blank" rel="noopener">Project</a></li>{% endif %}
                  {% if pub.code %}<li><a href="{{ pub.code }}" target="_blank" rel="noopener">Code</a></li>{% endif %}
                {% endcapture %}
                {% assign links = links | strip %}
                {% if links != "" %}<ul class="pub__links">{{ links }}</ul>{% endif %}
              </li>
              {% endfor %}
            </ul>
          </section>
            {% endif %}
          {% endfor %}
        </div>
      </div>
      {% endfor %}
    </div>
    {% else %}
      <p class="prose">No publications listed yet.</p>
    {% endif %}
  </div>
</section>
