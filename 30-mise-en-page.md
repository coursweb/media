---
layout: page
title: Mise en page
---

### Les CSS backgrounds

Pour les images placées en "Background" via CSS, il est possible de préciser la taille avec les mots-clés "cover" et "contain". Un exemple de code qui applique une image de fond:

```
.bg {
  background-image: url("https://1904.cc/i/clouds.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
```

<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="vEYgXPO" data-editable="true" data-user="eracom" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/eracom/pen/vEYgXPO">
  CSS Background</a> by Manuel Schmalstieg (<a href="https://codepen.io/eracom">@eracom</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

* Voir: [HTML Background Images sur W3Schools](https://www.w3schools.com/html/html_images_background.asp)

### La propriété object-fit

La propriété `object-fit` permet d'appliquer le mode "cover" ou "contain" sur des images ou vidéo dans le HTML (qui ne sont pas chargées par la propriété "background-image").
Une propriété CSS longtemps attendue, qui permet de spécifier comment une image (ou vidéo) doit s'adapter à son conteneur. 

Les valeurs possibles sont: 

* `fill` : déformation de l'image, pour remplir le cadre à tout prix.
* `contain` : essaie de remplir le cadre tout en gardant toute l'image visible, en la rapetissant s'il le faut.
* `cover` : masquage partiel de l'image, pour remplir entièrement le cadre, sans déformation.
* `scale-down` : l'image se rétrécit pour rentrer dans le cadre. Peut se comporter comme contain.
* `none` : comportement classique, affichage de l'image à taille réelle des pixels.

Exemples : 

* [Exemple interactif sur Mozilla.org](https://developer.mozilla.org/fr/docs/Web/CSS/object-fit)

<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="YPzNpPy" data-editable="true" data-user="eracom" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/eracom/pen/YPzNpPy">
  object-fit</a> by Manuel Schmalstieg (<a href="https://codepen.io/eracom">@eracom</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>


## Explication du object-fit sur Debug TV 

<iframe width="100%" style="aspect-ratio: 16 / 9;" src="https://www.youtube-nocookie.com/embed/y65JkO8-QaQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Dans l'épisode 4 de [Debug TV](https://www.youtube.com/playlist?list=PLlfJkWGxh-q2AueB9twTsnATiCH0W3kEB), Adrien Cater explique les propriétés `object-fit` et `aspect-ratio`.
