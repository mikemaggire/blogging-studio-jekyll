---
layout: post
tags: guide
author: Mike Maggire
title: Comment activer les commentaires sur un site StudioJekyll
---
## Technique du Mashup Applicatif

Votre site est un site statique sans base de données et sans moyen d'authentification. La question est donc : comment mettre en place un système de commentaires dynamique necessitant une base de données et un système d'authentification ?

La réponse est simple : grâce à la technique du **mashup applicatif**. 

Cela consiste à intégrer à notre site du contenu qui vient d'une autre application web ! Concretement notre site web intègre un script `javascript` qui va s'executer dans le navigateur de l'utilisateur. Sa fonction va être d'aller _chercher_ les commentaires dans une autre application web (une autre URL).

Cette application qui gère les commentaires et qui s'intègre aux autres sites c'est **DISQUS** !

![disqus-logo.png]({{ site.baseurl }}/assets/disqus-logo.png)

---

## Intégration de DISQUS dans _StudioJekyll_

La bonne nouvelle c'est que DISQUS est déja intégré aux sites StudioJekyll. Plus exactement c'est le _script_ Disqus qui est déja intégré dans vos pages statiques. Il ne reste donc plus qu'à le configurer.

Voilà à quoi cela ressemble en bas de vos articles :

![comment-wt-disqus2]({{ site.baseurl }}/assets/comment-wt-disqus2.png)

---

## Configuration des commentaires avec DISQUS

Vous devez avant tout [ouvrir un compte chez DISQUS](https://disqus.com/profile/signup/) (ils possèdent un plan gratuit entre autres). Puis vous allez 'installer DISQUS sur un nouveau site'. Le système vous attribut alors un identifiant pour votre site qui s'appelle _shortname_.

Ensuite vous allez indiquer cet identifiant dans le fichier de configuration `_config.yml` de votre site _StudioJekyll_.

```yaml
# ###### Gestion des commentaires sur les pages #######
# Pour activer DISQUS à la fin des articles
disqus:
  shortname: identifiant-donne-par-disqus
```

Et c'est tout !

A partir de ce moment, la gestion des commentaires apparait par défaut en bas de tous les articles de blog (les pages associées au layout 'post'), et n'apparait pas en bas des pages fixes (les pages associées au layout 'page').

> :exclamation: _la gestion des commentaires n'a pas été intégrée dans les autres layout._

## Changer le comportement par defaut

Pour changer le comportement par defaut il faut aller modifier les fichiers `_layout/page.html` et `_layout/post.html` et changer la variable `layoutcomments` au tout début du fichier.

```yaml
---
layout: default
---
{% raw %}{% assign layoutcomments = false %}{% endraw %}
```

## Forcer le comportement sur une page ou un article

Dans l'entête de chacune de vos page et de vos articles vous pouvez forcer la gestion des commentaires en attribuant à `true` ou à `false` la variable `comments`.

```yaml
---
layout: post
title: mon article sans gestion des commentaires
comments: false
---
```
