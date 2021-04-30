---
title: JSX Expressões React JS
description: Você pode executar qualquer expressão dentro das chaves {}.
date: 2021-04-30 03:27:50
thumbnail: https://miro.medium.com/max/5736/1*Th_2G92t3x5mARCCuFE_Dg.jpeg
category: ReactJS
background: "#50bbd7"
---
Se o resultado da expressão for um número, string ou array de números/strings o resultado irá aparecer na tela. Booleanos (true/false), undefined e null não irão resultar em nada na tela. Objetos irão retornar um erro.

```javascript
const App = () => {
  function meuNome() {
    return 'Henrique';
  }

  function quadrado(x) {
    return x * x;
  }

  const carro = {
    rodas: 4,
    marca: 'Palio',
  };

  return (
    <div>
      <p>{'MINHA EMPRESA'.toLowerCase()}</p>
      <p>{30 * 2}</p>
      <p>{true}</p>
      <p>{undefined}</p>
      <p>{(() => 'Função Executada')()}</p>
      <p>{meuNome()}</p>
      <p>{quadrado(2)}</p>
      <p>{quadrado(2) === 4 ? 'Fórmula correta' : 'Fórmula incorreta'}</p>
      <p>{quadrado(2) === 4 && 'Fórmula correta'}</p>
      <p>{Date.now()}</p>
      <p>{new Date().getFullYear()}</p>
      <p>
        Marca: {carro.marca}, Rodas: {carro.rodas}
      </p>
    </div>
  );
};

```