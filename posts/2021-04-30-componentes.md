---
title: Componentes  e Composição
description: Componentes  e Composição
date: 2021-04-30 07:42:20
thumbnail: https://easybase.io/assets/images/posts_images/5-great-react-libraries-1.png
category: ReactJS
background: "#50bbd7"
---
## Componentes

Permitem você dividir a sua interface em pequenos elementos. São criados através de funções que retornam elementos React ou classes que estendem React.Component e possuem o método render retornando um elemento React.

```javascript
// Function Component
const Button = () => {
  return <button>Comprar</button>;
};

// Class Component
class Button extends React.Component {
  render() {
    return <button>Comprar</button>;
  }
}
```



## Composição

O principal motivo de criarmos componentes é para podermos compor a interface com diversos componentes que podem ser reutilizados.

```javascript
const Button = () => {
  return <button>Comprar</button>;
};

const MainNav = () => {
  return (
    <nav>
      <a href="#">Link 1</a>
      <Button />
    </nav>
  );
};

const App = () => {
  return (
    <div>
      <MainNav />
      <Button />
    </div>
  );
};
```