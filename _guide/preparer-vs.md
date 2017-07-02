---
layout: page 
category: guide
title : Préparer VisualStudio Code pour blogger avec Jekyll 3
---
Pour préparer `Visual Studio Code` nous allons :

1. Installer des extensions à partir de la marketplace Visual Studio,
1. Configurer un raccourci de touches pour lancer la prévisualisation du rendu en live notre site.
1. Installer Git pour pouvoir cloner nos sites webs prêts à l'emploi
1. Installer un utilitaire Windows pour pouvoir déployer notre site avec le protocole `SFTP`.

---

> _Prérequis avant de contiunuer_  
> [:white_check_mark: installer Visual Studio Code](https://code.visualstudio.com/) en version 1.13 minimum

---

## 1. Installation des Extensions Visual Studio Code

Toutes les extensions dont nous avons besoin se trouvent sur la marketplace de Visual Studio :

- **Markdownlint** : controle la syntaxe markdown de votre texte brut.
- **Markdown shortcuts** : ajoute un menu contextuel pour la mise en forme de votre contenu, et des raccourcis clavier pour le gras, l'italique...
- **TODO Hightlight** : met en surbrillance du contenu à rédiger que vous remettez à plus tard.

Pour installer ces extensions, ouvrir Visual Studio Code, puis `CTRL+P` et saisissez tour à tour les commandes suivantes, en cliquant sur 'Install' et sur 'Reload' à chaque fois :

```shell
ext install vscode-markdownlint
ext install markdown-shortcuts
ext install vscode-todo-highlight
```

OK, à ce stade il peut être utile de fermer et de réouvrir Visual Studio Code.

---

## 2. Configurer un raccourci de touches

Nous utiliserons `CTRL + SHIFT + B` pour lancer un build unique de notre site. Cette combinaison de touche est standard dans Visual Studio aussi nous n'avons rien à configurer.

> _**Pour information** `CTRL + SHIFT + B` est associé à la tache qui possède la propriété `"isBuildCommand": true`. Nous vous fournissons le fichier `tasks.json` avec notre modèle de site prêt à l'emploi dans lequel ces taches sont préconfigurées._

Nous allons maintenant configurer la combinaison `CTRL + SHIFT + R` pour lancer la prévisualisation du rendu en live notre site.

Pour cela vous devez aller dans le menu `/Fichier/Préférences/Raccourcis clavier` puis tout en haut de la liste des raccourcis vous avez un lien qui permet d'ouvir le fichier de personnalisation `keybindings.json`. Cliquez dessus et modifiez le comme suit :

```settings
// Place your key bindings in this file to overwrite the defaults
[
    {
        "key": "ctrl+shift+r",
        "command": "workbench.action.tasks.runTask",
        "args": "liverender"
    }
]
```

Puis sauvegardez. C'est tout. Nous le testerons avec notre 1er site dans les prochaines étapes.

---

## 3. Installer GIT sur Windows

Visual Studio Code s'appuie sur l'installation GIT qui est déja présente sur votre PC, aussi vous avez besoin d'[installer GIT](https://git-scm.com/download) directement à partir du site officiel. Assurez-vous d'installer au moins la version `2.0.0`.

Redémarrez Visual Studio qui doit maintenant intégrer les fonctions de Git.

Pour vérifier, ouvrez le panneau de commande `CTRL + SHIFT + P` puis tappez `GIT`, vous devez voir apparaitre les commandes git :

![git-embededd-vs]({{ site.baseurl }}/assets/img/git-embededd-vs.png)

---

## 4. Installer l'utilitaire _PSFTP_ Windows

Windows intègre nativement une commande `FTP` mais pas une commande pour un transfert avec le [protocole sécurisé SFTP](https://fr.wikipedia.org/wiki/SSH_File_Transfer_Protocol). Donc pour pouvoir faire nos deploiements automatiques vers un `serveur SFTP` nous devons installer un utilitaire.

Nous utiliserons `PSFTP` qui est un des plus simples, des plus robustes et pour lequel les paramètres de transferts peuvent être personnalisés par un fichier de configuration.

Telechargez `PSFTP.exe` sur le [site officiel](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) en choisissant la version 32bits ou 64bits.

![psftp-download.png]({{ site.baseurl }}/assets/img/psftp-download.png)

Il est telement simple qu'il n'y a pas de programme d'installation ! Le programme `psftp.exe` telechargé se suffit à lui même.
Vous devez donc le déplacer dans un repertoire de votre PATH, comme `C:\Windows\System32` pour qu'il puisse s'executer depuis n'importe lequel de vos projets VS Code.

Pour tester que cela fonctionne, appelez le programme depuis une ligne de commande ouverte à la racine de vos dossiers personnels.

![psftp-ok.png]({{ site.baseurl }}/assets/img/psftp-ok.png)

---

## Conclusion

Voilà ce guide d'installation de votre environnement de travail est terminé.

A ce stade vous avez sur votre PC un environnement de travail pret pour créer des site et des blogs `Studio Jekyll`. Ils sont créables et testables sur votre PC, et publiables sur vos serveurs. Nous allons voir comment.

Récapitulons :  
:white_check_mark: ruby est installé sur votre PC  
:white_check_mark: jekyll 3 est opérationnel  
:white_check_mark: visual studio a été configuré  
:white_check_mark: vous avez accès aux repositories de GITHUB et vous allez donc pouvoir cloner un site de référence pour créer votre 1er site

Vous pouvez continuer avec le [Guide de création d'un nouveau site]({{ site.baseurl }}{% link _pages/guide-creation-site.md %}).

Let's go !

---

### _Références_

- [Visual Studio CODE](https://code.visualstudio.com/download) pour rédiger, tester et publier mes blogs.
- [VS Code Tips & tricks](https://github.com/Microsoft/vscode-tips-and-tricks), à tritre d'information.
- L'extension [Markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
- L'extension [Markdown shortcuts](https://marketplace.visualstudio.com/items?itemName=mdickin.markdown-shortcuts)
- L'extension [TODO Hightlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
- La [documentation de PSFTP](https://tartarus.org/~simon/putty-snapshots/htmldoc/Chapter6.html#psftp) de l'outil windows de transfert de fichiers via SFTP
