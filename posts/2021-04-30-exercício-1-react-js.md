---
title: Exercício 1 - React JS
description: Exercício 1 - React JS
date: 2021-04-30 04:22:13
thumbnail: https://i.pinimg.com/originals/30/79/39/307939d6388aa145b2fb0142a8b1e91b.png
category: ReactJS
background: "#50bbd7"
---
```javascript
import React from "react";

// Mostre os dados da aplicação, como aprensetado no vídeo
// Não utilize CSS externo, use o style para mudar as cores
// Se a situação estiver ativa pinte de verde, inativa vermelho
// Se o gasto for maior que 10000 mostre uma mensagem

const luana = {
  cliente: "Karolina",
  idade: 27,
  compras: [
    { nome: "Boneca", preco: "R$ 150" },
    { nome: "Bicicleta", preco: "R$ 400" },
    { nome: "Patinete", preco: "R$ 250" },
  ],
  ativa: true,
};

const mario = {
  cliente: "Mikael",
  idade: 31,
  compras: [
    { nome: "Moto Elétrica", preco: "R$ 800" },
    { nome: "Bicicleta", preco: "R$ 400" },
    { nome: "Boneco do Home de Ferro", preco: "R$ 100" },
    { nome: "Kit Brinquedos para Praia", preco: "R$ 60" },
  ],
  ativa: false,
};

const App = () => {
  const dadosOne = luana;
  const dadosTwo = mario;

  const totalOne = dadosOne.compras
    .map((item) => Number(item.preco.replace("R$", "")))
    .reduce((valorAnterior, valorAtual) => valorAnterior + valorAtual);

  const totalTwo = dadosTwo.compras
    .map((item) => Number(item.preco.replace("R$", "")))
    .reduce((valorAnterior, valorAtual) => valorAnterior + valorAtual);

  return (
    <>
      <div>
        <h2>Nome: {dadosOne.cliente}</h2>
        <h3>Idade: {dadosOne.idade}</h3>
        <h4>
          Situação:{" "}
          <span style={{ color: dadosOne.ativa ? "green" : "red" }}>
            {dadosOne.ativa ? "Ativa" : "Inativa"}
          </span>
        </h4>
        <span>Total gasto: {totalOne}</span>
        <p>{totalOne > 10000 && "Você está gastando muito!"}</p>
      </div>

      <hr />

      <div>
        <h2>Nome: {dadosTwo.cliente}</h2>
        <h3>Idade: {dadosTwo.idade}</h3>
        <h4>
          Situação:{" "}
          <span style={{ color: dadosTwo.ativa ? "green" : "red" }}>
            {dadosTwo.ativa ? "Ativa" : "Inativa"}
          </span>
        </h4>
        <span>Total gasto: {totalTwo}</span>
        {totalTwo > 1000 && <p>Você está gastando muito!</p>}
      </div>
    </>
  );
};

export default App;

```