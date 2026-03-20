---
layout: default
title: 搜尋
---

<input id="searchInput" placeholder="搜尋文章..." style="width:100%;padding:10px">

<ul id="results"></ul>

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
  const results = posts.filter(p => p.title.toLowerCase().includes(keyword));

  document.getElementById('results').innerHTML =
    results.map(p => `<li><a href="${p.url}">${p.title}</a></li>`).join('');
});
</script>
