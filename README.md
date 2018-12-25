# Readme blogging with Studio Jekyll

Ce repository contient les sources du site [Bloggez avec Studio Jekyll sous Windows](http://wiki.maggire.net/blogging-studio-jekyll)

Ce site a été créé avec Jekyll3 et Visual Studio Code sous Windows 10. Il est publié sous GitHubPages.

## Instructions

Ce site utilise la [version "3.8.5"](https://jekyllrb.com/news/releases/) de Jekyll.

Pour réinitialiser les dépendances, supprimer le fichier `Gemfile.lock` et le regenérer avec la commmande :

```
> bundle install
```

Pour développer lancer la tache `sjekyll live rendering`, cela régénère le site et lance un serveur de rendering sur le port 3300.

Pour déployer en production, lancer la tache `sjekyll deploy to PROD env`. Cela regenère le site directement dans le sous dossier `/docs` qui est utilisé par Githubpages pour afficher le site web.

--------------

## Auteur

**Mike Maggire**

- https://github.com/mikemaggire

## License

Open sources, sous [licence MIT](LICENSE.txt).

Le design de la version 0.1.0 est un fork du [thème Jekyll Lanyon] https://github.com/poole/lanyon
