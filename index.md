---
layout: default
title: Home
---

<div class="fade-in-up">
  <h1>Welcome to My Site</h1>
  <p class="lead">A beautiful dark-themed Jekyll site built for GitHub Pages.</p>
  
  <div class="intro-section">
    <p class="greeting">Hi there! 👋</p>
    <p>Welcome to the official <strong>SylarAtomic</strong> website.</p>
    <p>I'm currently developing my tower defense game, <strong>Echoes of the Archive</strong>, and streaming the whole process on Twitch and YouTube. This site is a hub for tips, tricks, tutorials, and all the useful resources I find along the way.</p>
    <p>My goal is to document my journey and share what I learn to help others on their own creative paths.</p>
  </div>
  
  <div class="social-hero">
    <h2>Connect With Me</h2>
    <div class="social-links-grid">
      <a href="https://www.twitch.tv/sylaratomic" target="_blank" class="social-card twitch">
        <div class="social-icon">
          <i class="bi bi-twitch"></i>
        </div>
        <div class="social-info">
          <h3>Twitch</h3>
          <p>Watch me live stream</p>
        </div>
      </a>
      
      <a href="https://www.youtube.com/@SylarAtomic" target="_blank" class="social-card youtube">
        <div class="social-icon">
          <i class="bi bi-youtube"></i>
        </div>
        <div class="social-info">
          <h3>YouTube</h3>
          <p>Check out my videos</p>
        </div>
      </a>
      
      <a href="https://discord.gg/9FeAq3afv3" target="_blank" class="social-card discord">
        <div class="social-icon">
          <i class="bi bi-discord"></i>
        </div>
        <div class="social-info">
          <h3>Discord</h3>
          <p>Join the community</p>
        </div>
      </a>
      
      <a href="https://bsky.app/profile/sylaratomic.bsky.social" target="_blank" class="social-card bluesky">
        <div class="social-icon">
          <i class="bi bi-cloud"></i>
        </div>
        <div class="social-info">
          <h3>Bluesky</h3>
          <p>Follow my thoughts</p>
        </div>
      </a>
    </div>
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