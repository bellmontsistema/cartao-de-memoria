---
title: Exercício 2 - React JS
description: Exercício 2 - React JS
date: 2021-04-30 10:06:03
thumbnail: https://miro.medium.com/max/3840/1*vHHBwcUFUaHWXntSnqKdCA.png
category: ReactJS
background: "#50bbd7"
---
```javascript
import React from "react";

// Organize os produtos como mostrado no vídeo
// Mostre apenas produtos que forem mais caros que R$ 1500
const produtos = [
  {
    id: 1,
    nome: "Smartphone",
    preco: "R$ 2000",
    cores: ["#29d8d5", "#252a34", "#fc3766"],
  },
  {
    id: 2,
    nome: "Notebook",
    preco: "R$ 3000",
    cores: ["#ffd045", "#d4394b", "#f37c59"],
  },
  {
    id: 3,
    nome: "Tablet",
    preco: "R$ 1500",
    cores: ["#365069", "#47c1c8", "#f95786"],
  },
];

const App = () => {
  return (
    <section>
      {produtos
        .filter(({ preco }) => Number(preco.replace("R$", "")) > 1500)
        .map(({ id, nome, preco, cores }) => {
          return (
            <div key={id}>
              <h1>{nome}</h1>
              <p>Preço: {preco}</p>
              <ul>
                {cores.map((cor) => {
                  return (
                    <li
                      style={{ backgroundColor: cor, color: "white" }}
                      key={cor}
                    >
                      {cor}
                    </li>
                  );
                })}
              </ul>
            </div>
          );
        })}
    </section>
  );
};

export default App;
```