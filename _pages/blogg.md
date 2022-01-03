---
layout: post
title: Blogg
order: 13
permalink: /_posts/
---
<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }}: {{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

