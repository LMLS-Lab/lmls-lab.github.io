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

    {% if pubs.size > 0 %}
      <ul class="publication-list">
        {% for pub in pubs %}
        {% assign authors_html = pub.authors | replace: "Sunwoo Lee", "<strong>Sunwoo Lee</strong>" %}
        <li class="publication-list__item">
          <div class="publication-list__body">
            <span class="publication-list__title">
              <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>{% if pub.note %} <span class="pub-note">{{ pub.note }}</span>{% endif %}
            </span>
            <span class="publication-list__meta">{{ authors_html }} — <strong class="publication-list__venue">{{ pub.venue }}</strong></span>
          </div>
          <span class="publication-list__year">{{ pub.year }}</span>
        </li>
        {% endfor %}
      </ul>
    {% else %}
      <p class="prose">No publications listed yet.</p>
    {% endif %}
  </div>
</section>
