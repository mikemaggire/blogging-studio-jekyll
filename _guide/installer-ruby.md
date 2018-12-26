---
layout: page  
category: guide
title:  Installer Ruby sur Windows 10
---
Ruby est le langage de programmation dans lequel est écrit `Jekyll`. Nous devons installer :

1. l'interpreteur `ruby` lui même
1. des plugins ruby.

---

## 1. Installer Ruby

Telechargez et executez [RubyInstaller for windows](https://rubyinstaller.org/downloads/).

:exclamation: Jekyll V3 à besoin de Ruby en version supérieure à la 2.2.5. Ici nous utilisons la version 2.5.3.

:warning:  Vous devez cocher `MSYS2 development toolchain 2018-10-21`.

![install3]({{ site.baseurl }}/assets/img/rubyinstaller3.png)

Vous pouvez vérifier que le programme est bien installé en allant dans la liste des programmes et fonctionnalités du panneau de configuration de votre ordinateur. Soit via le `menu démarrer`, soit avec la commande suivante: 

``` shell
# ouvre le panneau de configuration de Windows
> appwiz.cpl 
``` 

![install5]({{ site.baseurl }}/assets/img/rubyinstaller5.png)

Pour vous assurer que cela fonctionne bien, executez la commande `> ruby -v` :

![install4]({{ site.baseurl }}/assets/img/rubyinstaller4.png)

OK, votre PC peut maintenant executer des programmes écrits en Ruby !

> _**NOTE :** Les programmes écrits en Ruby portent l'extension `.rb`._

---

## 2. _kit de développement de Ruby_

> _Si vous aviez deja installé Ruby auparavent, je vous recommande de lancer un update via la commande `> gem update` avant de continuer_

Pour que certains programmes `ruby` fonctionnent et tout particulièrement certains plugins de jekyll, nous avons besoin d'installer le kit de développement Ruby. Depuis la version 2.4 de ruby ce programme a été automatiquemnt été installé si vous avez bien coché `MSYS2` lors de l'installation precedente.

---

## 3. Installer les plugins ruby

Nous avons besoin du `plugin wdm` qui permet de _scruter_ les changements dans les répértoires Windows. Ce plugin est utilisé par l'option `--watch` de jekyll.

Dans une fenêtre de commandes tappez la commande suivante :

``` shell
> gem install wdm
```

Voila, Ruby est opérationnel sur votre PC ! :+1:

---

## Prochaine étapes

| [:fast_forward: Installer Jekyll]({{ site.baseurl }}{% link _guide/installer-jekyll.md %}) |

---

### _Références_

* A propos de [Ruby](https://www.ruby-lang.org/fr/about/)
* [plugin WDM](https://github.com/Maher4Ever/wdm) pour scruter les changements dans les repertoires Windows
