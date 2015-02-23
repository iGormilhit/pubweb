---
title: Contenu de l'atelier de la semaine 2 
author: iGor
date: 2015-02-17
---

# Contenu de l'atelier de la semaine 2 | 45 min.

## Correction du devoir de la semaine suivante | 5 min.

   Le corrigé est accessible à l'URL suivante : [https://github.com/iGormilhit/pubweb-skeleton/archive/v.0.1.5.zip](https://github.com/iGormilhit/pubweb-skeleton/archive/v.0.1.5.zip).

   Les parties en *italique* ont été réalisées avec la balise `<em></em>`. Celle-ci permet de mettre en évidence une zone de texte dans une ligne. Contrairement aux balises `<hx>`, `<p>` ou `<img src="" alt="" >`, elle ne forme pas un bloc.   
   Par défaut la balise `<em>`, pour *emphasis* utilise l'italique. Pour mettre en gras, il y a la balise `<strong>`.

   En français, il est d'usage d'insérer des espaces insécables entre les guillemets. En `html`, il est nécessaire d'utiliser l'entité `&nbsp;` (pour *non breakable space*).

   Enfin, la liste à puce est réalisée avec la balise `<ul></ul>`, qui indique une liste non ordonnée (non numérotée). À l'intérieur de celle-ci, chaque élément de liste est indiqué par la balise `<li></li>`. Il est nécessaire de bien faire attention à l'imbrication !

## Utilisation du serveur Web local | 7 min.

   1. Faire une copie du dossier `mon-site` dans `P:\config\wwwroot.xamp\` ; démarrer XAMP, le service Apache.
   2. Ouvrir l'URL [`http://localhost:8005/mon-site`](http://localhost:8005/mon-site) et observer les différences avec la page ouverte "directement", principalement la police de caractère, ce qui correspond à la ligne 18 du fichier `index.html`.

## Modification de l'`index.html`.

### Structure de base

   Comme vu la semaine passée, une page `html` est toujours composée des parties principales suivantes :

   * La déclaration : `<!DOCTYPE html>`. Elle est obligatoire.
   * La balise `<html lang="fr"> ... </html>` contenant l'ensemble de la page `html`. Comme vous réalisez un site Web en français, nous pouvons changer la *valeur* de l'*attribut* `lang` de `en` (anglais) à `fr` (français).
   * Le `<head> ... </head>`, qui contient les informations générales du documents (les métadonnées), ainsi que le titre de la page (qui se retrouve sur la barre de la fenêtre ou l'onglet du navigateur), et les liens vers les feuilles de styles (`css`)^[[https://developer.mozilla.org/fr/docs/Web/HTML/Element/head](https://developer.mozilla.org/fr/docs/Web/HTML/Element/head)].
   * Le `<body> ... </body>`, dans lequel se trouve tout le contenu visible de la page Web.

   Dans le `head`, modifiez les balises suivantes :

   * `<title> ... </title> : donnez un titre à votre page Web.
   * `<meta name="description" content="[La description de votre site Web]">`
   * `<meta name="author" content="[Le nom de l'auteur du site Web"]>`

   Toujours dans le `head` se trouvent les balises `<link rel="..." href="...">`. Ce sont des liens qui lient au document `html` d'autres ressources, comme par exemple des polices de caractères, l'image du *favicon* et les feuilles de styles `css` responsables de la mise en forme.

   
### Le `header` et le `footer`

   Le `body` peut être structuré d'une manière assez libre. Le plus souvent pourtant, les sites Web proposent une structure assez classique, avec un en-tête et un pied de page commun à l'ensemble du site, et un contenu principal, qui change d'une page à l'autre.
   
   Depuis `html 5` existent les balises `header` et `footer` qui permettent de réaliser cela. L'en-tête comprendra le plus souvent le titre principale du site Web, ainsi qu'en général son soustitre. Le menu (`<nav></nav>`) est souvent inséré dans cette partie, mais ce n'est pas une obligation.

   Tout au sommet du contenu visible de la page `index.html`, à savoir tout de suite après la balise ouvrante du `body`, insérez l'en-tête suivant (que vous pouvez adapter librement) :

```
<header>
	<a href="/" title="Accueil"><img src="images/logo.svg" alt="Le logo du site est celui du HTML5"></a>
	<h1>Mon magnifique site Web !</h1>
	<h2>Ou comment j'ai appris à faire du Web.</h2>
</header>
```

Puis insérez le pied de page, que vous pouvez également modifier librement, à la fin du contenu visible de cette même page, donc juste avant la balise fermante du corps principal, le `body` :

```
<footer>
	<small>Ce site est sous licence <a href="http://copyheart.org/" title="Site de la licence Copyheart"><em>♡ Copyheart</em></a>.
</footer>
```
