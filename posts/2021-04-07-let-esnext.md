---
title: Let - ESNext
description: Declara uma variável local no escopo do bloco atual, opcionalmente
  iniciando-a com um valor.
date: 2021-04-06 10:22:20
thumbnail: assets/img/designer.svg
category: ESNext
background: "#fbde34"
---
## Let 

```javascript
var animal = 'cat'
console.log(animal)

{
  let animal = 'dog'
  console.log(animal)
}
console.log(animal)

//Output

cat
dog
cat
```