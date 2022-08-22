---
layout: page
title: Search
permalink: /search
---

<div id="search"></div>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.css" />
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@algolia/algoliasearch-netlify-frontend@1/dist/algoliasearchNetlify.js"></script>
<script type="text/javascript">
  algoliasearchNetlify({
    appId: 'JF08G8WUNK',
    apiKey: 'b113a01ae9d39bb783055a5d4b01b701',
    siteId: '0c6e6f1e-28a4-44fd-bf45-60e7113c4fb5',
    branch: 'master',
    selector: 'div#search',
    placeholder: 'Explore the site...',
    detached: false,
    hitsPerPage: 10,
  });
</script>


