---
layout: page
title: Guia de Estilo
description: Este é um guia de estilo do tema Scriptor Jekyll
---

Este é um parágrafo. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, commodo vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. Donec non enim in turpis pulvinar facilisis. Ut felis.

# Título 1

**Quisque facilisis erat a dui**. Nam malesuada ornare dolor. Cras gravida, diam sit amet rhoncus ornare, erat elit consectetuer erat, id egestas pede nibh eget odio. Proin tincidunt, velit vel porta elementum, magna diam molestie sapien, non aliquet massa pede eu diam. Aliquam iaculis. Fusce et ipsum et nulla tristique facilisis.

## Título 2

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero.

### Título 3

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero.

#### Título 4

Quisque facilisis erat a dui. Nam malesuada ornare dolor. Cras gravida, diam sit amet rhoncus ornare, erat elit consectetuer erat, id egestas pede nibh eget odio. Proin tincidunt, velit vel porta elementum, magna diam molestie sapien, non aliquet massa pede eu diam. Aliquam iaculis.

##### Título 5

Curabitur pellentesque facilisis orci, ut rhoncus nulla scelerisque ac. Integer in magna vel justo venenatis ornare vitae vel sem.

###### Título 6

Nulla tempus tortor nec nunc volutpat commodo. Vivamus efficitur imperdiet velit sagittis pellentesque. In fringilla dui nec dolor sollicitudin, et scelerisque elit pellentesque. Integer vestibulum viverra sem, vel ornare nibh. Proin lobortis elit nunc, ut consequat elit vulputate sit amet.

## Ênfase

**Este é um texto em negrito**

*Este é um texto em itálico*

~~Texto tachado~~

## Links

[Sou um link no estilo inline](https://www.google.com)

[Sou um link no estilo inline com título](https://www.google.com "Página inicial do Google")

## Citação

>"A criatividade é permitir que você mesmo cometa erros. Design é saber quais manter."

Lorem ipsum dolor sit amet, `consectetuer adipiscing` elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero.

***

## Blocos de Código

```css
#header h1 { 
  color: #fff;
  margin-bottom: 1.5em; 
}

.author-avatar {
  border-radius: 5px;
  display: block;
  height: 60px;   
  margin-right: 30px;
  width: 60px;
}
```

```javascript
// Mapa simples
var map;
function initMap() {
  map = new google.maps.Map(document.getElementById('map'), {
    center: {lat: -34.397, lng: 150.644},
    zoom: 8
  });
}
```

```json
{"menu": {
  "id": "file",
  "value": "File",
  "popup": {
    "menuitem": [
      {"value": "New", "onclick": "CreateNewDoc()"},
      {"value": "Open", "onclick": "OpenDoc()"},
      {"value": "Close", "onclick": "CloseDoc()"}
    ]
  }
}}
```

```yml
sass:
  input_file: sass/main.scss.njk
  output_file: assets/css/main.css
  indentWidth: 4
  outputStyle: nested
  precision: 10
```

```
Nenhuma linguagem indicada, então nenhum destaque de sintaxe.
```

`Código` inline tem `crases ao redor`.

## Vídeos

<iframe src="https://player.vimeo.com/video/153339497?byline=0" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

[Terraforming](https://vimeo.com/153339497) por [Studio Swine](https://vimeo.com/studioswine) no [Vimeo](https://vimeo.com)

## Imagem em Largura Total

Imagens também funcionam! Já sabe a URL da imagem que quer incluir no seu artigo? Basta colá-la assim para fazê-la aparecer:

{% include image_full.html imageurl="/images/apple-watch-in-car.jpg" title="Apple" caption="Esta é a legenda" %}

Lorem ipsum dolor sit amet, `consectetuer adipiscing` elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero.

## Imagem Normal

{% include image_caption.html imageurl="/images/apple-watch-in-car.jpg" title="Apple Super" caption="Esta é a legenda" %}

Lorem ipsum dolor sit amet, `consectetuer adipiscing` elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero. Lorem ipsum dolor sit amet, `consectetuer adipiscing` elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero.

## Listas

Aqui está uma lista não ordenada de itens, tipicamente renderizada como uma lista com marcadores:

+ Donec non tortor in arcu mollis feugiat
+ Lorem ipsum dolor sit amet, consectetuer adipiscing elit
+ Donec id eros eget quam aliquam gravida
+ Vivamus convallis urna id felis
+ Nulla porta tempus sapien

Aqui está uma lista ordenada de itens, tipicamente renderizada como uma lista numerada:

1. Donec non tortor in arcu mollis feugiat
2. Lorem ipsum dolor sit amet, consectetuer adipiscing elit
3. Donec id eros eget quam aliquam gravida
4. Vivamus convallis urna id felis
5. Nulla porta tempus sapien

### Tabelas

| Título | Título |
| ------| ----- |
| Texto  | Texto  |
| Texto  | Texto  |
| Texto  | Texto  |
