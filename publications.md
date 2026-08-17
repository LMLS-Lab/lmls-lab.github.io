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

    {% comment %} Grouped by the "type" front-matter field (conference | journal | preprint | workshop). {% endcomment %}
    {% assign types = "conference|journal|workshop|preprint" | split: "|" %}
    {% assign type_labels = "Conference Papers|Journal Articles|Workshop Papers|Preprints" | split: "|" %}

    {% assign has_any = false %}
    {% for pub in site.publications %}{% assign has_any = true %}{% endfor %}

    {% if has_any %}
      {% for type in types %}
        {% assign label = type_labels[forloop.index0] %}
        {% assign pubs = site.publications | where: "type", type | sort: "year" | reverse %}
        {% if pubs.size > 0 %}
        <div class="people-group">
          <h2>{{ label }}</h2>
          <ul class="publication-list">
            {% assign prev_year = "" %}
            {% for pub in pubs %}
            {% assign authors_html = pub.authors | replace: "Sunwoo Lee", "<strong>Sunwoo Lee</strong>" %}
            <li class="publication-list__item">
              <div class="publication-list__body">
                <span class="publication-list__title">
                  <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>{% if pub.note %} <span class="pub-note">{{ pub.note }}</span>{% endif %}
                </span>
                <span class="publication-list__meta">{{ authors_html }} — <strong class="publication-list__venue">{{ pub.venue }}</strong></span>
              </div>
              {% if pub.year != prev_year %}
              <span class="publication-list__year">{{ pub.year }}</span>
              {% assign prev_year = pub.year %}
              {% else %}
              <span class="publication-list__year"></span>
              {% endif %}
            </li>
            {% endfor %}
          </ul>
        </div>
        {% endif %}
      {% endfor %}
    {% else %}
      <p class="prose">No publications listed yet.</p>
    {% endif %}
  </div>
</section>
