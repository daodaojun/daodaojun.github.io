---
layout: default
title: 文章分类
permalink: /categories/
---

# 文章分类

{% for category in site.categories %}
## {{ category[0] }}（{{ category[1].size }} 篇）

<ul>
{% for post in category[1] %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span>{{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
{% endfor %}
</ul>
{% endfor %}