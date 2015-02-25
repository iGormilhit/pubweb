---
title: Contenu de l'atelier de la semaine 2 
author: iGor
date: 2015-02-17
---

# Contenu de l'atelier de la semaine 2 | 45 min.

## Correction du devoir de la semaine suivante | 5 min.

   Le corrigé est accessible à l'URL suivante : [https://github.com/iGormilhit/pubweb-skeleton/archive/v.0.1.5.zip](https://github.com/iGormilhit/pubweb-skeleton/archive/v.0.1.5.zip).

   Les parties en *italique* ont été réalisées avec la balise `<em></em>`. Celle-ci permet de mettre en évidence une zone de texte dans une ligne. Contrairement aux balises `<hx>`, `<p>` ou `<img src="" alt="" >`, elle ne forme pas un bloc.   
   Par défaut la balise `<em>`, pour *emphasis*, utilise l'*italique*. Pour mettre en **gras**, il y a la balise `<strong>`.

   En français, il est d'usage d'insérer des espaces insécables entre les guillemets. En `html`, il est nécessaire d'utiliser l'entité `&nbsp;` (pour *non breakable space*).

   Enfin, la liste à puce est réalisée avec la balise `<ul></ul>`, qui indique une liste non ordonnée (non numérotée). À l'intérieur de celle-ci, chaque élément de liste est indiqué par la balise `<li></li>`. Il est nécessaire de bien faire attention à l'imbrication !

## Modification de l'`index.html`

