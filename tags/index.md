---
title: 标签
layout: page
permalink: tags.html
image: /public/images/skyline.jpg
order: 1
---

<div class="taxonomy-cloud" aria-label="全部标签">
{% for tag in site.tags %}
  <a href="#{{ tag[0] | escape }}">#{{ tag[0] }} <span>{{ tag[1].size }}</span></a>
{% endfor %}
</div>

<ul class="listing">
{% for tag in site.tags %}
  <li class="listing-seperator" id="{{ tag[0] | escape }}">{{ tag[0] }}</li>
  {% for post in tag[1] %}
  <li class="listing-item">
    <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%Y-%m-%d' }}</time>
    <a href="{{ post.url | relative_url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
  {% endfor %}
{% endfor %}
</ul>
