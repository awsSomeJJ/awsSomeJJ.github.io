---
layout: post
title: All Tags
description:All Tags
---
<div class="tags-items-section">
    {% for tag in site.tags %}
        <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
<ul class="tags-items-posts">
    {% for post in tag[1] %}
<li>
        <a class="post-title" href="{{ site.baseurl }}/tags">
{{ post.title }}
<small class="post-date">{{ post.date | date_to_string }}</small>
</a>
</li>
    {% endfor %}
</ul>
    {% endfor %}
</div>