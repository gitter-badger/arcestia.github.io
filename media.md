---
title: Media
layout: default
permalink: /media/
id: /media
---
{% if site.github.url %}
  {% assign url_base = site.github.url %}
{% else %}
  {% assign url_base = site.url %}
{% endif %}
<ul class="media">
{% for page in site.media %}
  <li class="post">
    <div class="row">
        <div class="col-sm-9">
            <a href="{{ url_base }}{{ page.url }}">{% include smartify text=page.title %}</a>
        </div>
        <div class="col-sm-3 date">
            {{ page.date | date: '%B %d, %Y' }}
        </div>
    </div>
  </li>
{% endfor %}
</ul>