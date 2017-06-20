---
layout: page 
title : Installer nodejs sur windows
permalink: /installer-nodejs-lite-server-windows.html
---
# Installer _nodejs_ et _lite-server_ sur windows

Pour pouvoir tester le site web ou les nouveaux articles créés directement dans `Visual Studio Code` nous avons besoin qu'un serveur web s'execute en local sur notre PC. Ce serveur va avoir pour mission de servir notre site statique comme s'il était publié sur un serveur distant.

Microsost offre en standard le serveur IIS (Internet Information Server) disponible sur chaque PC avec Windows. Ce serveur, bien qu'il soit partie intégrante du système d'exploitation n'est pas installé automatiquement avec WINDOWS. Mais ce serveur est bien trop complexe à configurer et il n'est pas rare de passer des heures (en tout cas pour ma part) à trouver les bons paramètres ou pour attribuer les autorisations adequates pour que le site web s'affiche correctement.

J'ai donc opté pour une solution bien plus efficace et qui pour moi a fonctionnée du premier coup : le serveur **nodejs pour windows**.

> _:exclamation: nodejs est un serveur recommandé pour ceux qui développent des applications web avec Visual Studio Code._

Nous allons donc installer :  
1. **nodejs** pour windows
2. **lite-server** pour synchroniser le rendu en live de notre site
3. **des utilitaires** écrits en javascript et que nous allons utiliser via `nodjs`

---

> _Prérequis avant de continuer_  
> [:white_check_mark: installer ruby sur windows]({{ site.baseurl }}/installer-ruby-windows.html)  
> [:white_check_mark: installer jekyll sur windows]({{ site.baseurl }}/installer-jekyll3-windows.html)

---

## 1. Installer nodejs pour Windows

`nodejs` est une application windows comme les autres, elle apparait dans la liste des programmes de windows. Lancez la commande `> appwiz.cpl` pour ouvrir le panneau de configuration de Windows :

![programme-nodejs-installe]({{ site.baseurl }}/assets/programme-nodejs-installe.png)

Pour voir quelle version est installée, vous pouvez aussi utiliser la commande `> node -v`

![check-node-version]({{ site.baseurl }}/assets/check-node-version.png)

---

## 2. lite-server pour Windows

Le serveur `Lite-server` s'appuye lui même sur le serveur `browsersync` qui offre des fonctionnalités très utile pour tester notre site. C'est lui qui va nous permettre de visualiser le rendu en live de notre site.

Pour installer `lite-server` lancez la commande suivante :

``` shell
npm install --global lite-server

```

Nous verrons plus tard comment l'utiliser en phase de rédaction de nos pages et articles.

Néanmoins, pour vérifier que cela fonctionne lancez la commande `> lite-server --baseDir="C:/temp"`.

![lite-server-test1]({{ site.baseurl }}/assets/lite-server-test1.png)

Vous devez avoir d'une part la console qui vous montre que le serveur n'arrive pas à servir le fichier `index.html` (erreur `404 GET /index.html`) ce qui est normal puisque ce fichier n'existe pas dans le repertoire `temp`.

Puis d'autre part vous avez votre navigateur par defaut qui s'est ouvert et qui affiche `Cannot GET /` à l'URL `localhost:3000`.

lite-server est donc fonctionnel. Mais allons legerement plus loin et sans refermer la console qui fait tourner le serveur web en tache de fond, modifiez l'URL en changeant le port `localhost:3001`. Vous voyez apparaitre l'interface de monitoring et de configuration du serveur `browsersync.io` encapsulé dans lite-server :open_mouth:

![browsersync-test2]({{ site.baseurl }}/assets/browsersync-test2.png)

---

## 3. Utilitaires

L'avantage d'avoir installé `nodjs` sur notre environnement c'est que nous pouvons aussi utiliser des utilitaires écrits en `javascript` qui fonctionnent sous nodejs.

**rimraf** (supression récursive de repertoires), **parallelshell** (execution parallèle de taches), **copyfiles** (copie de fichiers) et **opn-cli** (lancement d'un navigateur internet) en sont quelque uns qui vons nous servir dans les taches d'automatisation et de deploiement.

Installez les avec les commandes suivantes :

``` shell
> npm install --global rimraf
> npm install --global parallelshell
> npm install --global copyfiles
> npm install --global opn-cli
```

Puis lancer la commande `> npm config set loglevel  'error'` pour éviter de voir apparaitre trop de messages dans la console quand nous executerons ces programmes.

> _:exclamation: Pour lister tous les modules npm installés au niveau global sur votre machine utilisez la commande `> npm list -g --depth=0`_

---

## On avance ! Prochaines étapes

Récapitulons :  
:white_check_mark: [ruby et ses plugins sont installés]({{ site.baseurl }}/installer-ruby-windows.html)  
:white_check_mark: [jekyll et ses plugins sont installés]({{ site.baseurl }}/installer-jekyll3-windows.html)  
:white_check_mark: nodejs, lite-server et les utilitaires node sont installés

Bravo :+1:

Pour la prochaine étape cela dépend si vous avez déja `visual studio code` sur votre machine. Il nous faut au moins la version 1.13.

| [:white_large_square: installer visual studio code :fast_forward:](https://code.visualstudio.com/) |
| [:white_large_square: preparer visual studio code :fast_forward:]({{ site.baseurl }}/preparer-visualstudio-code-pour-jekyll3.html) |

---

### _Références_

- [A Fast and Convenient Development Server with lite-server](https://scotch.io/bar-talk/a-fast-and-convenient-development-server-with-lite-server)
- [Visual Studio Code and local web server](https://weblogs.asp.net/lduveau/visual-studio-code-and-local-web-server)
- [rimraf](https://www.npmjs.com/package/rimraf) : l'utilitaire nodejs de suppression de repertoires
- [copyfiles](https://www.npmjs.com/package/copyfiles) : l'utilitaire nodejs de copie de repertoires et fichiers
- [opn-cli](https://github.com/sindresorhus/opn-cli) : l'utilitaire nodejs qui permet d'ouvrir un explorateur
- [Lite-server](https://www.npmjs.com/package/lite-server) : le serveur de synchronisation du rendu des pages
