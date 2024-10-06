---
layout: page
title: Balise Picture
---

La balise Picture
===

La balise `<picture>` est un élément d'image adaptative. Elle permet de définir plusieurs plusieurs éléments source. On peut ainsi proposer des résolutions différentes, ou des formats d'image alternatifs (voir [WebP, AVIF etc]()). 

Cette balise est acceptée par l'ensemble des navigateures depuis 2016.

Exemple pour proposer différents formats d'image (Avif et WebP).

```html
<picture>
    <source 
      srcset="chat_mignon.avif" 
      type="image/avif">
    <source 
      srcset="chat_mignon.webp"
      type="image/webp">
    <img 
      src="chat_mignon.jpg" 
      alt="Un chat très mignon" 
      loading="lazy"
      width="360" 
      height="240">
</picture>
```

On utilise le JPG comme format par défaut (*fallback*).

**Note:** les attributs "alt", "loading", "width" et "height" ne doivent figurer que sur la balise `<img>`, il n'est pas nécessaire de les dupliquer (voir [discussion Stackoverflow](https://stackoverflow.com/questions/24025464/lazy-loading-html5-picture-element)).

Un autre exemple pour proposer des images dans différentes résolutions, adaptées la taille de l'écran:

```html
<picture>
  <source 
    media="(min-width: 650px)"
    srcset="kitten-stretching.png">
  <source 
    media="(min-width: 465px)"
    srcset="kitten-sitting.png">
  <img 
    src="kitten-curled.png" 
    alt="a cute kitten">
</picture>
```

## Avec les images de background

Pour obtenir cette fonctionnalité avec les images de fond chargées en CSS, on peut utiliser la fonction CSS `image-set()`. Cette méthode permet au navigateur de sélectionner l'image la plus appropriée parmi un ensemble d'images.

Exemple:

```css
.box {
  background-image: image-set(
    "large-balloons.avif" type("image/avif"),
    "large-balloons.jpg" type("image/jpeg")
  );
}

```

Voir [plus d'infos sur MDN](https://developer.mozilla.org/fr/docs/Web/CSS/image/image-set).
