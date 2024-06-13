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
    <img src="chat_mignon.jpg" alt="My Image">
</picture>
```

## Support dans les navigateurs 

La balise picture est supportée dans quasiment tous les navigateurs, [selon CanIUse](https://caniuse.com/#feat=picture).

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
