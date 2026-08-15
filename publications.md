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

    {% assign pubs = site.publications | sort: "year" | reverse %}
    {% assign years = pubs | map: "year" | uniq | sort | reverse %}

    {% if pubs.size > 0 %}
      {% for year in years %}
        {% assign year_pubs = pubs | where: "year", year %}
        <div class="people-group">
          <h2>{{ year }}</h2>
          <ul class="publication-list">
            {% for pub in year_pubs %}
            <li class="publication-list__item">
              <span class="publication-list__title"><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></span>
              <span class="publication-list__meta">{{ pub.authors }} — {{ pub.venue }}</span>
            </li>
            {% endfor %}
          </ul>
        </div>
      {% endfor %}
    {% else %}
      <p class="prose">No publications listed yet.</p>
    {% endif %}
  </div>
</section>
