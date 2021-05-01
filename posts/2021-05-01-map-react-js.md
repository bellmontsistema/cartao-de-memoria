---
title: Map React JS
description: É comum usarmos o map direto na array como uma expressão,
  retornando um elemento para cada item novo da Array.
date: 2021-04-30 09:32:22
thumbnail: https://miro.medium.com/max/3840/1*vHHBwcUFUaHWXntSnqKdCA.png
category: ReactJS
background: "#50bbd7"
---
```javascript
const App = () => {
  const empresas = [<li key="e1">Apple</li>, <li key="e2">Google</li>];

  return <ul>{empresas}</ul>;
};

```