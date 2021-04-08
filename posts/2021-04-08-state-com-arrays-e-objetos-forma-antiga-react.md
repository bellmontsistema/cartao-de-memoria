---
title: State com arrays e objetos - (Forma antiga React)
description: Anotação
date: 2021-04-08 07:14:09
thumbnail: assets/img/designer.svg
category: ReactJS
background: "#50bbd7"
---
```javascript
import { Component } from 'react';

import './App.css';

class App extends Component {
    state = {
      posts: [
        {
          id: 1,
          title: 'Post 1',
          description: 'estou estudando react hoje',
        },
        {
          id: 1,
          title: 'Post 2',
          description: 'vou estudar react Amanhã',
        },
        {
          id: 1,
          title: 'Post 3',
          description: 'vou estudar react o mês todo',
        }
      ]
    }

  render() {

    const { posts } = this.state

    return (
      <div className="App">
        {
          posts.map(post => (
            <div key={post.id}>
              <h2>{post.title}</h2>
              <p>{post.description}</p>
            </div>
          ))
        }
      </div>
    );
  }
}

export default App;

```

![](/assets/img/state-com-arrays-e-objetos-forma-antiga.png)