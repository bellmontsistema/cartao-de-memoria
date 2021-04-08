---
title: Const - ESNext
description: Constantes possuem escopo de bloco, semelhantes às variáveis
  declaradas usando o palavra-chave let. O valor de uma constante não pode ser
  alterado por uma atribuição, e ela não pode ser redeclarada.
date: 2021-04-06 10:28:16
thumbnail: assets/img/designer.svg
category: ESNext
background: "#fbde34"
---
# const

Constantes possuem escopo de bloco, semelhantes às variáveis declaradas usando o palavra-chave let. O valor de uma constante não pode ser alterado por uma atribuição, e ela não pode ser redeclarada.

```javascript
const secretNumber = 28

const rick = {
  nome: 'Henrique',
  age: 32
}

rick.age = 26

console.log(rick)
```

Output \`{ nome: 'Henrique', age: 26 }\`