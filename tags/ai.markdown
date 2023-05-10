---
layout: tag
title: "Tag: AI"
permalink: /t/ai
---

<div class="row">
 {%- for post in site.tags["ai"] -%}
    <div class="col-md-4">
        <div class="card">
         <img src="{{post.coverphoto}}" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title">
                <a class="post-link" href="{{ post.url | relative url }}" style="font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 16px;"><b>
                    {{ post.title | escape }}</b>
                </a>
                </h5>
         <span class="post-meta card-text" style="font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 16px;">{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
         {{ post.date | date: date_format }}
          <br>
        <marquee><span class="post-meta">
          {%- for tag in post.tags -%}
            <a href="/t/{{ tag | downcase | replace: ' ', '-' }}" style="font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 16px;">
              #{{ tag }}
            </a>&nbsp;
          {%- endfor -%}
        </span></marquee>
        <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        <!--{{ post.excerpt }}-->
      </span>
 </div>
    </div>
    </div>
    {%- endfor -%}
</div>



