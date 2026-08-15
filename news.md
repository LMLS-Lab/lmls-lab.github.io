---
layout: default
title: News
permalink: /news/
---
<section class="section">
  <div class="wrap">
    <div class="section__head">
      <h1>News</h1>
    </div>

    {% assign items = site.news | sort: "date" | reverse %}
    {% if items.size > 0 %}
      <ul class="news-list">
        {% for item in items %}
        <li class="news-list__item">
          <time datetime="{{ item.date | date_to_xmlschema }}">{{ item.date | date: "%b %-d, %Y" }}</time>
          <span><a href="{{ item.url | relative_url }}">{{ item.title }}</a></span>
        </li>
        {% endfor %}
      </ul>
    {% else %}
      <p class="prose">No news yet — check back soon.</p>
    {% endif %}
  </div>
</section>
