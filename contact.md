---
layout: default
title: Contact
permalink: /contact/
group_photo_folder: /assets/images/group/
---
<section class="section">
  <div class="wrap">
    <div class="section__head">
      <h1>Contact</h1>
    </div>

    <div class="contact-grid">
      <div class="prose">
        <p><h2>Address</h2>
        {{ site.address }}</p>
        <p><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
      </div>

      <div class="prose">
        <h2>Prospective Students</h2>
        <p>We currently have NO open positions for international students. Good luck to your career path.</p><br>
        <p>우리 연구실은 딥러닝 이론, 분산/연합학습, 신경망 경량화를 연구합니다. 딥러닝을 깊이있게 연구하고자 하는 학생들에게 언제든지 열려있습니다. 이메일로 문의 바랍니다.</p>

        <!-- TODO: add admissions-cycle-specific notes, application links, or a map/directions here. -->
      </div>
    </div>
  </div>

  {% comment %}
    Collect all group photos.
  {% endcomment %}
  {% capture photo_list %}{% for f in site.static_files %}{% if page.group_photo_folder and f.path contains page.group_photo_folder %}{% assign ext = f.extname | downcase %}{% if ext == ".jpg" or ext == ".jpeg" or ext == ".png" or ext == ".webp" %}{{ f.path | relative_url }}|{% endif %}{% endif %}{% endfor %}{% endcapture %}
  
  {% assign photos = photo_list | split: "|" %}
  
  <div class="wrap">
    <section class="contact-photos">
      <h2>
        Photos
        <small>(Random moments from LMLS Lab!)</small>
      </h2>
  
      {% if photos.size > 0 %}
      <figure class="group-photo">
        <img id="group-photo"
             alt="LMLS Lab members"
             data-photos="{{ photo_list }}">
        <noscript>
          <img src="{{ photos[0] }}" alt="LMLS Lab members">
        </noscript>
      </figure>
  
      <script>
        (function () {
          var img = document.getElementById("group-photo");
          var list = img.getAttribute("data-photos")
                        .split("|")
                        .filter(Boolean);
          img.src = list[Math.floor(Math.random() * list.length)];
        })();
      </script>
      {% endif %}
  
    </section>
  </div>
</section>
