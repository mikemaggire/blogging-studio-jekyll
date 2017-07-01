---
layout: post
tags: Jekyll3
author: Mike Maggire
title: Jekyll, pour créer tout type de site web et de blog, ou presque
subtitle: Outre les performances et la sécurité élevée, Jekyll est très flexible. Il permet de génerer des sites intégrant de nombreuses fonctionnalités, voyez par vous même.
date_update: 2017-07-01 22:00:00 +0200
---
## Donc Jekyll, c'est quoi précisement

Jekyll est un **générateur de site statique** simple, et de type blog. Il lui faut un répertoire de modèles contenant des **fichiers de textes bruts et formatés** (la partie rédactionnelle de votre site, son contenu), puis il les traite à travers un **convertisseur** comme `Markdown` et le **générateur de rendu** `Liquid`, et produit un site Web statique complet et **prêt à publier** vers **votre serveur Web** préféré (chez un hebergeur par exemple). Jekyll est également le moteur de GitHub Pages, ce qui signifie que vous pouvez utiliser Jekyll pour héberger la page, le blog ou le site de votre projet à partir des serveurs de GitHub gratuitement.

## Caractéristiques d'un site web généré par Jekyll

* Le site web ne contient que des fichiers statiques, en conséquence de quoi :
  * **les temps de réponse sont les meilleurs qui soient**
  * **le niveau de sécurité est elevé**, comparé aux sites dynamiques servis à partir d'un CMS
  * en contrepartie, les possibilités de produire du contenu dynamiquement, par exemple à partir d'une base de données, n'est pas possible (cela n'empêche pas pour autant de pouvoir publier régulièrement des articles de blog).
* Le site web contient **une page principale**, la page d'accueil, qui peut être unique par ailleurs si vous les souhaitez.
* Le site web peut contenir **autant de pages fixes que necessaire**.
* Le site web peut contenir **des articles de blog**.
* Chaque page ou article peut **intégrer des images, des vidéos, des pdf à telecharger** ou tout autre contenu intégrable sur n'importe que site. Ce contenu peut provenir d'un repertoire de votre propre sité généré, soit provenir d'un source extérieur comme par exemple une vidéo `Youtube` ou encore les commentaires des blogueurs avec `Disqus`.
* Le **design est moderne** : responsive, flat design, formulaires plein écran...
* Le **design est totalement personnalisable**, vous avez accès à toutes les sources.
* Le **design est interactif**, grâce à l'utilisation de composants `javascript` : effets de "survols", fondus, burger bouton...
* Techniquement le rendu respecte les standards `HTML5` et `CSS3`.

et enfin, le tout est **gratuit**.

## Jekyll, pour quoi faire

* Un **blog**, en tout premier lieu, mais pas que !
* Un **wiki**, aussi, quand le contenu peut être enrichi par un groupe de personnes,
* De la **documentation** au format web, très pratique.
* Un **site institutionnel** "classique".
* ou encore une **single page** pour présenter un produit ou un service
