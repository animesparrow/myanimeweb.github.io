---
layout: page
menu: manga
title: Manga
permalink: /manga/
---

<ul class="post-list">
    {%- for post in site.categories['manga'] -%}
    <li>
        <span class="post-meta">
            {{post.date | date: date_format }}
        </span>
        <h3>
            <a class="post-link" href="{{ post.url | relative url }}">
                {{ post.title | escape }}
            </a>
        </h3>
        {%- if site.show_excerpts -%}
            {{post.excerpts}}
        {{%- endif -%}}
    {%- endif -%}
    </li>
    {%- endfor -%}
</ul>