---
layout: default 
title: Hello World!
tagline: hello cydu
---
{% include JB/setup %}

<ul class="posts">
    {% for post in site.posts %}
        <div class="post">
        <li><span>
        {{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
        </li>
        </div>
    {% endfor %}
</ul> 
