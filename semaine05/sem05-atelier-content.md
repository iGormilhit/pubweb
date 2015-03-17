---
title: Contenu de l'atelier de la semaine 4 
author: iGor
date: 2015-03-09
---

# Contenu de l'atelier de la semaine 5 | 45 min.

## Corrigé du devoir

Le corrigé est accessible à l'URL suivante : [https://github.com/iGormilhit/pubweb-skeleton/archive/v.0.4.5.zip](https://github.com/iGormilhit/pubweb-skeleton/archive/v.0.4.5.zip).

   1. Ajout d'une image, ici au format SVG dans le répertoire `images/`.
   2. Ajout d'une classe aux liens externes : `class="externe"`.
   3. Rédaction de règles CSS au sélecteur `.externe` ou `a.externe`.

La règle :

```
a.externe {
	background-position: right top;
	background-repeat: no-repeat;
	background-image: url(../images/lien-externe.svg);
	background-size: 8px;
	padding-right: 10px;
}
```

## Sélecteurs, suite et fin.

**Sélecteur universel** : `*`. S'applique à tout les éléments HTML, identifiants, classes et pseudo-classes. Il n'est pas très utilisé.

**Sélecteur composé** :

   * `li a`
   * `ul > li`
   * `a.externe`

**Sélecteur de pseudo-classe** : les pseudo-classes correspondent à des événements, par exemple le fait de survoler un élément avec le curseur, d'activer un lien, d'avoir visité un lien, etc. Elles sont listées sur *CSS Reference* : [http://tympanus.net/codrops/css_reference/#section_css-pseudo-class](http://tympanus.net/codrops/css_reference/#section_css-pseudo-class).

Pour appliquer une règle aux liens qui ont été visités, le sélecteur est le suivant : `a:visited`. Il est possible d'afficher les règles s'appliquant à une pseudo-classe dans l'inspecteur de *Firefox* au moyen d'un clic-droit sur la balise.

## Rappel de la boîte

Comment pouvez-vous expliquer la notion de boîte en HTML ?

## Les propriétés d'affichage des boîtes

*Correspond au point 3.1 du document* CSS - Théorie - Partie B.

Les boîtes s'affiche par défaut soit en blocs, l'une au-dessus de l'autre (`<p>`, `<h1>`, `<footer>`, `<img>`, etc.), soit en ligne, l'une à côté de l'autre (`<a href="">...</a>`, `<em>`, etc.). Il est possible de modifier ce comportement, grâce à la propriété `display` :

```
img {
	display: inline;
}

a {
	display: block;
}
```

La propriété `display` possède un grand nombre de valeur et notamment `none`, qui signifie que l'élément n'est pas affiché. Essayez d'escamoter temporairement les images avec cette méthode, en passant par l'inspecteur.

## Le positionnement des boîtes

*Correspond au point 3.2 du document* CSS - Théorie - Partie B.

Voir aussi la documentation sur le *Mozilla Developper Network* : [https://developer.mozilla.org/fr/docs/Web/CSS/position](https://developer.mozilla.org/fr/docs/Web/CSS/position)

Par défaut, les blocs (ou boîtes) se positionne les uns après les autres. Il est possible de modifier ce comportement avec la propriété `position` qui peut prendre les valeurs suivantes : `relative`, `absolute`, `fixed` (entre autres).

Pour les valeurs `absolute` et `fixed`, l'élément (le bloc ou la boîte) n'a pas d'espace attribué, ce qui signifie que si l'on ne détermine pas des marges, il chevauchera les autres éléments. La position `fixed` place l'élément en fonction de la fenêtre du navigateur, alors que la position `absolute` situe l'élément en fonction de l'élément le plus proche.

Afin d'observer ce qui se passe, essayez, au moyen de l'inspecteur, d'attribuer une position `fixed` ou `absolute` à un élément, par exemple au `<header>`.

La position `relative` ajuste les éléments les uns par rapport aux autres, en leur attribuant l'espace nécessaire.

## Le flottement

*Correspond au point 3.3 du document* CSS - Théorie - Partie B.

`float` est une propriété qui extrait un élément du positionnement normal de la page, afin de le faire flotter. L'élément peut flotter à droite ou à gauche :

```
img {
float: right;
}

img {
float: left;
}
```
## Applications pour mieux placer les images. 

Dans le corrigé que j'ai propos, les images ne s'adaptent pas à la taille de l'écran (vérifiez avec le ctrl+maj+m). Pour le faire, il est possible d'ajouter la règle suivante au sélecteur `img` : `width: 100%;`. Ainsi, l'image prendra toute la largeur disponible dans l'élément qui la contient, ce qui est parfait lorsque la taille de l'écran diminue.

Par contre, lorsque la taille de l'écran est au maximum, alors l'image est exagérément agrandie. Pour contourner ce problème, vous pouvez fixer une largeur maximale à l'image : `max-width: 600px;`

Comment feriez-vous pour place le logo à la même hauteur que le titre de l'en-tête ? Et pour améliorer le placement de l'en-tête du site Web ?

# Devoir de la semaine 05

Créez une nouvelle page, en remplaçant la partie principale de votre page par un ensemble d'images. Essayez de disposer les images sous la forme d'une galerie simple, en vous aidant des propriétés de positionnement et d'affichage des boîtes.

Pensez à mettre à jour les menu des autres pages, ce qui nous permettra de nous attaquer à la mise en forme du menu.
