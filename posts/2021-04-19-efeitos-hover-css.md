---
title: Efeitos HOVER CSS
description: Efeitos HOVER CSS
date: 2021-04-19 03:23:18
thumbnail: https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/120px-CSS3_logo_and_wordmark.svg.png
category: CSS
background: "#529DC4"
---
## 1 - Efeito Rotate

```css
<style>
.imagem1{
    transition: all 1s;
    cursor: pointer;
}

.imagem1:hover{
    -webkit-transform: rotateZ(360deg);
    transform: rotateZ(360deg);
}
</style>
```

## 2 - Efeito Filter Blur

```css
<style>
.imagem2{
    transition: all 0.5s;
    cursor: pointer;
}

.imagem2:hover{
    -webkit-filter: blur(5px);
    filter: blur(5px);
}
</style>
```

## 3 - Efeito Scale

```css
<style>
.imagem3{
    transition: all 0.5s;
    cursor: pointer;
}

.imagem3:hover{
    -webkit-transform: scale(1.5);
    transform: scale(1.5);
}
</style>
```

## 4 - Efeito Drop Shadow

```css
<style>
.imagem4{
    transition: all 0.5s;
    cursor: pointer;
}

.imagem4:hover{
    -webkit-filter: drop-shadow(15px 10px 5px rgba(0,0,0,.5));
    filter: drop-shadow(15px 10px 5px rgba(0,0,0,.5));
}
</style>
```

## 5 - Efeito border e border-radius

```css
<style>
.imagem5{
    transition: all .5s;
    border: 10px solid transparent;
}
.imagem5:hover{
    border: 10px solid #136497;
    border-radius: 50%;
}
</style>
```

## Extra - Todos Efeitos Juntos (menos o BLUR)

```css
<style>

.imagem6{
    transition: all .5s;
    border: 10px solid #eeeeee;
}
.imagem6:hover{
    border: 10px solid #781f40;
    border-radius: 50%;
    -webkit-filter: drop-shadow(15px 7px 1px rgba(0,0,0,.5));
    filter: drop-shadow(15px 7px 1px rgba(0,0,0,.5));
    -webkit-transform: rotateZ(-360deg) scale(1.5);
    transform: rotateZ(-360deg) scale(1.5);
}

</style>
```