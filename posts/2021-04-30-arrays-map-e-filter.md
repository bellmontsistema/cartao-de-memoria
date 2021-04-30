---
title: Arrays (Map e Filter)
description: Métodos para iterarmos entre os valores de arrays.
date: 2021-04-30 06:58:38
thumbnail: https://miro.medium.com/max/1400/1*VgaIWfqJXvp1HY8UxdAEKQ.jpeg
category: Javascript
background: "#FEC748"
---
```javascript
const precos = [
  'Crédito',
  'R$ 200',
  'R$ 400',
  'Contas Pagar',
  'R$ 300',
  'R$ 400',
  'Meus dados',
];

// Retorna uma array nova, que contem os items em
// que o retorno da função for verdadeiro
const precosFiltro = precos.filter((preco) => preco.includes('R$'));

// Retorna uma nova array, modificada com o
// retorno de cada item da função
const precoNumeros = precosFiltro.map((preco) =>
  Number(preco.replace('R$ ', '')),
);

```