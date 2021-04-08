---
title: Buscando dados de uma api externa com fetch
description: Aplicando fetch
date: 2021-04-08 08:33:30
thumbnail: assets/img/designer.svg
category: ReactJS
background: "#50bbd7"
---
Buscando apenas uma api

```javascript
import { Component } from 'react';

import './App.css';

class App extends Component {
    state = {
      posts: []
    }
    componentDidMount() {
      fetch('https://jsonplaceholder.typicode.com/posts')
      .then(response => response.json())
      .then(posts => this.setState({ posts }))
    }

  render() {

    const { posts } = this.state

    return (
      <div className="App">
        {
          posts.map(post => (
            <div key={post.id}>
              <h2>{post.title}</h2>
              <p>{post.body}</p>
            </div>
          ))
        }
      </div>
    );
  }
}

export default App;

```

```javascript
    state = {
      posts: []
    }
    componentDidMount() {
      fetch('https://jsonplaceholder.typicode.com/posts')
      .then(response => response.json())
      .then(posts => this.setState({ posts }))
    }
```