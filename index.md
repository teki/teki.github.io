---
layout: base
---

👾

Random things (blog):

<ul class="pure-menu-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
