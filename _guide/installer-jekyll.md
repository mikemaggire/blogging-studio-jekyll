---
layout: page 
title: Installer Jekyll3 sur Windows
---
# Installer Jekyll et ses plugins sur Windows

`Jekyll` est le générateur de site statique qui va transformer nos fichiers textes en fichiers HTML. Nous allons :

1. installer `Jekyll` lui même,
1. installer des plugins Jekyll.

---

> _Prérequis avant de continuer_  
> [:white_check_mark: installer ruby sur windows]({{ site.baseurl }}{% link _guide/installer-ruby.md %})

---

## 1. Installation de Jekyll

Le langage de programmation `Ruby` offre de nombreuses extensions et un utilitaire de gestion des packages appelé `gem`. Cet utilitaire a été installé sur votre machine en même temps que Ruby. La commande `gem install` permet d'installer un package Ruby sur votre machine.

> _La notion de package est très utilisée dans le contexte LINUX et beaucoup moins dans le contexte Windows même si elle tend à se vulgariser. Pour faire simple un package est un logiciel avec sa documentation et sa procédure d'installation._

Le logiciel Jekyll est un package de Ruby qu'il est necessaire d'installer avec la commande suivante :

```shell
> gem install jekyll bundler
```

Après quelques secondes `Jekyll` et ses dépendances sont installés :

![gem jekyll cmd line]({{ site.baseurl }}/assets/gemjekyll1.png)

Pour tester que Jekyll fonctionne bien, vous pouvez lancer la commande ```jekyll -v``` qui vous retourne le numéro de version du logiciel installé sur votre machine :

![jekyll-v]({{ site.baseurl }}/assets/jekyll-v.png)

> _Jekyll n'étant pas un programme windows il n'apparait pas dans la liste des programmes installés du panneau de configuration de windows._

## 2. Installation des plugins de jekyll

Il existe plusieurs extensions Jekyll qui permettent d'enrichir ses capacités. La plupart sont disponibles sous la forme de `package Gem`. Ce ne sont ni plus ni moins que des programmes `ruby`. Voici celles que nous avons besoin :

- **jekyll-feed** : pour intégrer un flux rss à votre site
- **emoji_for_jekyll** : pour intégrer des emoji dans les pages de votre site
- **tzinfo** : pour prendre en compte les fuseaux horaires dans les calculs de dates
- **rouge** : pour formater automatiquement des extraits de code dans vos publications

Lancez successivement les commandes suivantes pour les installer :

```shell
> gem install jekyll-feed
> gem install emoji_for_jekyll
> gem install tzinfo
> gem install tzinfo-data
> gem install rouge
> gem install jekyll-sitemap
```

Yes, Jekyll est opérationnel sur votre PC ! :+1:

---

## Prochaines étapes

| [:fast_forward: installer nodejs et lite-server]({{ site.baseurl }}{% link _guide/installer-nodejs.md %}) |

---

### _Références_

- Site officiel de [Jekyll](https://jekyllrb.com/)
- Liste des [pluggins Jekyll](https://jekyllrb.com/docs/plugins/#available-plugins)
- [documentation de `gem install`](http://guides.rubygems.org/command-reference/#gem-install)
- Le [package Jekyll](https://rubygems.org/gems/jekyll)
