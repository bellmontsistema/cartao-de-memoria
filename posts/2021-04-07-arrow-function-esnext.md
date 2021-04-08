---
title: Arrow Function - ESNext
description: Uma expressão arrow function possui uma sintaxe mais curta quando
  comparada a uma expressão de função (function expression) e não tem seu
  próprio this, arguments, super ou new.target. Estas expressões de funções são
  melhor aplicadas para funções que não sejam métodos, e elas não podem ser
  usadas como construtoras (constructors).
date: 2021-04-07 12:36:05
thumbnail: assets/img/designer.svg
category: ESNext
background: "#fbde34"
---
## Arrow Function

Uma **expressão *arrow function*** possui uma sintaxe mais curta quando comparada a uma expressão de função (*[function expression](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/function)*) e não tem seu próprio *[this](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/this)*, *[arguments](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Functions/arguments)*, *[super](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/super)* ou *[new.target](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/new.target)*. Estas expressões de funções são melhor aplicadas para funções que não sejam métodos, e elas não podem ser usadas como construtoras (*constructors*).

## JavaScript Tradicional

```javascript
const maceio = ['Jatiúca', 'Ponta Verde', 'Pajuçara']

const amo = maceio.map(function(nome) {
  return `Eu Amo ${nome}`
})

console.log(amo)
```

Output  `[ 'Eu Amo Jatiúca', 'Eu Amo Ponta Verde', 'Eu Amo Pajuçara' ]`

## Arrow Function

Observe que na versão com `arrow function` podemos retirar a palavra reservada `function`

```javascript
const amoArrow = maceio.map((nome) => {
  return `Eu Amo ${nome}`
})

console.log(amoArrow)
```

Output  `[ 'Eu Amo Jatiúca', 'Eu Amo Ponta Verde', 'Eu Amo Pajuçara' ]`

## Arrow Function Parâmetros

Observe que como temos apenas um parâmetro podemos retirar os `()` da aplicação

```javascript
const amoArrowSingle = maceio.map(nome => {
  return `Eu Amo ${nome}`
})

console.log(amoArrowSingle)
```

Output  `[ 'Eu Amo Jatiúca', 'Eu Amo Ponta Verde', 'Eu Amo Pajuçara' ]`

## Arrow Function com apenas uma linha

Observe que retiramos as `{}` e a palavra reservada `return` e deixamos o códito ainda menor.

```javascript
const amoArrowOneSingle = maceio.map(nome => `Eu Amo ${nome}`)

console.log(amoArrowOneSingle)
```

Output  `[ 'Eu Amo Jatiúca', 'Eu Amo Ponta Verde', 'Eu Amo Pajuçara' ]`

## Exemplo com encadeamento de métodos

Observe que utilizamos o encadeamento do `filter` e o encadeamento do `map` de maeira bem mais simples e de fácil entendimento do código.

```javascript
const amoChain = maceio
                .filter(nome => nome === 'Ponta Verde')
                .map(nome => `Eu Amo ${nome}!`)

console.log(amoChain)
```

Output  `[ 'Eu Amo Ponta Verde!' ]`

## Dos fatores influenciaram a introdução das Arrow Functions:

`funções mais curtas` e a inexistência da palavra chave `this`.

Observe que quando eu quero utilizar um método de dentro do objeto a `arrow function` é bastante útil. 

```javascript
const feijoada = {
  feijao: 'preto',
  carne: 'porco',
  tempero: 'baiano',

  preparo: function() {
    return `Eu coloco na panela: feijão ${feijao}, carne de ${carne} e tempero ${tempero}.`
  },

  depois: function() {
    window.setTimeout(() => {
      console.log(this.preparo())
    }, 500)
  }
}

const btn = document.getElementById('btn')

btn.addEventListener('click', function(){feijoada.depois})
```