---
layout: page
title: Balise Picture
---

La balise Picture
===

Exemple:

```html
<picture>
    <source type="image/webp" srcset="chat_mignon.webp">
    <source type="image/jpeg" srcset="chat_mignon.jpg">
    <img src="chat_mignon.jpg" alt="Un chat particulièrement mignon" loading="lazy">
</picture>
```
Note: les attributs "alt" et "loading" ne doivent figurer que sur la balise `<img>`, il n'est pas nécessaire de les dupliquer (voir [discussion Stackoverflow](https://stackoverflow.com/questions/24025464/lazy-loading-html5-picture-element)).

## Avec les images de background

Pour obtenir cette fonctionnalité avec les images de fond chargées en CSS, on peut utiliser la fonction CSS `image-set()`.

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
