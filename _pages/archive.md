---
layout: page
title: Archive
permalink: /archive
---

# Archive

<ul class="archive">
{% for note in site.notes %}
  <li>
    <a href="{{ note.url }}{%- if site.use_html_extension -%}.html{%- endif -%}" class="internal-link">
    <b>{{note.title}}</b></a>{% if note.category != null %} in {{note.category}}{% endif %} 
    <span>({{ note.last_modified_at | date: "%B %Y" }})</span>
    <p>
        <span class="summary">
        {% if note.summary %}
          {{ note.summary | strip_html | truncate: 50, "..." }}
        {% else %}
          {{ note.excerpt | strip_html | truncate: 50, "..." }}
        {% endif %}
       </span>
    </P>
  </li>
{% endfor %}
</ul>

<section>
  {%- if site.show_notes_graph -%}<p>Here are all the notes in this garden, along with their links, visualized as a graph.</p>{% include notes-graph.html %}{%- endif -%}</section>
