---
layout: page
title: Search
permalink: /search
---

<div id="search"></div>

<div class="post-list" id="search-hits">
</div>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.css" />
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.js"></script>
<script type="text/javascript">
  algoliasearchNetlify({
    appId: 'AC4IYHQBFD',
    apiKey: '5e776877457a7a11f77d5f7ec94fbffc',
    siteId: '777455cf-95e4-4e36-96b8-dffb1428e7ae',
    branch: 'master',
    selector: 'div#search',
  });
</script>
