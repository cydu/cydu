---
layout: default 
title: Hello World!
tagline: hello cydu
---
{% include JB/setup %}

<ul class="posts">
    {% for post in site.posts %}
        <div class="title"><a href="{{ post.url }}">{{ post.title }}</a></div>
        <div class="date">{{ post.date | date: "%B %d, %Y" }}</div>
        <div class="extract">{{post.content | strip_html | truncatewords:40}}</div>
    {% endfor %}
</ul> 
