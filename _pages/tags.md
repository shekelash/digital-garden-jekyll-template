---
layout: page
title: Tags
permalink: /tags
---

  <div class="tags-list">
    {% for note in tag[1] %}
      <li><a href="{{ note.url }}">{{ note.title }}</a></li>
    {% endfor %}
  </div>
