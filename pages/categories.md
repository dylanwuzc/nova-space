---
layout: page
title: 分类
description: 按主题分类浏览
keywords: 分类, categories
comments: false
permalink: /categories/
---

{% assign sorted_categories = site.categories | sort %}

{% for category in sorted_categories %}
## {{ category[0] }}

<ul>
{% for post in category[1] %}
  <li>
    <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    <span style="color: #666; font-size: 0.85rem;">({{ post.date | date: "%Y-%m-%d" }})</span>
  </li>
{% endfor %}
</ul>
{% endfor %}
