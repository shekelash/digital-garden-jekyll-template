---
layout: page
title: Archive
permalink: /archive
---
# archive

<div id="search"></div>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.css" />
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.js"></script>
<script type="text/javascript">
  algoliasearchNetlify({
    appId: 'JF08G8WUNK', //切记填写正确
    apiKey: 'b113a01ae9d39bb783055a5d4b01b701', //Search-Only API Key 切记填写正确
    siteId: '0c6e6f1e-28a4-44fd-bf45-60e7113c4fb5', //切记填写正确
    branch: 'master',
    selector: 'div#search',
    placeholder: 'Explore the site...', //搜索框的占位符
    detached: false, //移动视图下，搜索不使用分离模式
    hitsPerPage: 10, //默认返回10个结果
  });
</script>

<ul class="archive">
{% for note in site.notes %}
  <li>
    <a href="{{ note.url }}{%- if site.use_html_extension -%}.html{%- endif -%}" class="internal-link">
    {{note.title}}</a>{% if note.category != null %} in {{note.category}}{% endif %} 
    <span>({{ note.last_modified_at | date: "%B %Y" }})</span>
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

<section>
  {%- if site.show_notes_graph -%}<p>Here are all the notes in this garden, along with their links, visualized as a graph.</p>{% include notes-graph.html %}{%- endif -%}</section>




