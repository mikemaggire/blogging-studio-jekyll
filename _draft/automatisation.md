
dans task manager, on va appeler un script nodejs, qui se lance à partir de npm

### _Références_

* Très bon article trufé d'exemples de [@Keith Cirkel](https://twitter.com/keithamus) 
[How to Use npm as a Build Tool] https://www.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/
* Pourquoi nous n'utilisons pas grunt ni gulp https://www.keithcirkel.co.uk/why-we-should-stop-using-grunt/


package.json
{
  "name": "myproject",
  "devDependencies": {
    "jshint": "latest",
    "browserify": "latest",
    "mocha": "latest"
  },
  "scripts": {
    "lint": "jshint **.js",
    "test": "mocha test/"
	"deploy2prod": 
  }
}


Nous avons besoin d'une tache de build simple
Nous avons besoin d'une tache de build live
	Nous l'appelerons Start
	lance en tache de fond 
		jekyll build --watch --incremental -environement:local
	lance en tache de fond
		lite-server

Nous avons besoin d'une tache de cleaning
	arrete les taches de fonds
	lance
		jekyll clean
		supprime les repertoires de build et de deploiement

Nous avons besoin d'une commande qui stoppe toutes les taches de fond
	Nous l'appelerons stop
	
		
Nous avons besoin d'une tache de test
	lance un build unique
		jekyll build --config _config.yml,_config_test.yml --environement:production
	puis une fois terminé
		deploy vers bigmama
	puis une fois terminé
		lance directement l'explorateur à la bonne url
		
Nous avons besoin d'une tache de publication
	lance un build unique 
		jekyll build --config _config.yml,_config_test.yml --environement:production
	puis une fois terminé
		deploy vers bigmama



Variables de substitution dans Deploy ou Task
		https://code.visualstudio.com/docs/editor/tasks#_variable-substitution

		