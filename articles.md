---
layout: page
title: Artcles
subtitle: Articles
ref: posts
lang: fr
permalink: /articles/
location: posts
---

<div class="list-posts">
    <ul class="no-style">
      {% assign posts = site.posts | sort: 'date' | reverse %}
      {% for post in posts %}
        <li>
          {{ post.date | date: '%Y-%m-%d' }} - 
          <a href="{{ post.url }}">{{ post.title | capitalize }}</a>
          by {{ post.author }}.
          {% for keyword in post.keywords %}
            {{ keyword }};
          {% endfor %}
        </li>
        <hr>
      {% endfor %}
    </ul>
 </div>