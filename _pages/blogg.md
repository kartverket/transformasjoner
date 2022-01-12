---
layout: page
title: Nyheter
order: 3
permalink: /_posts/
---
<ul>
  {% for post in site.posts  limit:5 %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }}: {{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

