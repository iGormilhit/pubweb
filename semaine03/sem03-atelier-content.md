---
title: Contenu de l'atelier de la semaine 3 
author: iGor
date: 2015-03-03
---

# Contenu de l'atelier de la semaine 3 | 45 min.

## Correction du devoir de la semaine suivante | 5 min.

Une proposition de corrigé se trouve à l'URL suivante&nbsp;:   
[https://github.com/iGormilhit/pubweb-skeleton/releases/tag/v.0.2.6](https://github.com/iGormilhit/pubweb-skeleton/releases/tag/v.0.2.6).

Les points à observer&nbsp;:

   * La structure de base est identitique, ainsi que le contenu de la balise `<head>`.
   * La modification du `<title>...</title>`.
   * Au passage, l'URL du lien vers la police (ligne 18).
   * Le `header` et le `nav` n'ont pas changé.
   * C'est la partie principale, l' `<article>` à l'intérieur du `<body>` qui a changé.

Concernant cette partie principale&nbsp;:

   * Ici, elle est elle-même structurée avec un `<header>` et un `<article>`.
   * Elle comprend deux images cliquables. Elles pointent vers le fichiers original sur Flick. Elles sont au format `JPG`. La balise `<img src="" alt="">` forme un bloc.
   * `<code>...</code>` qui permet d'insérer, à l'intérieur d'une ligne du texte en police à chasse fixe, le plus souvent afin d'afficher du code, par exemple une balise `html`&nbsp;;
   * `<abbr title="">` affiche au survol du curseur le développement de l'acronyme.
   * Le logo cliquable.

## Trois feuilles de styles principales

Ce sont des feuilles de styles en cascades, parce qu'il y en a plusieurs :

   1. La feuille de style de l'utilisateur.
   2. La feuille de style du navigateur Web.
   3. La feuille de style du site Web lui-même.

Jusqu'ici, l'ébauche de site Web qui a été réalisé utilise la feuille de style du site Web, celle qui est proposée par le *template* que l'on utilise : `skeleton.css`. Petite démonstration :

   1. Ouvrez la page `index.html` dans un éditeur de texte et dans un navigateur Web.
   2. Commentez les lignes 22 et 23.
   3. Recharger la page Web dans le navigateur.
   4. Que constatez-vous ?
   5. Une fois l'expérience réalisée, n'oubliez pas de réactiver les deux lignes en supprimant le commentaire&nbsp;!

Il est possible de faire également une autre démonstration, avec l'extension pour Firefox *Tranquility*^[[https://addons.mozilla.org/en-US/firefox/addon/tranquility-1/](https://addons.mozilla.org/en-US/firefox/addon/tranquility-1/)]. Le but de cette extension est de supprimer le plus possible le contenu non-textuel d'une page Web, afin d'en améliorer la lecture.

Les règles de styles de ces différentes feuilles sont appliquées selon un ordre de priorité précis. Il en est fait mention au point 1 du document *CSS - Théorie -  Partie A*.

## Lier une feuille de style

Il s'agit d'une balise spécifique, qui se situe *toujours* dans le `<head>` :

```
<link rel="stylesheet" href="css/skeleton.css">
```

Il est possible de lier à une page `html` plusieurs feuilles de style. Le *template* en propose déjà deux :

   * `normalize.css` a pour fonction de mettre à zéro tous les propriétés. Elle n'est pas obligatoire.
   * `skeleton.css` est la feuille de style du *template* lui-même. Il n'est pas nécessaire, ni conseillé, de la modifier.
   * Vous allez ajouter votre feuille de style personnelle, dans laquelle vous pourrez écrire vos propres règles CSS. Vous la nommerez comme bon vous semble, mais l'usage est d'utiliser le nom `style.css`.

D'autres feuilles de styles sont possibles, selon les médias que vous voudriez utiliser : écran, projecteur, mobile, imprimante. Pour cela, il est nécessaire d'ajouter un attribut indiquant le média concerné :

```
<link rel="stylesheet" href="css/print.css" media="print">
```

## Commentaire et syntaxe de base

Ouvrez la feuille de style principale du *template*. On peut voir :

   * Les commentaires : /* --- */ (par exemple de la ligne 29 à 30)
   * La syntaxe de base : `{sélecteur: propriété: variable;}`


Un exemple de règle : 

```
body {
	font-family: "Raleway", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
	color: #222;
}
```

## Création de *votre* feuille de style

Comment feriez-vous ? [Réponse en classe]

Dans la feuille de style que vous venez de créer, vous pouvez commencer par écrire un commentaire expliquant quel est ce fichier, qui l'a créé et éventuellement à quoi il sert. Vous pouvez vous inspirez de ce que vous trouvez dans le fichier `skeleton.css`.

Écrivez une règle pour centrer le texte du `footer`. Arrivez-vous à vous aider du document *Cascading Style Sheets (CSS3)* ?

```
footer {
	text-align: center;
}
```

## Les sélecteurs

Cette règle utilise un sélecteur de balise : `footer` renvoie à la balise `<footer>`. Elle s'applique dont à **toutes** les balises `<footer>` de votre site Web. Il est existe donc un sélecteur pour chaque balise `html`.

Écrivez ensuite une règle s'appliquant à l'élément *image*, afin d'entourer chaque image d'une bordure de 1px, arrondie sur les côtés.

```
img {
	border-width: 1px;
	border-style: solid;
	border-radius: 20px;
}
```

Pour cette règle, c'est encore le sélecteur de balise qui est utilisé. Les propriétés modifiées sont la largeur de la bordure, son style, et la courbure dans les angles. Vous pouvez vous référez aux *Quick Reference* ou au document en ligne *CSS Reference*^[[http://tympanus.net/codrops/css_reference](http://tympanus.net/codrops/css_reference)] pour découvrir les différents styles de bordures existants.

Avec le sélecteur choisi, cette règle s'applique à toutes les images du site Web, dont le logo du `header`. Pour appliquez une règle seulement à ce logo, une possibilité est d'utiliser un sélecteur d'identifiant.

Pour cela, il faut d'abord modifier le code `html`, à la fois dans le fichier `index.html` et `apropos.html`. Trouvez la ligne suivante (ce devrait être la ligne 40) :

```
<a href="index.html" "Retour à l'accueil"><img src="images/logo.svg" alt="le logo HTML5" title="le logo HTML5"></a>
```

Ajoutez à la balise `<img>` l'attribut `id=""` et donnez-lui la valeur "logo" :

```
<a href="index.html" "Retour à l'accueil"><img src="images/logo.svg" alt="le logo HTML5" title="le logo HTML5" id="logo"></a>
```

Il est nécessaire de répéter cette modification dans toutes les pages `html` de votre site. Une fois cela fait, il est désormais possible de créer un sélecteur spécifique à l'image de l'en-tête :

```
#logo {
	width: 6em;
	border: none;
	border-radius: 0px;
}
```

Le dièse signifie qu'il s'agit d'un sélecteur d'identifiant. L'identifiant ici étant bien "logo", le "nom" qui a été choisi pour *identifier* le logo. Les règles suivantes servent à remettre à zéro les règles qui s'appliquent aux images en général.