### Structure de base | 7 min.

   Comme vu la semaine passée, une page `html` est toujours composée des parties principales suivantes :

   * La déclaration : `<!DOCTYPE html>`. Elle est obligatoire.
   * La balise `<html lang="fr"> ... </html>` contenant l'ensemble de la page `html`. Comme vous réalisez un site Web en français, vous pouvez changer la *valeur* de l'*attribut* `lang` de `en` (anglais) à `fr` (français).
   * Le `<head> ... </head>`, qui contient les informations générales du document (les métadonnées), ainsi que le titre de la page (qui se retrouve sur la barre de la fenêtre ou l'onglet du navigateur), et les liens vers les feuilles de style (`css`)^[[https://developer.mozilla.org/fr/docs/Web/HTML/Element/head](https://developer.mozilla.org/fr/docs/Web/HTML/Element/head)].
   * Le `<body> ... </body>`, dans lequel se trouve tout le contenu visible de la page Web.

   Dans le `head`, modifiez les balises suivantes :

   * `<title> ... </title>` : donnez un titre à votre page Web, et vérifiez que les changements que vous apportez sont visibles.
   * `<meta name="description" content="[La description de votre site Web]">`.
   * `<meta name="author" content="[Le nom de l'auteur du site Web"]>`.

   Toujours dans le `head` se trouvent les balises `<link rel="..." href="...">`. Elles relient au document `html` d'autres ressources, comme par exemple des polices de caractères, l'image du *favicon* et les feuilles de styles `css` responsables de la mise en forme.
   
### Le `header` et le `footer` | 17 min.

   Le `body` peut être structuré d'une manière assez libre. Le plus souvent pourtant, les sites Web proposent une structure assez classique, avec un en-tête et un pied de page commun à l'ensemble du site, et un contenu principal, qui change d'une page à l'autre.
   
   Depuis `html 5`, les balises `header` et `footer` permettent de réaliser cela. L'en-tête comprendra le plus souvent le titre principal du site Web, ainsi qu'en général son soutitre. Le menu (`<nav></nav>`) est souvent inséré dans cette partie, mais ce n'est pas une obligation.

   Tout au sommet du contenu visible de la page `index.html`, à savoir tout de suite après la balise ouvrante du `body`, insérez l'en-tête suivant (que vous pouvez adapter librement) :

```
<header>
	<h1>Mon magnifique site Web !</h1>
	<h2>Ou comment j'ai appris à faire du Web.</h2>
</header>
```

On trouve souvent dans l'en-tête d'un site Web une image constituant le logo du site Web. En `html`, il est possible d'insérer des images avec la balise `<img>`. Celle-ci a plusieurs particularités :

   1. Elle est *auto-fermante*. Tout son contenu est dans la balise ; elle ne se termine pas par `</img>`.
   2. Elle contient un *attribut* **obligatoire** : `src=""`, c'est-à-dire la *source* de l'image, dont la *valeur* indique où le serveur Web doit aller chercher l'image à afficher.
   3. Elle contient également au moins un autre *attribut*, qui n'est pas obligatoire, mais fortement conseillé : `alt=""`. La valeur de cet *attribut* est constitué d'un court texte descriptif remplaçant l'image si elle ne peut être affichée.

Les formats d'images qui peuvent être insérés sont principalement le JPG, le PNG, le GIF et le SVG. Ce point fera l'objet d'un cours complet.

Pour l'exercice, utilisez le logo officiel du HTML 5^[Le HTML 5 est une recommandation du W3C depuis le 23 octobre 2014 : [http://www.w3.org/blog/news/archives/4167](http://www.w3.org/blog/news/archives/4167).], disponible sur *Wikipedia* : [https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg](https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg). Téléchargez le fichier SVG et enregistrez-le dans le dossier *images* du répertoire de votre site Web, **avec le nom logo.svg**.

Entre la balise `<header>` et le titre principal du site Web, insérez une ligne avec le contenu suivant (ligne commençant par `<img...`) :

```
<header>
	<img src="images/logo.svg" alt="[courte description]">
	<h1>Mon magnifique site Web !</h1>
	<h2>Ou comment j'ai appris à faire du Web.</h2>
</header>
```

La valeur de l'attribut `src=""` est un chemin *relatif* qui mène à l'image à insérer. Il est dit *relatif*, parce qu'il s'agit du chemin à parcourir dans la structure **physique** du site Web, depuis le point où est situé le code actuel. En l'occurrence, le fichier qui est édité, `index.html` est à la *racine* de notre site Web. Il suffit donc d'aller dans le dossier `images` pour trouver le fichier `logo.svg` : `images/logo.svg`. Ce point sera vu plus en détail plus tard.

Puis insérez le pied de page, que vous pouvez également modifier librement, à la fin du contenu visible de cette même page, donc juste avant la balise fermante du corps principal, le `body` :

```
<footer>
	<small>Ce site est sous licence <a href="http://copyheart.org/" title="Site de la licence Copyheart"><em>Copyheart</em></a>.</small>
</footer>
```

Ce `footer` contient un lien hypertexte. Il s'agit de la balise `<a> ... </a>`. Celle-ci possède :

   1. Un attribut **obligatoire**, `href=""`, dont la valeur est la cible du lien. Cette cible peut être un lien relatif, comme cela a été vu dans le cas de l'image du logo, ou un lien absolu, comme c'est le cas ici : d'où que l'on se situe, la valeur `http://copyheart.org/` pointe toujours au même endroit.
   2. Un attribut facultatif, mais fortement conseillé, `title=""`, dont la valeur est un texte bref informant le visiteur sur la nature du lien. Elle est particulièrement utile pour les visiteurs visuellement déficients, comme cela sera vu lors d'un cours sur l'accessibilité.

### `<article>` comme contenant principal | 2 min.

   En plus de l'en-tête et du pied de page, une page Web comprend le contenu principal. Le HTML5 propose une balise pour ce contenu : `<article> ... </article>`. Un article peut contenir un article, et même un en-tête et un pied de page. Un article est une réalité un &laquo; contenu autonome &raquo;^[[https://developer.mozilla.org/fr/docs/Web/HTML/Element/article](https://developer.mozilla.org/fr/docs/Web/HTML/Element/article)].

   Insérez juste après le `header` la ligne suivante, y compris l'attribut `class="container"` dont on verra l'utilité plus tard :

   ```
   <article class="container">
   ```

   Fermez cette balise juste avant le `footer`, afin d'imbriquer l'essentiel du contenu de la page Web dans la balise `<article>`.

### Le menu | 12 min.

   Il manque encore à cette page un menu permettant de lier la page d'accueil aux autres pages du site Web. Pour l'instant, ce menu doit comporter deux entrées :

   * Un lien vers la page d'accueil.
   * Un lien vers une page présentant le site Web, par exemple une page &laquo; à propos &raquo;.

   En `html 5` le menu peut être inséré à l'intérieur de la balise `<nav> ... </nav>`, pour *navigation*. Habituellement, les menus sont structurés avec des listes non-numérotées (`<ul>`). Bien entendu, d'autres méthodes sont possibles.

   Ces deux entrées de menu sont en réalité des liens hypertextes (`<a href=""> ... </a>`. Comme ces deux liens pointent vers des ressources internes au site Web, il est préférable (et obligatoire dans le cas de votre mini-site) d'utiliser une référence relative.

   Pour des raisons propres au *template* *Skeleton*, il faut encore imbriquer le menu dans une balise `<div class="container"> ... </div>`, ce qui sera expliqué plus tard.

   Insérez donc le code suivant, constituant le menu, entre le `header` et le contenu principal de la page (`article`) :

```
<div class="container">
	<nav>
		<ul>
			<li><a href="index.html" title="Retour à l'accueil">Accueil</a></li>
			<li><a href="apropos.html" title="Vers l'à propos">À propos</a></li>
		</ul>
	</nav>
</div>
```

# Devoir pour la semaine suivante | 2 min.

Réalisez la page `apropos.html`. Celle-ci doit contenir :

   * La déclaration.
   * La structure de base : `html`, `head` et le `body`, avec les adaptations nécessaires.
   * Un body comprenant le `header`, le `footer`, le `nav` et le contenu principal.
   * Essayez de rendre le logo de l'en-tête cliquable. Il doit pointer vers la page d'accueil.
   * Le contenu principal doit avoir au moins 2 niveau de titre et 2 paragraphes.
   * Essayez d'insérer au moins une image (en format JPG ou PNG), ainsi qu'un lien externe (en plus des liens existants dans le menu).

Soyez également attentifs à enregistrer votre page `apropos.html` de manière à ce que le lien du menu fonctionne correctement, et inversement.
