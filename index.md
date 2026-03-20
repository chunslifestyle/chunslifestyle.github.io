---
layout: default
title: 淳粹生活 Chunslifestyle
---

<style>
.container {
  max-width: 900px;
  margin: 60px auto;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto;
}

.header {
  margin-bottom: 50px;
}

.title {
  font-size: 42px;
  font-weight: 700;
}

.subtitle {
  color: #777;
  margin-top: 10px;
}

.grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 30px;
}

.card {
  display: flex;
  gap: 20px;
  text-decoration: none;
  color: black;
  border-bottom: 1px solid #eee;
  padding-bottom: 20px;
  transition: 0.2s;
}

.card:hover {
  transform: translateY(-3px);
}

.card img {
  width: 160px;
  height: 100px;
  object-fit: cover;
  border-radius: 8px;
}

.card-content {
  flex: 1;
}

.card-title {
  font-size: 22px;
  font-weight: 600;
}

.card-date {
  color: #999;
  margin-top: 8px;
  font-size: 14px;
}
</style>

<div class="container">
  <div class="header">
    <div class="title">淳粹生活</div>
    <div class="subtitle">分享生活、想法與靈感</div>
  </div>

  <div class="grid">
    {% for post in site.posts %}
    <a class="card" href="{{ post.url }}">
      {% if post.image %}
        <img src="{{ post.image }}">
      {% endif %}
      <div class="card-content">
        <div class="card-title">{{ post.title }}</div>
        <div class="card-date">{{ post.date | date: "%Y-%m-%d" }}</div>
      </div>
    </a>
    {% endfor %}
  </div>
</div>
  {% endfor %}
</div>
