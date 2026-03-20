---
layout: default
title: 首頁
---
<h1>最新文章</h1>
{% for post in site.posts %}
<div class="post-item">
  <a class="article-link" href="{{ post.url }}">{{ post.title }}</a>
  <div class="post-date">{{ post.date | date: "%Y-%m-%d" }}</div>
  <div class="tags">
    {% for tag in post.tags %}
      <a href="/tags/{{ tag | slugify }}/">#{{ tag }}</a>
    {% endfor %}
  </div>
</div>
{% endfor %}
