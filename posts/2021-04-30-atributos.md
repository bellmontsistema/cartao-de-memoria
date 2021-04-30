---
title: Atributos
description: Atributos podem ser passados como no HTML, porém com alguns casos especiais.
date: 2021-04-30 03:17:12
thumbnail: https://community-cdn-digitalocean-com.global.ssl.fastly.net/variants/ZomDS8ECVLNK7RBdhjjUest1/035575f2985fe451d86e717d73691e533a1a00545d7230900ed786341dc3c882
category: ReactJS
background: "#50bbd7"
---


```javascript
const App = () => {
  return (
    <a href="https://bellmontsistema.com.br" title="Bellmont Sistema">
      Origamid
    </a>
  );
};

```

## Casos Especiais

O caso especial mais comum é o atributo class. Pelo fato de class ser uma palavra reservada do JavaScript, o JSX resolveu mudar o nome para evitar conflitos. O correto é className.

```javascript
const App = () => {
  return <div className="grid">Origamid</div>;
};

```

```javascript
const App = () => {
  return (
    <form>
      <label htmlFor="nome">Nome</label>
      <input type="text" id="nome" />
    </form>
  );
};

```

<https://reactjs.org/docs/dom-elements.html>