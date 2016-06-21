---
layout: post
title: ReadyNAS Apps
---

<div class="card-parent">
{% for rnapp in site.data.readynas_apps %}
  <div class="card">
    <img class="rn-icon" src="{{ rnapp.rn_img }}" alt="" />
    <h2 class="rn-name">{{ rnapp.name }}</h2>
    <p class="app-date">{{ rnapp.date }}</p>
    <p class="desc">{{ rnapp.desc }}</p>
    <div class="app_info">
      <a class="card-link" href="{{ rnapp.app_info }}">More Info</a>
      <a class="card-link" href="{{ rnapp.pkg_info }}">Package Info</a>
    </div>
    <div class="app_downloads">
      <br/>Download:
      {% if rnapp.dl_x86 contains 'amd64' %}
        <a class="card-link" href="{{ rnapp.dl_x86 }}">x86</a>
      {% endif %}
      {% if rnapp.dl_arm contains 'arm' %}
        <a class="card-link" href="{{ rnapp.dl_arm }}">arm</a>
      {% endif %}
      {% if rnapp.dl_all != 'false' %}
        <a class="card-link" href="{{ rnapp.dl_all }}">all</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>
