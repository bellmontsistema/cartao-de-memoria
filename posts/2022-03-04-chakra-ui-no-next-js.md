---
title: Chakra UI no Next JS
description: Como instalar o Chakra UI e configurar no Next JS
date: 2022-03-04 08:33:40
thumbnail: https://res.cloudinary.com/practicaldev/image/fetch/s--0UnD_9S7--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/n95iol17gaecwx2rwm2y.jpeg
category: NextJS
background: "#000000"
---
## Instalação

Primeiro Instalamos as dependências do chakra UI

```jsx
yarn add @chakra-ui/react @chakra-ui/core @emotion/react @emotion/styled framer-motion
```

Após instalado criamos uma pasta com 2 arquivos no `src`

Pasta => styles

Arquivos => `config.ts` e `theme.ts`

`Criando um Tema Padrão`

No arquivo theme.ts efetuaremos a seguinte configuração.