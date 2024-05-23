---
layout: page
title: WebP, AVIF etc
permalink: format-webp.html
---

Le format WebP est un format d'image développé et mis à disposition par Google. Il est destiné à remplacer les formats JPEG et PNG. A qualité égale, le format propose des images d'environ 30% plus légères. Le format permet de produire des images sans perte (comme le PNG) ou compressées (comme le JPEG), autorise la transparence et les images animées.

## Exporter des WebP

Les images peuvent être exportées au format WebP depuis ces logiciels:

- [Squoosh](https://squoosh.app/), web app de compression d'images créée par Google, permettant de choisir des formats comme WebP, AVIF, JPEG XL...
- [Just Gimme an IMG](https://just-gimme-an-img.vercel.app/), outil web pour optimiser des images et obtenir le code HTML pour les insérer.
- [Sketch](https://www.sketch.com/)
- Pixelmator
- Google [propose une extension](https://developers.google.com/speed/webp/docs/webpshop) pour l'export depuis Photoshop.

## Support dans les navigateurs

Entre 2018 et 2019, la prise en charge du format WebP est arrivée dans les navigateurs Chrome, Edge et Firefox. Le navigateur Safari offre une prise en charge depuis la version 14 (parue en 2020) sur iOS et macOS Big Sur. Le support actuel pour être vérifié [sur le site CanIUse](https://caniuse.com/webp) (95% en fin 2022).

En 2021, le CMS WordPress ajoute la prise en charge du format WebP ([lire l'annonce](https://make.wordpress.org/core/2021/06/07/wordpress-5-8-adds-webp-support/)).

## Support dans MacOS

Pour pouvoir afficher les images WebP dans le finder, il est nécessaire d'installer un utilitaire. Vous trouverez des informations [sur StackOverflow](https://apple.stackexchange.com/questions/285698/webp-support-on-macos-is-it-indended-to-actually-work).

## Autres formats de nouvelle génération

- **AVIF**. Nouveau format open-source, qui offre généralement une meilleure compression que WebP, JPEG, PNG et GIF. En compétition avec JPEG XL. Voir [support actuel sur CanIUse](https://caniuse.com/avif) (78% en fin 2022).
- **JPEG XL**. Un format "conçu pour être plus efficace que les formats existants". Voir [support actuel sur CanIUse](https://caniuse.com/jpegxl) (aucun support natif en fin 2022).

Autres formats de compression:

- **HEIC** (High Efficiency Image File Format). Apple l'a déployé en 2017 comme format par défaut pour les photos avec iOS 11, et le présente comme 2 fois plus petit qu'une image équivalente en JPEG.  
- **JPEG 2000**. Alternative au JPEG, avec des options "lossless". Jamais largement adopté, ce format n'est pas pris en charge par la plupart des navigateurs. Utilisé dans certaines industries comme format d'archivage. Lire [l'article Wikipédia](https://fr.wikipedia.org/wiki/JPEG_2000).

## Utiliser la balise Picture

Pour les formats ayant un support partiel, c'est une excellente idée de les intégrer avec un "fallback" au moyen de la balise HTML `picture`. Exemple:

```html
<picture>
 <source srcset="img/photo.avif" type="image/avif">
 <source srcset="img/photo.webp" type="image/webp">
 <img src="img/photo.jpg" alt="Description" width="360" height="240">
</picture>
```

## Voir aussi

- [Un article](https://www.smashingmagazine.com/2021/09/modern-image-formats-avif-webp/) comparant WebP et AVIF dans Smashing Magazine. AVIF donne de meilleurs résultats.
- [Just Gimme an IMG](https://just-gimme-an-img.vercel.app/), outil web pour optimiser des images et obtenir le code HTML pour les insérer.
- [Squoosh](https://squoosh.app/), web app de compression d'images créée par Google, permettant de choisir des formats comme WebP, AVIF, JPEG XL...