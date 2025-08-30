---
layout: default
title: Blog
---

<div class="fade-in-up">
  <h1>Blog</h1>
  <p class="lead">Tips, tutorials, and insights from my game development journey. Everything I learn, I share here to help others on their creative paths.</p>
  
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
          {% if post.excerpt %}
            {{ post.excerpt | strip_html | truncatewords: 50 }}
          {% else %}
            {{ post.content | strip_html | truncatewords: 50 }}
          {% endif %}
        </div>
        <a href="{{ post.url | relative_url }}" class="read-more-btn">Read More →</a>
      </article>
      {% endfor %}
    </div>
  {% else %}
    <div class="no-posts">
      <div class="card">
        <h2>Coming Soon!</h2>
        <p>I'm just getting started with this blog. Check back soon for updates on my game development journey, tutorials, and useful resources I discover along the way.</p>
        <p>In the meantime, you can follow my live development streams on <a href="https://www.twitch.tv/sylaratomic" target="_blank">Twitch</a> or check out my videos on <a href="https://www.youtube.com/@SylarAtomic" target="_blank">YouTube</a>!</p>
      </div>
    </div>
  {% endif %}
</div>