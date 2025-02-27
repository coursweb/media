---
layout: page
title: Lazy load
---

La technique du "lazy load" consiste à ne charger des ressources que lorsqu'elles sont nécessaires pour l'affichage visible.

Ainsi, des images qui se situent "hors-champ" lors du chargement initial, ne seront chargées que lorsque le scroll les fait entrer dans la zone visible à l'écran.

Cette méthode a été utilisée depuis de nombreuses années en ayant recours à des solutions JavaScript.

Désormais, un attribut HTML a été défini, qui est progressivement adopté par les navigateurs - [voir l'état actuel sur CanIUse](https://caniuse.com/loading-lazy-attr). L'attribut est supporté notamment:

- Depuis 2019 dans Chrome (77)
- Depuis 2020 dans Edge (79)
- Depuis 2020 dans Firefox (75)
- Depuis 2022 dans Safari (15.4)
- Depuis décembre 2022 dans Chrome pour Android (108)

En 2024, cet attribut est pris en compte dans 95.57% des navigateurs!

## Comment l'utiliser

Il suffit d'ajouter un attribut `loading="lazy"` à la balise `img`. Exemple:

```html
<img src="image.png" loading="lazy" alt="…" width="200" height="200">
```

C'est tout 😄 ! Cet attribut indique au navigateur de ne déclencher le chargement qu'au moment où l'image devient visible. Vous améliorez ainsi la performance de votre site, car le chargement initial est accéléré.

## Ressources

- CanIUse: [https://caniuse.com/loading-lazy-attr](https://caniuse.com/loading-lazy-attr) - l'état du support des navigateurs.
- web.dev [https://web.dev/browser-level-image-lazy-loading/](https://web.dev/browser-level-image-lazy-loading/) - article très complet sur la manière d'utiliser le Lazy Load.
