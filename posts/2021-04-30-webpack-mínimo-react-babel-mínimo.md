---
title: Webpack Mínimo - React - Babel Mínimo
description: Instalando uma aplicação React JS Manualmente
date: 2021-04-30 01:26:45
thumbnail: https://cdn.shortpixel.ai/client/q_glossy,ret_img,w_1200,h_600/https://ezdevs.com.br/wp-content/uploads/2019/03/react.jpg
category: ReactJS
background: "#50bbd7"
---
## Webpack Mínimo

Iniciar um pacote npm na pasta do seu aplicativo

`npm init -y`

Instalar o webpack, webpack-cli e webpack-dev-server

`npm install webpack webpack-cli webpack-dev-server --save-dev`

Criar arquivos mínimos

* `index.html`
* `src/`

  * `index.js`

index.html

```javascript
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React</title>
  </head>

  <body>
    <div id="root"></div>
    <!-- Main é criado pelo webpack -->
    <script src="main.js"></script>
  </body>
</html>
```

Adicionar os scripts de desenvolvimento e build ao package.json

```javascript
"scripts": {
  "start": "webpack serve --mode development --open --hot",
  "build": "webpack --mode production"
},

```

## React

`npm install react react-dom`

index.js

```javascript
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(App(), document.getElementById('root'));

```

app.js

```javascript
import React from 'react';

const App = () => {
  return React.createElement(
    'a',
    { href: 'https://www.origamid.com' },
    'Origamid',
  );
};

export default App;
```

Inicie o desenvolvimento com:

<!--StartFragment-->

```bash

```

`npm start`

## Babel Mínimo

`npm install @babel/core @babel/preset-react babel-loader --save-dev`

Criar o webpack.config.js para configurarmos o babel no webpack

```javascript
module.exports = {
  // Nos módulos
  module: {
    // Aplique as seguintes regras
    rules: [
      {
        // Nos arquivos que terminam ($) com .js
        test: /\.js$/,
        // Não procure nada em node_modules
        exclude: /node_modules/,
        // Use o seguinte:
        use: {
          // Babel
          loader: 'babel-loader',
          // Com as opções padrões para o React
          options: {
            presets: ['@babel/preset-react'],
          },
        },
      },
    ],
  },
};

```

App.js

```javascript
import React from 'react';

const App = () => {
  return <a href="https://bellmontsistema.com.br">Origamid</a>;
};

export default App;

```

index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(<App />, document.getElementById('root'));
```

Inicie o desenvolvimento com:

`npm start`

Crie a build final com:

`npm run build`

## Babel Mínimo

Instalar @babel/core, @babel/preset-react e babel-loader

`npm install @babel/core @babel/preset-react babel-loader --save-dev`

Criar o webpack.config.js para configurarmos o babel no webpack



```javascript
module.exports = {
  // Nos módulos
  module: {
    // Aplique as seguintes regras
    rules: [
      {
        // Nos arquivos que terminam ($) com .js
        test: /\.js$/,
        // Não procure nada em node_modules
        exclude: /node_modules/,
        // Use o seguinte:
        use: {
          // Babel
          loader: 'babel-loader',
          // Com as opções padrões para o React
          options: {
            presets: ['@babel/preset-react'],
          },
        },
      },
    ],
  },
};

```

App.js

```javascript
import React from 'react';

const App = () => {
  return <a href="https://www.origamid.com">Origamid</a>;
};

export default App;

```

index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(<App />, document.getElementById('root'));

```

Inicie o desenvolvimento com:

`npm start`

Crie a build final com:

`npm run build`