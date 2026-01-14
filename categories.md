---
layout: page
title: 分类
permalink: /categories/
---

{% assign cats = site.categories | sort %}
{% for c in cats %}
## {{ c[0] }}（{{ c[1].size }}）
<ul>
  {% for post in c[1] %}
    <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endfor %}
