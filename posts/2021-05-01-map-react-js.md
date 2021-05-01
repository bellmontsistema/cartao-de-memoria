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
  const filmes = ['Before Sunrise', 'Before Sunset', 'Before Midnight'];

  return (
    <ul>
      {filmes.map((filme) => (
        <li key={filme}>{filme}</li>
      ))}
    </ul>
  );
};

```