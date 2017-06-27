---
layout: page  
title:  Installer Ruby sur Windows 10
---
# Installer Ruby sur Windows 10

Ruby est le langage de programmation dans lequel est écrit `Jekyll`. Nous devons installer :

1. l'interpreteur `ruby` lui même,
1. le kit de développement utilisé par quelques pluggins,
1. des plugins ruby.

---

## 1. Installer Ruby

Telechargez et executez [RubyInstaller for windows](https://rubyinstaller.org/downloads/).

:exclamation: Jekyll V3 à besoin de Ruby en version supérieure à la 2.0.0

:warning:  Vous devez cocher `Add Ruby Executables to your PATH`.

![install3]({{ site.baseurl }}/assets/rubyinstaller3.png)

Vous pouvez vérifier que le programme est bien installé en allant dans la liste des programmes et fonctionnalités du panneau de configuration de votre ordinateur. Soit via le `menu démarrer`, soit avec la commande `> appwiz.cpl` pour ouvrir le panneau de configuration de Windows:

![install5]({{ site.baseurl }}/assets/rubyinstaller5.png)

Pour vous assurer que cela fonctionne bien, executez la commande `> ruby -v` :

![install4]({{ site.baseurl }}/assets/rubyinstaller4.png)

OK, votre PC peut maintenant executer des programmes écrits en Ruby !

> _**NOTE :** Les programmes écrits en Ruby portent l'extension `.rb`._

---

## 2. Installer le _kit de développement de Ruby_

> _Si vous aviez deja installé Ruby auparavent, je vous recommande de lancer un update via la commande `> gem update` avant de continuer_

Pour que certains programmes `ruby` fonctionnent et tout particulièrement certains plugins de jekyll, nous avons également besoin d'installer le kit de développement Ruby. Ce programme se trouve aussi sur la page de telechargement de [RubyInstaller](https://rubyinstaller.org/downloads/).

![ruby-devkit-install]({{ site.baseurl }}/assets/ruby-devkit-install.png)

Une fois téléchargé, vous devez lancer l'executable qui propose une décompression dans un repertoire de votre choix. Choisissez un emplacement définitif. Nous proposons de choisir un sous-repertoire de ruby que nous appelerons 'devkit'. Les fichiers telechargés et décompressés doivent donc se trouver dans `C:/ruby23-x64/devkit/`.

Ensuite il faut ouvrir un fenêtre de commandes dans ce repertoire et lancer successivement trois commandes d'initialisation :

```shell
> devkitvars.bat
> ruby dk.rb init
> ruby dk.rb install
```

![init-devkit-ruby.png]({{ site.baseurl }}/assets/init-devkit-ruby.png)

:exclamation: Il est important que cette installation soit réussie. Aussi si vous avez besoin de plus d'explications ou d'aides sur les messages d'erreur rencontrés vous pouvez aller regarder du coté du [wiki dédié au kit de development de ruby](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit).

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

| [:white_large_square: Installer Jekyll :fast_forward:]({{ site.baseurl }}{% link _guide/installer-jekyll.md %}) |

---

### _Références_

* A propos de [Ruby](https://www.ruby-lang.org/fr/about/)
* [plugin WDM](https://github.com/Maher4Ever/wdm) pour scruter les changements dans les repertoires Windows
