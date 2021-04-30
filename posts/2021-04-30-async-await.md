---
title: Async / Await
description: Fetch retorna uma promisse. É possível criarmos funções
  assíncronas, que irão esperar a promisse resolver, antes de continuar com o
  código.
date: 2021-04-30 06:35:14
thumbnail: https://www.mundojs.com.br/wp-content/uploads/2018/11/asynexpress.png
category: Javascript
background: "#FEC748"
---
```javascript
async function fetchProdutos(url) {
  const response = await fetch(url);
  const json = await response.json();
  return json;
}

fetchProdutos('https://backend-bellmont.herokuapp.com/pages');
```