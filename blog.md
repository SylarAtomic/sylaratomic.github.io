---
layout: default
title: Blog
---

<div class="fade-in-up">
  <h1>Blog</h1>
  <p class="lead">Here's everything I've written so far. Tips, tutorials, and thoughts from my development journey.</p>
  
  {% if site.posts.size > 0 %}
    <div class="posts-container">
      {% for post in site.posts %}
      <article class="post-item">
        <h2 class="post-title">
          <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
        <div class="post-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
          {% if post.categories.size > 0 %}
            <span class="post-categories">
              {% for category in post.categories %}
                <span class="category">{{ category }}</span>
              {% endfor %}
            </span>
          {% endif %}
        </div>
        <div class="post-excerpt">
          {{ post.excerpt | strip_html | truncatewords: 50 }}
        </div>
        <a href="{{ post.url | relative_url }}" class="read-more-btn">Read More →</a>
      </article>
      {% endfor %}
    </div>
  {% else %}
    <div class="no-posts">
      <p>No posts yet! Check back soon for updates on my game development journey.</p>
    </div>
  {% endif %}
</div>