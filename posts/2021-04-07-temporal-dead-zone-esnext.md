---
title: "Temporal Dead Zone - ESNext "
description: Variáveis declaradas com const e let não são afetadas pela TDZ,
  pois obrigatoriamente precisam ser inicializadas durante sua declaração.
date: 2021-04-06 10:54:46
thumbnail: assets/img/designer.svg
category: ESNext
background: "#fbde34"
---
Variáveis declaradas com `const` e `let` não são afetadas pela `TDZ`, pois obrigatoriamente precisam ser inicializadas durante sua declaração.



## Const

```javascript
console.log(rick)
const rick = 'lindo'
```

ReferenceError

```javascript
VM121:1 Uncaught ReferenceError: Cannot access 'rick' before initialization
    at <anonymous>:1:13
```

## Let

```

```

SyntaxError

```
Uncaught SyntaxError: Identifier 'rick' has already been declared
```