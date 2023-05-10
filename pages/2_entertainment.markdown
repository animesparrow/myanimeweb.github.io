---
layout: page
menu: entertainment
title: Entertainment
permalink: /entertainment/
---


<div class="row">
    {%- for post in site.categories['entertainment'] -%}
    <div class="col-md-4 p-1">
        <div class="card">
         <img src="{{post.coverphoto}}" class="card-img-top" alt="{{post.title}}">
            <div class="card-body">
                <h5 class="card-title">
                <a class="post-link" href="{{ post.url | relative url }}" style="font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 16px;color: black;"><b>
                    {{ post.title | escape }}</b>
                </a>
                </h5>
         <span class="post-meta card-text" style="font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 16px;">{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
         {{ post.date | date: date_format }}
          <br>
     <!-- <marquee><span class="post-meta">
          {%- for tag in post.tags -%}
            <a href="/t/{{ tag | downcase | replace: ' ', '-' }}" style="font-family: Verdana, Geneva, Tahoma, sans-serif;font-size: 16px;">
              #{{ tag }}
            </a>&nbsp;
          {%- endfor -%}
        </span></marquee> -->
        <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        <!--{{ post.excerpt }}-->
      </span>
 </div>
    </div>
    </div>
    {%- endfor -%}
</div>