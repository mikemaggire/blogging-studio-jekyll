---
layout: page
title: Initialisez un nouveau site web
permalink: /initialiser-site-web-blog-jekyll3-visual-studio.html
---
# Initialisez votre 1er site web

> _TODO: à completer_

## Ce que vous devez préparer avant de commencer

Le process de publication : fast, avec revue...
Plutot type blog, ou plutot type site, sachant que nous pouvons faire les deux et les faiure évoluer après. 
L'adresse URL ou sera publier votre site, meme si on va en avoir besoin plus tard.

> _TODO: à completer_

## Configurer les propriétés du site web

Vous devez aller modifier le fichier '_config.yml'

> _TODO: à completer_

## Générer le site web

Lancez une 1er génération Jekyll à l'aide des touches `CTRL + SHIFT + B`. Cela lance la commande `jekyll build` qui est définie dans le fichier de configuration des taches `tasks.json` de notre projet.

![single-jekyll-build-output-ok]({{ site.baseurl }}/assets/single-jekyll-build-output-ok.png)

Si tout c'est bien passé vous pouvez maintenant tester votre site.

## Tester le site web

Lancez le server web avec `CTRL + 'P'` puis en tappant `task run_webserver`.

![run-web-server-task.png]({{ site.baseurl }}/assets/run-web-server-task.png)

Le terminal de visual studio s'ouvre et vous devriez voir que le serveur web est démarré en tache de fond. Voila à quoi cela ressemble :

![webserver-running]({{ site.baseurl }}/assets/webserver-running.png)

Puis votre navigateur internet par défaut s'ouvre également. Vous pouvez alors naviger dans votre site et vérifier que tout fonctionne correctement.

Vous allez pouvoir laisser cette fenêtre terminal ouverte pour que le serveur web puisse continuer à fonctionner. Cela va être très pratique pour pouvoir suivre en _live_ les modifications apportées sur le site.

**A NOTER :** Le fichier bs-config.json contient la configuration du serveur web qui est lancé.

```json
    {
        "port": 3000,
        "injectChanges": true,
        "files": [ "./**/*.{html,htm,css,js,png,jpg}" ]
    }

```

Maintenant que tout est ok, nous allons activer la regeneration permanente de jekyll, en tache de fond.

Lancez la tache `CTRL + 'P'` puis tappez `task build_jekyll_live` dans la fenêtre de commande de visual studio code.

Une nouvelle fenêtre terminal s'ouvre que vous allez également devoir laisser ouverte.

## Conclusion

Continuez avec le [Guide pour rédiger et publier]({{ site.baseurl }}/guide-rediger-publier-jekyll3-visualstudio-code.html)
