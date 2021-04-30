---
title: Expressões / Variáveis React JS
description: Expressões e variáveis podem ser colocadas dentro do JSX, utilizando chaves {}.
date: 2021-04-30 03:25:49
thumbnail: https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGC8FHJxkcWI8YI5ROqT_iNm8IrKG-l56ezg&usqp=CAU
category: ReactJS
background: "#50bbd7"
---
```javascript
const App = () => {
  const nome = 'André';
  return <p>{nome}</p>;
};

```

```javascript
const App = () => {
  const desconto = 50;
  const preco = 250;
  return <p>{preco - desconto}</p>;
};

```

```javascript
const App = () => {
  const ativo = true;
  return <p className={ativo ? 'ativo' : 'inativo'}>Estoque</p>;
};

```

Também posso atribuir JSX direto a uma constante/variável

```javascript
const Titulo = <h1>Meu título</h1>;

const App = () => {
  return <div>{Titulo}</div>;
};

```