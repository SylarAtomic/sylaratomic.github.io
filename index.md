---
layout: default
title: Home
---

<div class="fade-in-up">
  <h1>Welcome to My Site</h1>
  <p class="lead">A beautiful dark-themed Jekyll site built for GitHub Pages.</p>
  
  <div class="card">
    <h2>About This Theme</h2>
    <p>This is a clean, modern dark theme featuring a beautiful color palette of dark blues, purples, and white. Perfect for portfolios, blogs, and project showcases.</p>
    <a href="#" class="btn">Learn More</a>
  </div>
</div>

{% if site.posts.size > 0 %}
<div class="fade-in-up">
  <h2>Latest Posts</h2>
  <ul class="post-list">
    {% for post in site.posts limit:3 %}
    <li class="post-item">
      <h3 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h3>
      <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </li>
    {% endfor %}
  </ul>
</div>
{% endif %}