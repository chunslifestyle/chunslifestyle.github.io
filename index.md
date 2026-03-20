---
layout: default
title: 淳粹生活 Chunslifestyle
---

<style>
.container {
  max-width: 700px;
  margin: 60px auto;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto;
}

.title {
  font-size: 42px;
  font-weight: 700;
  margin-bottom: 10px;
}

.subtitle {
  color: #777;
  margin-bottom: 40px;
}

.post {
  padding: 20px 0;
  border-bottom: 1px solid #eee;
}

.post a {
  text-decoration: none;
  color: black;
}

.post-title {
  font-size: 24px;
  font-weight: 600;
}

.post-date {
  color: #999;
  font-size: 14px;
  margin-top: 5px;
}
</style>

<div class="container">
  <div class="title">淳粹生活</div>
  <div class="subtitle">分享生活、想法與靈感</div>

  {% for post in site.posts %}
  <div class="post">
    <a href="{{ post.url }}">
      <div class="post-title">{{ post.title }}</div>
    </a>
    <div class="post-date">{{ post.date | date: "%Y-%m-%d" }}</div>
  </div>
  {% endfor %}
</div>
