---
layout: page
title: Archive
permalink: /archive
---
<ul class="archive">
{% for note in site.notes %}
  <li>
    <a href="{{ note.url }}{%- if site.use_html_extension -%}.html{%- endif -%}" class="internal-link">
    <b>{{note.title}}</b></a>{% if note.category != null %} in {{note.category}}{% endif %} 
    <span>({{ note.last_modified_at | date: "%B %Y" }})</span>
    <p>
        <span class="summary">
        {% if note.summary %}
          {{ note.summary | strip_html | truncate: 60, "..." }}
        {% else %}
          {{ note.excerpt | strip_html | truncate: 60, "..." }}
        {% endif %}
       </span>
    </P>
  </li>
{% endfor %}
</ul>

