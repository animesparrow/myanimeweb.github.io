---
layout: tag
title: "Tag: Spring 2023 Anime"
permalink: /t/spring2023anime
---

<ul class="post-list">
  {%- for post in site.tags["Spring2023Anime"] -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <span class="post-meta">
        {{ post.date | date: date_format }}
      </span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
    </li>
  {%- endfor -%}
</ul>