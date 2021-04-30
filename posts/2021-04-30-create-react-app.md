---
title: Create React App
description: Iniciando um projeto com React JS
date: 2021-04-30 02:12:22
thumbnail: https://res.cloudinary.com/practicaldev/image/fetch/s--o3NPyJMc--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/hsb1f9m59s04q9xnyml4.png
category: ReactJS
background: "#50bbd7"
---
Cria um ambiente de desenvolvimento já configurado e otimizado para a criação de aplicativos com React. <https://create-react-app.dev/>

`npx create-react-app meuapp`

npx é um comando do NPM que executa diretamente um pacote online, sem a necessidade de instalarmos o pacote na nossa máquina. A vantagem é que ele irá sempre instalar a versão mais atualizada do ambiente criado por create-react-app.

## Estrutura Mínima

Abaixo os arquivos essenciais. Todos os demais arquivos, apenas definem padrões que a equipe do React assume que vamos precisar, porém não são necessários.

```
- node_modules
- public
  - index.html
- src
  - index.js
- package.json
- package-lock.json

```

Código mínimo para o index.html

```javascript
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="utf-8" />
    <title>React App</title>
  </head>

  <body>
    <div id="root"></div>
  </body>
</html>

```

Código mínimo para o index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(<div>Aplicativo</div>, document.getElementById('root'));

```

## Comandos

`Inicia o desenvolvimento`

`npm start`

Cria a build final

`npm build`