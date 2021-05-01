---
title: JSX Arrays
description: O JSX irá listar cada um dos itens da array. Ele não irá separar ou
  colocar vírgula, é você que deve modificar a array para o resultado desejado.
date: 2021-04-30 09:28:30
thumbnail: https://miro.medium.com/max/3840/1*vHHBwcUFUaHWXntSnqKdCA.png
category: ReactJS
background: "#50bbd7"
---
```javascript
const App = () => {
  const produtos = ['Notebook', 'Smartphone', 'Tablet'];

  return <p>{produtos}</p>;
};
```