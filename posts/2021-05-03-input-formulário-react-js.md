---
title: input - Formulário React JS
description: input - Formulário React JS
date: 2021-05-02 09:34:09
thumbnail: https://www.luiztools.com.br/wp-content/uploads/2020/06/reactJS.png
category: ReactJS
background: "#50bbd7"
---
## Reatividade

Para criarmos campos de formulário reativos, devemos definir o estado para o `value` e a função atualizadora para o `onChange`.

```jsx
const App = () => {
  const [nome, setNome] = React.useState('');

  return (
    <form>
      <label htmlFor="nome">Nome</label>
      <input
        type="text"
        id="nome"
        value={nome}
        onChange={(event) => setNome(event.target.value)}
      />
      <p>{nome}</p>
    </form>
  );
};

```

> O atributo for é usado como htmlFor no JSX

## Form

No `form` controlamos o que acontece ao enviar o mesmo, por isso definimos uma função para lidar com o `onSubmit`. O `preventDefault()` irá prevenir o comportamento padrão, que seria de atualizar a página, enviando uma requisição para o que estiver em `action=""`.

```jsx
const App = () => {
  const [nome, setNome] = React.useState('');

  function handleSubmit(event) {
    event.preventDefault();
    console.log(nome);
  }

  return (
    <form onSubmit={handleSubmit}>
      <label htmlFor="nome">Nome</label>
      <input
        type="text"
        id="nome"
        value={nome}
        onChange={(event) => setNome(event.target.value)}
      />
      <button>Enviar</button>
    </form>
  );
};

```

## Múltiplos Campos

Podemos definir um estado para cada campo.

```jsx
const App = () => {
  const [nome, setNome] = React.useState('');
  const [email, setEmail] = React.useState('');

  function handleSubmit(event) {
    event.preventDefault();
    console.log(nome, email);
  }

  return (
    <form onSubmit={handleSubmit}>
      <label htmlFor="nome">Nome</label>
      <input
        type="text"
        id="nome"
        value={nome}
        onChange={(event) => setNome(event.target.value)}
      />
      <label htmlFor="email">Email</label>
      <input
        type="email"
        id="email"
        value={email}
        onChange={(event) => setEmail(event.target.value)}
      />
      <button>Enviar</button>
    </form>
  );
};

```

## Objeto

Podemos definir um objeto que irá conter todos os valores dos campos do formulário.

```jsx
const App = () => {
  const [form, setForm] = React.useState({
    nome: '',
    email: '',
  });

  function handleSubmit(event) {
    event.preventDefault();
    console.log(form);
  }

  function handleChange({ target }) {
    const { id, value } = target;
    setForm({ ...form, [id]: value });
  }

  return (
    <form onSubmit={handleSubmit}>
      <label htmlFor="nome">Nome</label>
      <input type="text" id="nome" value={form.nome} onChange={handleChange} />
      <label htmlFor="email">Email</label>
      <input
        type="email"
        id="email"
        value={form.email}
        onChange={handleChange}
      />
      <button>Enviar</button>
    </form>
  );
};

```