---
title: Template Literals (Template String, Concatenação) - ESNext
description: Template Strings são strings que permitem expressões embutidas.
  Você pode utilizar string multi-linhas e interpolação de string com elas.
date: 2021-04-07 01:38:47
thumbnail: assets/img/designer.svg
category: ESNext
background: "#fbde34"
---
## Concatenação com javaScript ES5

```javascript
const local = {
  cidade: 'Maceió',
  hoby: 'Praia'
}

const sobreMinEs5 = 'Eu moro em ' + local.cidade + ' e adoro ir à ' + local.hoby

console.log(sobreMinEs5)
```

Output  `Eu moro em Maceió e adoro ir à Praia`

## Concatenação com JavaScript ES6

```javascript
const sobreMinEs6 = ` Eu moro em ${local.cidade} e adoro ir à ${local.hoby}`

console.log(sobreMinEs6)
```

Output  `Eu moro em Maceió e adoro ir à Praia`

## Concatenação com quebra de linha ES5

```javascript
const frutas = 'banana'
              + '\n'
              + 'manga'
              + '\n'
              + 'abacate'

console.log(frutas)
```

Output 

  `banana`

  `manga`

  `abacate`

## Concatenação com quebra de linha ES6

```javascript
const frutasEs6 = `
  banana
  manga
  abacate
`

console.log(frutasEs6)
```

Output 

  `banana`

  `manga`

  `abacate`

## HTML Fragments

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>



</body>
<script>

    const article = {
      title: 'Aprendendo Template Strings',
      intro: `Uma breve instrodução de como utilizar
      templete strings do es6 no seu código hoje`,
      tags: ['es6', 'js', 'template literals'],
      author: 'Henrique Teixeira'
    };

    function renderAuthor(name) {
      return (name) ? name : 'Autor anônimo'
    };

    const markup = `
      <article>
        <header>
          <h1>${article.title}</h1>
        </header>
        <section>
          <p>${article.intro}</p>
        </section>
        <footer>
          <ul>
            ${article.tags.map((content) => `
              <li>${content}</li>
              `).join('')}
          </ul>
          <p>Author: ${renderAuthor(article.author)}</p>
        </footer>
      </article>
    `;

      document.body.innerHTML = markup
</script>
</html>
```

![](/assets/img/template-literals-template-string-concatenação-.png)

## Tagged Templete

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .color {
      color: red;
      font-size: 24px;
      font-weight: bold;
      text-decoration: underline;
    }
  </style>
</head>
<body>
  
</body>
<script>
  const cidade = 'Maceió'
  const bairro = 'Feitosa'
  const referencia = 'Rodoviária'

  function color(template, ...values) {
    return template.reduce((accumulator, port, i) => {
      return `
        ${accumulator}
        <span class="color">${values[i - 1]}</span>
        ${port}
      `
    })
  }

  const logradouro = color`Eu moro em ${cidade} no bairro ${bairro} próximo a ${referencia}!`

  document.body.innerHTML = logradouro

</script>
</html>
```



![](assets/img/tagged-template.png)