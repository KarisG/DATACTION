![EFREI Paris](https://www.efrei.fr/wp-content/uploads/2019/06/Logo-Efrei-2017-Eng-Web.png)

Dataction
============================

Notre application Web *Dataction* permet de détecter si une image fournit par un utilisateur contient un déchet plastique, et où se trouve cette image sur une carte. Pour cela, nous renseignons les coordonnées de l'image au préalable, nous la chargeons et nous l'analysons.

Prérequis
-----------------------
python 3.8.XX 

Afin de pouvoir exécuter l'application sur votre ordinateur, vous devez tout d'abord installer les dépendences avec la commande suivante dans la racine du projet:
	
```bash
pip install -r requirements.txt
```

Exécution
-----------------------
Afin de lancer l'application ouvrez un invite de commande ou shell à la racine du projet et executé la commande suivante :
```bash
python manage.py runserver
```
Au lancement du site le modèle d'IA est chargé, cette opération peu prendre entre une et deux minutes et soulève un certain nombre de warning à ignorer.

Ensuite pour accéder à la page d'accueil de l'application rendez vous à l'adresse suivante via votre navigateur **http://127.0.0.1:8000/dataction/**.

Tests
-----------------------
Pour testé le bon fonctionnement des différentes fonctionnalité de l'application vous pouvez procédez au action suivante

1. Sur la page **http://127.0.0.1:8000/dataction/submit/** soummetez une image en prenant soin de suivre les instructions, vous devriez être redirogé vers la page correspondante à l'image soummise. ATTENTION à l'heure actuel l'image doit obligatoirement se situé dans le dossier image prévu à cet effet.
2. Sur la page **http://127.0.0.1:8000/dataction/point_index/** vous devriez voir la liste des point enregistré localement dans l'application, vous pouvez clické sur un point afin d'accéder au détail de celui-ci.
3. Sur la page **http://127.0.0.1:8000/dataction/global_map/** vous devriez voir s'affiché une carte affichant l'emsemble des point enregistré localement dans l'application. ATTENTION cette page ne fonctionne correctement que si une clé D'API google maps valide est utilisé dans le code. la clé utilisé dans notre cas est nominative et ne fonctionneras donc pas pour vous. Si vous le souhaité vous pouvez remplacé la clé dans le code par une valide créable en suivant les instruction sur la page suivante **https://developers.google.com/maps/documentation/android-sdk/get-api-key?hl=fr**
