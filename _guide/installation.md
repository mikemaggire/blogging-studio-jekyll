---
layout: page
title: Guide d'installation de l'environnement de travail Jekyll3 Visual Studio Code
sidebar: Guide installation
---
# Guide d'installation de l'environnement de travail _Studio Jekyll_

## Composition de notre environnement de travail

* L'IDE Microsoft **Visual Studio Code**. Il intègre :
  * un éditeur de texte,
  * une intégration `GIT` pour la gestion de nos brouillons et des historiques de publications,
  * un ensemble d'outils d'automatisation de taches.

* **Jekyll** :
  * pour générer les pages HTML statiques.

* **nodejs** avec **lite-server** :
  * comme serveur web de développement pour 'voir' en live le rendu de nos pages et de nos articles, mais aussi
  * une solution de publication vers differents types de serveurs cibles.


_**NOTE :** Nous travaillons sous **Windows 10**._

---

## Etapes d'installation

1. [installer Ruby]({{ site.baseurl }}{% link _guide/installer-ruby.md %}) qui est utilisé par Jekyll (voir notes ci-après).
1. [installer Jekyll]({{ site.baseurl }}{% link _guide/installer-jekyll.md %}) lui même, et quelques plugins dont nous avons besoin,
1. [installer nodejs]({{ site.baseurl }}{% link _guide/installer-nodejs.md %}), lite-server, et quelques plugins nodejs.

Dans cet ordre, c'est important !

Puis :

1. [installer visual studio code](https://code.visualstudio.com/) si ce n'est pas déja fait,
1. [préparer visual studio code]({{ site.baseurl }}{% link _guide/preparer-vs.md %}) en installant des extensions et quelques utilitaires.

**NOTE :** _Nous utiliserons les outils windows autant que faire ce peut, et quand nous utilisons la ligne de commmande nous détaillons les étapes façon 'pour les nulls'._

---

## Quelques remarques au sujet de Jekyll

**NOTE 1 :** _`Jekyll` n'est pas officiellement supporté sur Windows mais si vous suivez notre guide d'installation cela fonctionne très bien :smile:_

**NOTE 2 :** _`Jekyll` n'est pas un programme executable windows `.exe` qu'il suffirait d'installer comme n'importe quel logiciel WINDOWS ! Ce n'est pas non plus une app que l'on peut trouver sur le Windows Store ! `Jekyll` vient du monde `Linux` et il a été écrit dans le langage de programmation `Ruby`. Donc la première chose à faire est d'**installer Ruby sur votre PC**, puis d'installer Jekyll seulement après._

**NOTE 3 :** _`Jekyll` a besoin de s'executer quelque part pour transformer le texte brut et tous les fichiers qui sont embarqués avec (html, css, js, images...) en magnifique site web statique. `Jekyll` n'est utilisé exclusivement **que pour générer le site** et ses modifications. Une fois votre site ou vos pages publiées, `Jekyll` n'est plus utilisé. **Jekyll a donc besoin d'être installé uniquement sur votre machine locale**, votre machine de "rédaction/publication"._

**NOTE 4 :** _Donc rien n'est à installer sur les serveurs de tests et de production. Seuls les fichiers statiques html, css, js et images y seront copiés._

---

## C'est parti !

| [:white_large_square: installer Ruby :fast_forward:]({{ site.baseurl }}{% link _guide/installer-ruby.md %})