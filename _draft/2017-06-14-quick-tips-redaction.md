---
layout: post
title: quick-tips
---
# Quick Tips

## Codes d'emotji courants

  | smile :smile: | wink :wink: | heart :heart: | star :star: | fire :fire: | +1 :+1: |

## backslash au début et à la fin des permalink

Pas de backslah au début du permalink signifie que le chemin est relatif, ce qui est un mauvais choix pour le permalink d'une page !

Donc nous preferons mettre systématiquement un backslash au début des permalink des pages, cela 

```markdown
---
layout: page
title : Installer nodejs sur windows
permalink: /installer-nodejs-windows.html
---

```

backslash à la fin

## formatage de dates

formats de dates https://learn.cloudcannon.com/jekyll/date-formatting/

localisation https://www.yohann-decharraud.com/2015/12/11/localiser-une-date-avec-jekyll.html

# creer une ancre

https://stackoverflow.com/questions/6695439/how-to-link-to-a-named-anchor-in-multimarkdown


# Contenu dynamique
Par ailleurs il est possible de construire du contenu dynamique au sein de vos documents en utilisant le modèle de langage [**Liquid**](https://shopify.github.io/liquid/). Mais avec les  [templates de sites prêt à l'emploi](/maggire-jekyll3-templates.html) que je vous fourni vous n'aurez pas besoin de vous plonger dans cet apprentissage.

TODO: à completer
