---
title: React Element
description: Todo elemento React é criado com a função createElement. O Babel é
  o responsável por transformar o elemento criado com JSX (que se parece com
  HTML) em funções de React.
date: 2021-04-30 07:35:07
thumbnail: https://miro.medium.com/max/3840/1*vHHBwcUFUaHWXntSnqKdCA.png
category: ReactJS
background: "#50bbd7"
---
```javascript
function App() {
  return <div id="container">Meu App</div>;
}
// É transformado em:
function App() {
  return React.createElement('div', { id: 'container' }, 'Meu App');
}
```

![](https://www.origamid.com/slide/react-completo/aulas/02-react-para-iniciantes/0202-react-basico/createlement.png)

Babel <https://babeljs.io/repl>