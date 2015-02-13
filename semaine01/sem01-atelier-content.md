---
title: Contenu de l'atelier de la semaine 1
author: iGor
date: 2015-02-04
---

# Contenu de l'atelier de la semaine 1 | 2015-02-18

## Présentation framework | 5 min.

Un *framework* est un ensemble de composants logiciels améliorant le développement, parfois spécialisé dans un langage particulier. Dans le contexte de la publication Web, on parle souvent de _framework_ CSS. Il en existe plusieurs catégories. Pour le cours, nous allons utiliser des versions simplifiées, dans lesquelles nous modifierons uniquement les fichiers `html` et `css`.

Le choix pour notre cours s'est porté sur [Skeleton](http://getskeleton.com/). Il est un peu abusif de parler de _framework_, il s'agit plus d'un _template_ CSS, mais c'est justement sa simplicité qui nous intéresse, convenant particulièrement bien à un cours d'introduction tel que le notre.

## Téléchargement et décompression | 5 min.

Source : [http://getskeleton.com](http://getskeleton.com), le bouton *download*.

Enregistrez l'archive ZIP sur votre disque dur, dans un dossier de travail dans `Mes Documents`. Décompressez l'archive. Vous devriez obtenir l'arborescence suivante :

```
Skeleton-2.0.4
├── css
│   ├── normalize.css
│   └── skeleton.css
├── images
│   └── favicon.png
└── index.html
```

Renommez selon vos désirs le dossier `Skeleton-2.0.4`, par exemple `mon-site`.

## Navigateur de fichier et navigateur Web | 2 min.

   1. Ouverture du dossier `mon-site` avec le navigateur de fichier.
   2. **Clic-droit** sur `index.html` et "ouvrir avec Firefox" et observation, notamment de l'URL.

## Structure physique | 10 min.

   Les éléments importants à repérer : le fichier `html` (le contenu), les dossiers `css/` (contenant les fichiers `css` correspondant à la mise en forme) et `images`. Cette structure est la structure *physique*. On peut y ajouter tous les dossiers que l'on désire : `documents/`, par exemple.

## Comment éditer les fichiers `html` et `css` | 5 min.

   Les fichiers `.html` et `.css` sont des fichiers textes et peuvent s'ouvrir avec un éditeur de texte simple, comme le bloc-notes ou *TextEdit*, ou avec un éditeur plus complet comme *Notepad++*, *gedit* ou *geany*.

   **Remarque 1** : par défaut à l'école les fichiers `.html` et `.css` s'ouvrent avec *Dreamweaver*, un éditeur WYSIWYG que nous n'allons pas utiliser dans ce cours. Il faut d'abord faire un clic-droit sur ces fichiers pour configurer l'application par défaut pour l'ouverture de ces fichiers : *Notepad++* me semble un bon choix.
   **Remarque 2** : selon le type d'encodage utilisé (ISO 8859-1 ou utf-8), les lettres accentuées et les signes diacritiques ne sont pas rendus correctements par les navigateurs Web. Le plus simple est de paramétrer l'éditeur de texte (par exemple *Notepad++*), afin d'utiliser l'encodage `utf-8`. Une autre solution est d'écrire les caractères accentués, les caractères spéciaux et les signes diacritiques sous la forme d'[entités de caractères en HTML](https://fr.wikipedia.org/wiki/Liste_des_r%C3%A9f%C3%A9rences_d%27entit%C3%A9s_de_caract%C3%A8res_en_XML_et_HTML#R.C3.A9f.C3.A9rences_d.27entit.C3.A9s_de_caract.C3.A8res_en_HTML). Par exemple, le caractère "é" s'écrira `&eacute;`.

## Édition du fichier `index.html` | 10 min.

   1. Depuis le navigateur de fichier, aller dans le répertoire `mon-site`.
   2. **Clic-droit** sur le fichier `index.html` et ouvrir avec *Notepad++* ou *Editplus*.
   3. Repérer les balises `<html> </html>`, `<head> </head>` et `<body> <body>`. Pour la session de la semaine 01, on ne travaille que dans le `<body>` (lignes 30 à 45).
   4. Supprimer les lignes 35 à 40.
   5. Sous la ligne 34, on insère le code qui suivant :

```
	<h1>Mon premier titre</h1>
	<h2>Un titre de niveau 2</h2>

	<p>Ici, nous pouvons écrire un paragraphe, par exemple.</p>
	<p>Ajoutez un paragraphe un peu plus long au moyen d'un copier-coller.</p>
```
   6. Enregistrer votre fichier `index.html` et recharcher la page Web correspondante.

## Utilisation du serveur Web local | 7 min.

   1. Faire une copie du dossier `mon-site` dans `P:\config\wwwroot.xamp\` ; démarrer XAMP, le service Apache.
   2. Ouvrir l'URL `http://localhost:8005/mon-site` et observer les différences avec la page ouverte "directement", principalement la police de caractère. Voir la ligne 18 du fichier `index.html`.

# Notions vues

   * *framework*
   * Accès aux fichiers et à la page Web
   * Structure physique
   * Éditer et éditeurs, encodage utf-8 et entités.
   * Fonctionnement des balises : chevron, ouvrantes, fermantes, slash.
   * 3 balises de structures (`html`, `head`, `body`) et trois balises de contenu (`h1`, `h2` et `p`).
   * Accès via le serveur Web local
