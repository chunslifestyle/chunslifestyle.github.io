---
layout: default
title: Chun｜Portfolio & Blog
---

<style>
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto;
}

.container {
  max-width: 900px;
  margin: 60px auto;
}

.hero {
  margin-bottom: 60px;
}

.name {
  font-size: 48px;
  font-weight: 700;
}

.bio {
  color: #666;
  margin-top: 10px;
  font-size: 18px;
}

.section-title {
  font-size: 24px;
  margin-bottom: 20px;
}

.card {
  display: flex;
  gap: 20px;
  text-decoration: none;
  color: black;
  border-bottom: 1px solid #eee;
  padding: 20px 0;
  transition: 0.2s;
}

.card:hover {
  transform: translateY(-4px);
}

.card img {
  width: 160px;
  height: 100px;
  object-fit: cover;
  border-radius: 10px;
}

.card-title {
  font-size: 20px;
  font-weight: 600;
}

.card-date {
  color: #999;
  font-size: 14px;
  margin-top: 6px;
}
</style>

<div class="container">

  <!-- 個人介紹 -->
  <div class="hero">
    <div class="name">Chun</div>
    <div class="bio">
      分享生活、想法與創作 ✨<br>
      Developer / Creator / Thinker
    </div>
  </div>

  <!-- 部落格 -->
  <div class="section-title">最新文章</div>

  {% for post in site.posts %}
  <a class="card" href="{{ post.url }}">
    {% if post.image %}
      <img src="{{ post.image }}">
    {% endif %}
    <div>
      <div class="card-title">{{ post.title }}</div>
      <div class="card-date">{{ post.date | date: "%Y-%m-%d" }}</div>
    </div>
  </a>
  {% endfor %}

</div>
