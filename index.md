---
layout: page
title: Welcome
tagline: truth and love
---
{% include JB/setup %}

### What's in this blog
* My thought on various things
* My personal life, sometimes
* Some resources you may find helpful

### Who am I
* a normal human being, who wants to do something
* [resume]({{johnzw.github.io}}/assets/new_version_cv.pdf)
* github: [johnzw](https://github.com/johnzw)

### History posts
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



