---
layout: page 
category: guide
title: Configurer contenu d'un nouveau site
---

> _Prérequis_  
> [:white_check_mark: Cloner un site modèle à partir de GitHub]({{ site.baseurl }}{% link _guide/cloner-site.md %})

---

Dans ce guide nous allons :  
1. Modifier le fichier `_config.yml`
1. Modifier le fichier `index.html`
1. Modifier le fichier `package.json`
1. Choisir la couleur de notre site
1. Personaliser la page à propos
1. Ecrire le message de bienvenue
1. Tester et enregistrer notre travail

---

## 1. le fichier _config.yml

```yaml
########################
# Configuration initiale
########################
# C'est ici que vous définissez les paramètres initiaux de vore nouveau site. 
# Sivous regardez dans vos fichiers HTML, vous verrez qu'ils y accedent
# via {{ site.title }}, {{ site.email }}, et ainsi de suite.

title: Le titre de votre site
tagline: Votre tagline
description: Rédigez une description parlante de votre site. Vous pouvez éditer ce texte dans le fichier '_config.yml'. Il apparaitra dans les metadonnées des entêtes des pages de votre site (utilisé par le référencement Google) et dans la description de votre flux RSS. 

copyright:
  name: Votre copyright
  url: https://votre-domaine.com/auteur-copyright.html
  licence: Libre de droits sous license MIT

author:
  name: Votre pseudo
  url: https://twitter.com/mikemaggire

# id utilisés pour faire apparaitre les boutons réseaux sociaux sur le site
email: votre-email@example.com
twitter_userid: mikemaggire
github_userid:  mikemaggire
#gplus_userid: +mikemaggire
#facebook_userid: mikemaggire
#linkedin_userid: mikemaggire
```
---

## 2. Le fichier index.html

**1ere option** : vos visiteurs arrivent directement sur le blog

Supprimez la ligne suivante et remplacez là éventuellement par votre message de bienvenue.

```yaml
Vous pouvez ajouter votre message de bienvenue au dessus des publications. :rocket:
```

**2eme option** : la page d'accueil de votre site est une page fixe

...et vous avez éventuellement un blog mais qui est accessible par la barre de navigation.

> TODO: 

## 3. Réinitialiser le numéro de version

Dans le fichier `package.json`, initialisez le numéro de version à 0.1.0

```json
        "version": "0.1.0",
```

## 4. Choisissez la couleur

Ouvrez le fichier `_studiojekyll/_config.scss` et choisissez la couleur soit en prenant une des valeurs proposées soit avec votre propre couleur.

![chooseyourcolor.png]({{ site.baseurl }}/assets/img/chooseyourcolor.png)

## 5. Personnalisez la page 'A propos'

> TODO: 

## 6. Ecrivez votre message de bienvenue

> TODO:

## 6. Et pour terminer

Voyons le résultat avec [CTRL+SHIFT+R].

Si tout est ok alors nous pouvons arreter le _live rendering_ avec [CTRL+C] dans le terminal au niveau de la tache '1: Tâche - liverendering'.

Puis nous allons enregistrer notre travail avant de réaliser la première publication en test.

Dans VS Code, ouvrez le controle de code source en clickant sur l'icon correspondant ou bien avec [CTRL+MAJ+G]. Saisissez le message `contenu configuré`, puis [CTRL+ENTER].

C'est fait. Il ne reste plus qu'à synchroniser pour sauvegarder sur GitHub : Menu `.../Synchroniser`.

---

## Prochaine étape

| [:fast_forward: configurer la publication]({{ site.baseurl }}{% link _guide/configuration-publication.md %}) |
