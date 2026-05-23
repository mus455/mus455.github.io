---
layout: default
title: "Home"
---

HI, I'M MATIJA. THIS WEBSITE IS MY MINIMALIST REPOSITORY OF OBSERVATIONS.

My work tends to explore what i call slice of life : streets, architecture and various feelings that i want to narrate. This is currently more of an beta version of my final website.

Below is a collection of my work in photography since the march of 2026 when i got a RICOH GR III since i wanted to learn photography for an upcoming trip and started my journey in photography (photos are after experiences best sorts of free-willed memories we make along the way). 

---

{% assign books = site.books %}
{% assign blogs = site.blog %}
{% assign unified_feed = books | concat: blogs | sort: 'date' | reverse %}

<section class="strong-index">
  {% for item in unified_feed %}
    <article class="feed-entry">
      <a href="{{ item.url | relative_url }}" class="entry-link">
        <h3 class="entry-title">{{ item.title }}</h3>
        
        {% if item.cover_image %}
          <div class="photo-preview">
            <img src="{{ item.cover_image | relative_url }}" class="gritty-thumb" alt="{{ item.title }}">
          </div>
        {% endif %}
        
        {% if item.collection == 'blog' %}
          <div class="text-preview">
            {{ item.content | strip_html | truncatewords: 20 }} 
            <span class="read-more">// READ MORE</span>
          </div>
        {% endif %}
        
        <span class="entry-date">{{ item.date | date: "%Y.%m" }}</span>
      </a>
    </article>
  {% endfor %}
</section>

**[Send me an email](mailto:autumntrees@protonmail.com)**