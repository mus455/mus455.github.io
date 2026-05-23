---
layout: default
title: "Blog"
---

# Notes and blogposts

Everything that isnt photos.

---

<div class="blog-list">
  {% for post in site.blog reversed %}
    <article class="blog-item">
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <p class="meta">{{ post.date | date: "%B %d, %Y" }}</p>
    </article>
  {% endfor %}
</div>