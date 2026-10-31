---
layout: default
title: Blog
permalink: /blog/
---
<h1 class="page-title">Blog</h1>
<p>
  {% for c in site.data.categories %}<a class="chip" href="#{{ c.key }}">{{ c.label }}</a>{% endfor %}
</p>

{% for c in site.data.categories %}
<section id="{{ c.key }}">
  <h2>{{ c.label }}</h2>
  <p class="cat-desc">{{ c.desc }}</p>
  <ul class="post-list">
    {% assign posts = site.posts | where: "category", c.key %}
    {% for post in posts %}
    <li>
      <time>{{ post.date | date: "%Y.%m.%d" }}</time>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% else %}
    <li>아직 글이 없습니다.</li>
    {% endfor %}
  </ul>
</section>
{% endfor %}
