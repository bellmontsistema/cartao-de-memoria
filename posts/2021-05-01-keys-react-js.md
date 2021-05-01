---
title: Keys React JS
description: O JSX necessita de uma key única para cada elemento da Array.
  https://reactjs.org/docs/lists-and-keys.html
date: 2021-04-30 09:31:39
thumbnail: https://miro.medium.com/max/3840/1*vHHBwcUFUaHWXntSnqKdCA.png
category: ReactJS
background: "#50bbd7"
---
```javascript
const App = () => {
  const empresas = [<li key="e1">Apple</li>, <li key="e2">Google</li>];

  return <ul>{empresas}</ul>;
};

```