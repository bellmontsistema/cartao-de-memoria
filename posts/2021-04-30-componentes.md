---
title: Componentes
description: Permitem você dividir a sua interface em pequenos elementos. São
  criados através de funções que retornam elementos React ou classes que
  estendem React.Component e possuem o método render retornando um elemento
  React.
date: 2021-04-30 07:42:20
thumbnail: https://easybase.io/assets/images/posts_images/5-great-react-libraries-1.png
category: ReactJS
background: "#50bbd7"
---
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