---
layout: default
title: Chun｜Portfolio & Blog
---

<div style="max-width:900px;margin:60px auto;font-family:-apple-system,system-ui;">

  <h1 style="font-size:48px;margin-bottom:10px;">Chun</h1>
  <p style="color:#666;font-size:18px;">
    分享生活、想法與創作 ✨<br>
    Developer / Creator / Thinker
  </p>

  <h2 style="margin-top:50px;">最新文章</h2>

  {% for post in site.posts %}
    <div style="margin:20px 0;border-bottom:1px solid #eee;padding-bottom:15px;">
      <a href="{{ post.url }}" style="text-decoration:none;color:black;">
        <div style="font-size:22px;font-weight:600;">
          {{ post.title }}
        </div>
      </a>
      <div style="color:#999;font-size:14px;">
        {{ post.date | date: "%Y-%m-%d" }}
      </div>
    </div>
  {% endfor %}

</div>
