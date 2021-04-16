---
title: useCallBack
description: Retorna um callback memoizado.
date: 2021-04-16 04:43:26
thumbnail: data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9Ii0xMS41IC0xMC4yMzE3NCAyMyAyMC40NjM0OCI+CiAgPHRpdGxlPlJlYWN0IExvZ288L3RpdGxlPgogIDxjaXJjbGUgY3g9IjAiIGN5PSIwIiByPSIyLjA1IiBmaWxsPSIjNjFkYWZiIi8+CiAgPGcgc3Ryb2tlPSIjNjFkYWZiIiBzdHJva2Utd2lkdGg9IjEiIGZpbGw9Im5vbmUiPgogICAgPGVsbGlwc2Ugcng9IjExIiByeT0iNC4yIi8+CiAgICA8ZWxsaXBzZSByeD0iMTEiIHJ5PSI0LjIiIHRyYW5zZm9ybT0icm90YXRlKDYwKSIvPgogICAgPGVsbGlwc2Ugcng9IjExIiByeT0iNC4yIiB0cmFuc2Zvcm09InJvdGF0ZSgxMjApIi8+CiAgPC9nPgo8L3N2Zz4K
category: ReactJS
background: "#50bbd7"
---
Recebe como argumentos, um callback e um array. `useCallback` retornará uma versão memoizada do `callback` que só muda se uma das entradas tiverem sido alteradas. Isto é útil quando utilizamos callbacks a fim de otimizar componentes filhos, que dependem da igualdade de referência para evitar renderizações desnecessárias (como por exemplo `shouldComponentUpdate`).

`useCallback(fn, inputs)` é equivalente a `useMemo(() => fn, inputs)`

```javascript
import React, { useCallback, useState } from "react";
import "./App.css";

const Button = React.memo(({ incrementButton }) => {
  // console.log('Filho Renderizou')
  return <button onClick={() => incrementButton(10)}>+</button>;
});

function UseCallBack() {
  const [counter, setCounter] = useState(0);

  const incrementCounter = useCallback((num) => {
    setCounter((c) => c + num);
  }, []);

  // console.log('pai renderizou')

  return (
    <div className="App" style={{background: 'blue'}}>
      <h1>useCallBack</h1>
      <h1>C1: {counter}</h1>
      <Button incrementButton={incrementCounter} />
    </div>
  );
}

export default UseCallBack;

```