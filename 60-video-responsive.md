---
layout: page
title: Vidéo responsive
permalink: video-responsive.html
---

## Méthode pour les balises `<video>`

En utilisant une balise `<video>`: code css pour que votre vidéo soit en pleine largeur et responsive: 

```css
video {
	width: 100% !important;
	height: auto !important;
}
```

Source: [w3schools.com](https://www.w3schools.com/css/css_rwd_videos.asp)

## Méthode responsive pour les IFRAME

Si vous importez une vidéo depuis Youtube ou Vimeo, le code fourni comporte une balise "iframe". Cette balise ne pourra pas automatiquement se mettre à la hauteur de la vidéo, il faut donc appliquer une astuce. 

Depuis 2021 ([selon caniuse](https://caniuse.com/mdn-css_properties_aspect-ratio)), on peut utiliser très simplement la propriété `aspect-ratio`:

```css
.video-iframe {
  width: 100%;
  aspect-ratio: 16 / 9;
}
```

Auparavant, une méthode (légèrement plus compliquée) utilisant le "padding-top" était une solution souvent utilisée. Cette méthode "fluid-width video" a été décrite sur le site [CSS Tricks](https://css-tricks.com/fluid-width-video/).

## Insérer (une vidéo en background) depuis Youtube ou Vimeo

Collection d’exemples: [https://github.com/eracom/yt-video-bg](https://github.com/eracom/yt-video-bg)

