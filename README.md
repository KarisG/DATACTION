![Logo](https://github.com/KarisG/DATACTION/blob/main/loggo.png)

Dataction
============================

Notre application Web *Dataction* permet de détecter si une image fournie par un utilisateur contient un déchet plastique, et où se trouve cette image sur une carte. Pour cela, nous renseignons les coordonnées de l'image au préalable, nous la chargeons et nous l'analysons.

Prérequis
-----------------------
Python 3.8.XX 

Afin de pouvoir exécuter l'application sur votre ordinateur, vous devez tout d'abord installer les dépendancesnces avec la commande suivante dans la racine du projet:
	
```bash
pip install -r requirements.txt
```

Exécution
-----------------------
Afin de lancer l'application ouvrez un invite de commande ou shell à la racine du projet et exécutez la commande suivante :
```bash
python manage.py runserver
```
Au lancement du site le modèle d'IA est chargé, cette opération peut prendre entre une et deux minutes et soulève un certain nombre de warning à ignorer.

Ensuite pour accéder à la page d'accueil de l'application rendez-vous à l'adresse suivante via votre navigateur **http://127.0.0.1:8000/dataction/**.

Tests fonctionnalités
-----------------------
Pour tester le bon fonctionnement des différentes fonctionnalités de l'application vous pouvez procéder aux actions suivantes:

1. Sur la page **http://127.0.0.1:8000/dataction/submit/** soumettez une image en prenant soin de suivre les instructions, vous devriez être redirigé vers la page correspondante à l'image soumise. ATTENTION à l'heure actuelle l'image doit obligatoirement se situé dans le dossier image prévu à cet effet situé à la racine du projet.
2. Sur la page **http://127.0.0.1:8000/dataction/point_index/** vous devriez voir la liste des points enregistrés localement dans l'application, vous pouvez clicker sur un point afin d'accéder au détail de celui-ci.
3. Sur la page **http://127.0.0.1:8000/dataction/global_map/** vous devriez voir s'afficher une carte affichant l'ensemble des points enregistrés localement dans l'application. ATTENTION cette page ne fonctionne correctement que si une clé D'API google maps valide est utilisé dans le code. La clé utilisée dans notre cas est nominative et ne fonctionnera donc pas pour vous. Si vous le souhaité vous pouvez remplacer la clé dans le code par une valide en suivant les instructions sur la page suivante **https://developers.google.com/maps/documentation/android-sdk/get-api-key?hl=fr**


Fonction d'administration
-----------------------
Le site dispose d'un ensemble de pages d'administration fournit par django pour y accéder rendez-vous à l'adresse **http://127.0.0.1:8000/admin/**
Pour vous connecter, vous pouvez créer un superuser avec la commande suivante : 
```bash
python manage.py createsuperuser
```
ou bien utilisez le compte créé uniquement dans un but de démonstration:
Username : admin
Password : ultrasecurepwd

Outils et Langages de dévellopement
-----------------------
Visual Studio Code
Python - HTML - CSS - Javascript

## Exemple de chargement d'image

![Chargement d'une image](https://github.com/KarisG/DATACTION/blob/main/chargement.png)

## Exemple de détection

![Chargement de détection](https://github.com/KarisG/DATACTION/blob/main/bouteille.PNG)


Contibuteurs
-----------------------
* Abdel Bekhouche : Design
* Armand Boudin : Développeur WEB/Design
* Nil Cailleux : Cartographie
* Karis Gwet : Développeur IA
* Mathieu Hanania : Cartographie
* Moise Iloo : Développeur IA
