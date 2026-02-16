---
layout: base
title: All Topics
permalink: /tags/
---

<h1>{{ page.title }}</h1>

<div class="tag-index">
  {% assign sorted_tags = site.tags | sort %}

  {% for tag in sorted_tags %}
    {% assign tag_name = tag[0] %}
    {% assign posts = tag[1] %}

    <section class="tag-section" id="{{ tag_name }}">
      <h2>#{{ tag_name | replace: '-', ' ' }}</h2>

      <ul class="tag-post-list">
        {% for post in posts %}
          <li>
            <a href="{{ post.url | relative_url }}">
              {{ post.title }}
            </a>
            <span class="post-meta">
              {{ post.date | date: "%b %-d, %Y" }}
            </span>
          </li>
        {% endfor %}
      </ul>
    </section>
  {% endfor %}
</div>