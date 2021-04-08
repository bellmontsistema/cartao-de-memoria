---
title: "React - Componentes Stateless  e Stateful "
description: Componentes sem estado são componentes funcionais simples sem ter
  um estado local, mas lembre-se de que há um gancho em reagir para adicionar
  comportamento de estado em ...
date: 2021-04-08 05:39:03
thumbnail: assets/img/designer.svg
category: ReactJS
background: "#50bbd7"
---
## Component Stateless

components sem estado.

Exemplo 1 sem classe

```javascript
import React from 'react'

function App() {
  return (
    <h1>Olá Mundo</h1>
  )
}

export default App
```

Exemplo 2 com classe

```javascript
import React, { Component } from 'react'

class App extends Component () {
  render() {
    return (
      <h1>Olá Mundo</h1>
    )
  }
}

export default App
```

## Component Stateful

components com estado

exemplo com classe

```javascript
import React,{ Component } from 'react';
import logo from './logo.svg';
import './App.css';

class App extends Component {

  constructor(props) {
    super(props)

    this.state = {
      name: 'Carlos Henrique'
    }
  }

  render() {

    const { name } = this.state

    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <p>
            Meu nome é {name}
          </p>
        </header>
      </div>
    );
  }
}

export default App;
```

![](/assets/img/components-com-estado-stateful.png)