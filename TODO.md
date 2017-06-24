# Backlog StudioJekyll for Windows

TODO:

## Fonctionnalités

- [x] gestion des erreurs de pages 404
- [x] sitemap
- [x] Disqus
- [ ] gestion des tags
- [ ] SEO
- [ ] analytics
- [ ] pré-traitement des fichiers image
- [ ] boutons sociaux
- [ ] multilingues https://www.sylvaindurand.fr/rendre-jekyll-multilingue/
- [ ] vérifier orthographe et grammaire. /!\ ds VSCODE la seule extention existante sur la marketplace ['Code Spellchecker'](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) ne controle que l'Anglais.

# Rédactions
- [ ] générer les entetes yaml
- [ ] checker https://jekyllrb.com/docs/variables/
- [ ] customiser markdowlint

## design

- [ ] migrer theme CSS vers SASS
- [x] ombres autour des images
- [ ] logo StudioJekyll
- [ ] angular ?

## fix

- [x] blancs ajoutés dans html par jekyll. Voir https://shopify.github.io/liquid/basics/whitespace/ 
- [x] double header sur les articles de blog
- [x] code blocks mal rendus
- [x] robots.txt et non robot.txt
- [x] gestion des environnements
- [ ] convertir tous les link et permalink en minuscules
- [ ] title incorrect sur page blog.html

## CI / Deploiement

- [x] process publication : lan, sftp
- [x] publications 'propres' : vider les repertoires de destination avant de republier, forcer le transfert de .htaccess
- [x] ouvrir explorateur après deploiement avec URL du site publié selon la destination
- [ ] créer des taches de test : vérification des liens URL, des images etc (idéalement extension ruby HTMLproofer mais ne fonctionne pas, voir aussi une extension qui controle les liens en live, comme MDlint qui vérifie la syntaxe markdown en cours de frappe.)
- [ ] incrément automatique des versions
- [ ] automatiser gitcommit et gitpush avec le deploiement en production
