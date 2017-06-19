# Backlog StudioJekyll for Windows

TODO:

## fonctionnalités

- [x] gestion des erreurs de pages 404
- [ ] migrer theme CSS vers SASS avec prise en compte du style block code (ext rouge)
- [ ] SEO
- [ ] analytics
- [ ] pré-traitement des fichiers image
- [ ] sitemap (voir dans doc jekyll)
- [ ] angular ?
- [ ] logo StudioJekyll
- [ ] boutons sociaux
- [ ] multilingues https://www.sylvaindurand.fr/rendre-jekyll-multilingue/
- [ ] vérifier orthographe et grammaire. /!\ ds VSCODE la seule extention existante sur la marketplace ['Code Spellchecker'](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) ne controle que l'Anglais.
- [ ] générer les entetes yaml
- [ ] checker https://jekyllrb.com/docs/variables/
- [ ] customiser markdowlint

## fix

- [ ] blancs ajoutés dans html par jekyll
- [ ] convertir tous les link et permalink en minuscules
- [ ] double header sur les articles de blog

## CI

- [ ] créer des taches de test : vérification des liens URL, des images etc (idéalement extension ruby HTMLproofer mais ne fonctionne pas, voir aussi une extension qui controle les liens en live, comme MDlint qui vérifie la syntaxe markdown en cours de frappe.)
- [ ] incrément automatique des versions
- [ ] publication : vider les repertoires de destination avant de republier
- [ ] process publication sftp : droits https://github.com/mkloubert/vs-deploy/wiki/target_sftp#modes-for-specific-files

## explications / documentation

- [ ] compilateur SAAS inclus avec Jekyll3