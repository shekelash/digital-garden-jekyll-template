---
layout: page
title: test0
permalink: /test0
---

<style>
  .wrapper {
    max-width: 46em;
  }
</style>


<ul class="archive">
{% for note in site.notes %}
  <li>
    <a href="{{ note.url }}{%- if site.use_html_extension -%}.html{%- endif -%}" class="internal-link">
    {{note.title}}</a>{% if note.category != null %} in {{note.category}}{% endif %} 
    <span>{{ note.last_modified_at | date: "%B %-d, %Y" }}</span>
    <p>
        {% if note.summary %}
          {{ note.summary | strip_html | truncate: 50, "..." }}
        {% else %}
          {{ note.excerpt | strip_html | truncate: 50, "..." }}
        {% endif %}
    </P>
  </li>
{% endfor %}
</ul>


<div class = "paginator">
    {% if paginator.total_pages > 1 %}
    {% if paginator.next_page %}
      <a class = "older paginate-button" href="{{ paginator.next_page_path | relative_url }}">Older Posts</a>
    {% endif %}
    {% if paginator.previous_page %}
    <a class = "newer paginate-button" href="{{ paginator.previous_page_path | relative_url }}">Newer Posts</a>
  {% endif %}
  {% endif %}
</div>

<section>
  {%- if site.show_notes_graph -%}<p>Here are all the notes in this garden, along with their links, visualized as a graph.</p>{% include notes-graph.html %}{%- endif -%}</section>
