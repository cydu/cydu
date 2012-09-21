---
layout: default 
title: Hello World!
tagline: hello cydu
---
{% include JB/setup %}

<div>
    <a href="feed://blog.cydu.net/atom.xml" class="right">
    <img border="0" src="img/feed-icon-28x28.png" 
    title="Chuanying Du's Feed"/></a>
<h1>Articles</h1>
</div>

<ul class="posts">
    {% for post in site.posts %}
        <div class="post">
            <div class="title"><a href="{{ post.url }}">{{ post.title }}</a></div>
            <div class="date">{{ post.date | date: "%B %d, %Y" }} &nbsp &nbsp 
                {% for tag in post.tags %}
                    <a href="/tags.html#tag_{{ tag }}">{{ tag }}</a> &nbsp 
                {% endfor %}
            </div>
            <div class="extract">{{post.content | strip_html | truncatewords:40}}</div>
        </div>
    {% endfor %}
</ul> 
