---
layout: post
tags: Jekyll3 MiniMax
title: Minimax, un modèle de site pret à l'emploi
subtitle: "Simple et musclé : pages et blog, analytics, disqus, .htacces... et bien entendu conçus pour visual studio code. Enfin il intègre les taches de déploiement automatique."
date_update: 2017-07-01 22:00:00 +0200
---
Pour démarrer rapidement à rédiger du contenu avec `StudioJekyll` nous vous proposons d'utiliser le `modèle Minimax`. Ses caractéristiques sont détaillées dans cet article.

Nous vous présentons :

1. les caractéristiques des sites web créés à partir de Minimax_
1. les fonctions intégrées pour une utilisation avec Visual Studio Code
1. les taches de déploiement automatique

---

## 1. Sites web créés à partir de _Minimax_

Il s'agit avant tout d'un site initialisé avec `Jekyll3.5` et reprenant le style du `thème minima`. Le site que vous allez créer à partir du `modèle minimax` hérite donc des [caractéristiques des sites créés à partir de Jekyll]({{ site.baseurl }}{% post_url 2017-06-22-caracteristiques-sites-jekyll %}) et des caractéristiques du thème minima.

![screenshot-minimax1.png]({{ site.baseurl }}/assets/img/screenshot-minimax1.png)

Nous avons ajoutés :

:white_check_mark: **Formatage Français du contenu**

- La langue `fr` par defaut sur toutes les pages, ainsi que `l'encodage utf-8` des fichiers.
- Le format `jj/mm/aaaa` pour les dates.

:white_check_mark: **Amélioration du référencement sur les moteurs de recherche**

- Le fichier `robots.txt` pour (a) que vos images ne soient pas indexées, (b) référencer le sitemap.
- Un `sitemap.xml`, qui se met à jour automatiquement à chaque génération de votre site.
- Un `flux RSS` contenant vos publications.

:white_check_mark: **Statistiques de consultation**

- l'intégration de `google analytics` sur toutes vos pages.

:white_check_mark: **Commentaires des internautes**

- la prise en charge des commentaires des internautes avec `Disqus` sur vos articles et vos pages, paramétrable.  
  ![comment-wt-disqus]({{ site.baseurl }}/assets/img/comment-wt-disqus.png)

:white_check_mark: **Renforcement de la sécurité**

- un fichier `.htaccess` type (utile pour un hebergement sur un serveur LAMP type chez OVH )
  - incluant des directives pour renforcer la protection de votre site
  - la prise en charge d'une page d'erreur 404 personnalisée
- une `page 404` personnalisée

:white_check_mark: **et aussi...**

- un `favicon` par défaut (le standard et aussi celui pour la consultation sur iPhone)

---

## 2. _Minimax_ a été conçu pour Visual Studio Code

Ouvrir un dossier _Minimax_ sous `Visual Studio Code` vous fait immédiatement bénéficier des fonctions suivantes :

:white_check_mark: **le 'live rendering'**, c'est à dire la visualisation de l'aspect fini de votre site au fur et à mesure que vous saisissez. Pas besoin d'attendre de compilation ou de génération par batch.

:white_check_mark: **des taches préparametrées sous VSCode**

- le rendu en live du site avec `CTRL + SHIFT + R`
- la génération immédiate et détaillée du site avec `CTRL + SHIFT + B`

:white_check_mark: **le forcage de l'encodage UTF-8 _sans BOM_ des fichiers**

- au travers du fichier `.editorconfig` préconfiguré. A noter que ce format d'encodage est requis impérativement par Jekyll et `Liquid` sans quoi la génération du site ne fonctionne pas.

:white_check_mark: **le controle de la syntaxe Markdown en cours de frappe**

- avec l'extension `markdownlint`

---

## 3. Déploiement automatisé

Le déploiement automatisé est directement accessible depuis VisualStudio avec `CTRL + P` puis en tappant `task`.

![task-deploiement]({{ site.baseurl }}/assets/img/task-deploiement.png)


:white_check_mark: **traitement automatisé du déploiement vers les environnements de test et de production**

- la build automatisé prend en compte les paramètres propres à l'environnement de destination comme l'URL, la compression des fichiers ou encore l'activation des fonctions d'analytics
- le transfert des fichiers via `SFTP`, utilisable avec la plupart des hebergeurs de sites mutualisés
