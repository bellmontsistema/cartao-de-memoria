---
title: Ziper de API
description: Juntando dados de uma api em outra
date: 2021-04-09 06:30:43
thumbnail: assets/img/designer.svg
category: Javascript
background: "#FEC748"
---
![](assets/img/ziper-de-api.png)

Simplesmente fazer um `map` de um aí dando espalhamento `(Spread)` de todo seu `index` em um bloco de código e adicionado um `index` da outra `api` junto.

```javascript
import { Component } from "react";

import "./App.css";

class App extends Component {
  state = {
    posts: [],
  };

  componentDidMount() {
    this.loadPosts()
  }

  loadPosts = async () => {
    const postsResponse = fetch('https://jsonplaceholder.typicode.com/posts')
    const photosResponse = fetch('https://jsonplaceholder.typicode.com/photos')

    const [posts, photos] = await Promise.all([postsResponse, photosResponse])

    const postsJson = await posts.json()
    const photosJson = await photos.json()

    const postsAndPhotos = postsJson.map((post, index) => {
      return { ...post, cover: photosJson[index].url}
    })

    this.setState({posts: postsAndPhotos})
  }

  render() {
    const { posts } = this.state;

    return (
      <section className="container">
        <div className="posts">
          {posts.map((post) => (
            <div className="post">
              <img src={post.cover} alt=""/>
              <div key={post.id} className="post-content">
                <h2>{post.title}</h2>
                <p>{post.body}</p>
              </div>
            </div>
          ))}
        </div>
      </section>
    );
  }
}

export default App;
```