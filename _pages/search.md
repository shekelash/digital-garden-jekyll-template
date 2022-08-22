---
layout: page
title: Search
permalink: /search
---

<div id="search-searchbar"></div>

<div class="post-list" id="search-hits">
</div>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.css" />
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.js"></script>
<script type="text/javascript">
  algoliasearchNetlify({
    appId: 'BGF57BCC8H',
    apiKey: 'd5f055680f96a3284c0d448b654e198a',
    siteId: '777455cf-95e4-4e36-96b8-dffb1428e7ae',
    branch: 'master',
    selector: 'div#search',
  });
</script>
