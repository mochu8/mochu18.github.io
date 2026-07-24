---
title: 分类
layout: page
permalink: categories.html
image: /public/images/skyline.jpg
order: 2
---

<div class="taxonomy-cloud" aria-label="全部分类">
{% for cat in site.categories %}
  <a href="#{{ cat[0] | escape }}">{{ cat[0] }} <span>{{ cat[1].size }}</span></a>
{% endfor %}
</div>

<ul class="listing">
{% for cat in site.categories %}
  <li class="listing-seperator" id="{{ cat[0] | escape }}">{{ cat[0] }}</li>
  {% for post in cat[1] %}
  <li class="listing-item">
    <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%Y-%m-%d' }}</time>
    <a href="{{ post.url | relative_url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
  {% endfor %}
{% endfor %}
</ul>
