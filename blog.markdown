---
layout: page
title: Blog
permalink: /blog/
---

# Blog Posts

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    <p>{{ post.excerpt }}</p>
    <a href="{{ post.url | relative_url }}">Read more →</a>
  </article>
  <hr>
{% endfor %}

{% if site.posts.size == 0 %}
  <p>No blog posts yet. Check back later!</p>
{% endif %}