---
layout: page 
category: guide
title: Cloner un site modèle à partir de GitHub
---

> _Prérequis_  
> [:white_check_mark: installer l'environnement de travail]({{ site.baseurl }}{% link _pages/guide-installation.md %})

---

Dans ce guide nous allons tout faire à partir de l'IDE de Visual Studio Code.

Donc commencons par ouvrir Visual Studio Code puis à fermer le dossier en cours `[CTRL+K F]`.

## > Git Clone

Puis lancons la commande 'Git Clone' à partir du clavier `[CTRL+SHIFT+P]` et en saisissant `>Git clone` puis `[enter]`.

![cmd-gitclone.png]({{ site.baseurl }}/assets/img/cmd-gitclone.png)

Ensuite nous devons choisir le modèle de site à utiliser. Ici nous choisirons **studiojekyll-minimax** : https://github.com/mikemaggire/studiojekyll-minimax

![choix-model.png]({{ site.baseurl }}/assets/img/choix-model.png)

Enfin nous devons préciser l'emplacement des sources de notre nouveau site en local :

![choix-nomrepo.png]({{ site.baseurl }}/assets/img/choix-nomrepo.png)

Puis confirmons l'ouverture du projet dans Visual Studio.

![msg-ouvrirrepo.png]({{ site.baseurl }}/assets/img/msg-ouvrirrepo.png)

OK ! Voilà à quoi cela doit ressembler :

![freshnewsite.png]({{ site.baseurl }}/assets/img/freshnewsite.png)

Bon maintenant vérifions que l'[installation de votre environnement]({{ site.baseurl }}{% link _pages/guide-installation.md %}) s'est correctement déroulée. Faites une première génération de votre site simplement avec `[CTRL+SHIFT+B]`. Cela déclenche la tache de build en local avec la configuration spécifique à studiojekyll. Vous avez la fenêtre du terminal qui s'ouvre et en quelque secondes vous avez le résultat. _1.055 secondes précisement sur ma machine !_

![buildpassed.png]({{ site.baseurl }}/assets/img/buildpassed.png)

<p class="message-yellow"> :warning: il est important qu'il n'y ait pas d'erreur au niveau de ce premier build avant de continuer. </p>

## Live rendering

Pour terminer cette première étape lançons le _live rendering_ avec `[CTRL+SHIFT+R]`. Cela relance la génération du site en mode _watch_ et cela ouvre votre navigateur avec notre site.

![liverending-output.png]({{ site.baseurl }}/assets/img/liverending-output.png)

Une nouvelle tache s'est déclenchée et la sortie du traitement de rendu en tache de fond  apparait en parallèle dans le terminal integré à Visual Studio Code.

![liverenderong console.png]({{ site.baseurl }}/assets/img/liverenderong console.png)

> :exclamation: _Pour être plus précis deux taches de fond ont été lancées en parallèle. Tout d'abord le la géneration Jekyll et aussi le serveur web synchronisé qui sert les fichiers générés par jekyll. Dans la console on voit donc appraitre les messages des deux traitements._

On va stopper le mode `live rendering` en interrompant le processus avec `[CTRL+C]` au niveau de la console de taches.

![arret-live-rendering.png]({{ site.baseurl }}/assets/img/arret-live-rendering.png)

<p class="message"> _Le repertoire contenant le projet sur votre PC porte le nom du repretoire cloné, c'est à dire `/studiojekyll-minimax`. Il peut être interessant de renommer ce repertoire. Pour cela vous devez d'abord refermer visual studio code puis le réouvrir après avoir renommer le repertoire sous windows._ </p>

## Synchroniser le repository avec GitHub

Ouvrez le terminal de visual studio `[CTRL+ù]` code et lancer les commandes suivantes :

```
rm .git
git init
git add .
git commit -m initialisation
git remote add origin https://github.com/yourgitaccount/newrepo
opn "https://github.com/yourgitaccount?tab=repositories" --ext=html
# create the repo direcly onto github.com
git push -u origin master

```

---

## Prochaine étape

| [:fast_forward: configurer le contenu]({{ site.baseurl }}{% link _guide/configuration-contenu.md %}) |
