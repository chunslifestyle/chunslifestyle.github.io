---
layout: default
title: 搜尋
---

<div style="max-width:700px;margin:60px auto;">
  <h1>搜尋文章</h1>

  <input id="searchInput" placeholder="輸入關鍵字..." 
    style="width:100%;padding:12px;margin-top:20px;border:1px solid #ddd;border-radius:8px;">

  <ul id="results" style="margin-top:30px;"></ul>
</div>

<script>
const posts = [
  {% for post in site.posts %}
    {
      title: "{{ post.title }}",
      url: "{{ post.url }}"
    },
  {% endfor %}
];

document.getElementById('searchInput').addEventListener('input', function() {
  const keyword = this.value.toLowerCase();

  const results = posts.filter(p =>
    p.title.toLowerCase().includes(keyword)
  );

  document.getElementById('results').innerHTML =
    results.map(p => `<li><a href="${p.url}">${p.title}</a></li>`).join('');
});
</script>
