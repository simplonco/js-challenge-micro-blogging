# Comérage

Créer une plateforme de micro blogging qui s'appellera "Comérage". Cette application permettra au bloggueur 
de publier des articles courts de 200 caractères maximum.

1. [Brief](#brief)
    * [Description des entités](#description-des-entites)
2. [Analyse fonctionnelle](#analyse-fonctionnelle)
3. [Modélisation de la base de données ](#modelisation-bdd)
4. [Script de création de base données ](#script-bdd)
5. [Maquettes](#maquettes)
6. [Création des pages](#dev)
    * [Planning développement](#planning)
    * [Développement des pages](#dev-pages)
7. [Techno](#techno)
8. [Contraintes](#contraintes)
9. [A rendre](#a-rendre)
10. [Ressources](#ressources)

Temps estimé : 1 semaine.

Vous ferez une présentation des fonctionnalités à la fin.

# <a name="brief"></a>Brief

Pour l'application, nous identifierons 2 types d'utilisateurs :

- L'internaute qui est utilisateur non connecté
- Le blogueur qui est un utilisateur enregistré sur le site

User stories :

- En tant qu'internaute je veux m'inscrire au site afin de pouvoir poster mes articles 
- En tant que blogueur je veux me connecter via une interface sécurisée au site
- En tant que blogueur je veux pouvoir poster un article de 200 caractères max afin que tout le monde puisse commenter
- En tant qu'internaute je veux pouvoir voir la liste de tous les articles
- En tant que blogueur je veux pouvoir modifier mes propres articles afin de rectifier les informations
- En tant que blogueur je veux pouvoir supprimer mes propres articles et les commentaires associées 
- En tant que blogueur je veux pouvoir commenter n'importe quel article
- En tant que blogueur je veux pouvoir attribuer une catégorie à mon article
- En tant que blogueur je veux pouvoir trier les articles selon les catégories
- En tant que blogueur je veux que l'interface m'indique le nombre de caractères en temps réel afin de savoir combien de caractères il me reste à utiliser

Bonus : 

- En tant qu'utilisateur je veux pouvoir supprimer mes commentaires
- En tant qu'utilisateur je veux pouvoir modifier mes commentaires

## <a name="description-des-entites"></a>Description des entités

- Un article possède obligatoirement un corps 
- Un article possède obligatoirement une ou plusieurs catégories.
- Un article possède obligatoirement une date de publication
- Un article est lié obligatoirement à un utilisateur et un seul mais un utilisateur peut publier plusieurs articles
- Un article possède un champ qui détermine si l'article est visible ou pas.
- Un commentaire possède obligatoirement un corps 
- Un commentaire possède obligatoirement une date de publication
- Un commentaire est obligatoirement lié à un utilisateur et un seul mais un utilisateur peut publier plusieurs commentaires
- Un commentaire est obligatoirement associé à un article est un seul, mais un article peut avoir plusieurs commentaires
- Un utilisateur possède obligatoirement un surnom
- Un utilisateur possède obligatoirement un email qui est unique à l'application (il ne peut pas avoir 2 utilisateurs avec le même email)
- Une catégorie possède uniquement un nom

# <a name="analyse-fonctionnelle"></a>Analyse fonctionnelle (30min)

Selon le brief, créer le diagramme de cas d'utilisation qui reflète le périmètre de l'application.

> **Avant de passer à l'étape suivante : la modélisation doit être validé par le facilitateur**

# <a name="modelisation-bdd"></a>Modélisation de la base de données (45min)

A l'aide d'un **diagramme de classe** modéliser toutes entités de la base de données.

> **Avant de passer à l'étape suivante : la modélisation doit être validé par le facilitateur**

# <a name="script-bdd"></a>Script de création de base donnée (30min)

Créer les scripts SQL de création de la base de données (tables, relations, etc.).

Vous pouvez utiliser un logiciel de modélisation (Mysql WorkBench).

> **Avant de passer à l'étape suivante : expliquer les différentes instructions du script au facilitateur**

# <a name="maquettes"></a>Maquettes (1h30)

Réaliser les maquettes fonctionnelles des différentes pages. Vos maquettes doivent être ergonomiques. Vous devez faire apparaître les interactions
utilisateurs ainsi que les liens entre les différentes pages

Vous pouvez utiliser le logiciel de modélisation de votre choix. 

> **Avant de passer à l'étape suivante : faites valider votre maquette par le facilitateur** 

# <a name="dev"></a>Création des pages

## <a name="planning"></a>Planning développement (30 min)

Établissez un planning de développement en choississant l'ordre des user stories réalisées et des fonctionnalités. Pour cela, vous pouvez utiliser trello.

Dans ce planning dois apparaitre : 

- Les users stories 
- Les fonctionnalités à développer pour ces users stories
- Le temps estimé pour chaque fonctionnalité

> **Avant de passer à l'étape suivante : Faites valider votre planning** 

## <a name="dev-pages"></a>Développement des pages

Vous devez développer, à minima, toutes les fonctionnalités sans les bonus. 

*Conseil* : 

- *Réfléchissez à la structure des dossiers et fichiers*
- *Pensez, dès la création des pages, au layout afin de ne pas répéter header et footer sur toutes les pages...*

# <a name="techno"></a>Techno 

- ExpressJS
- Pour la vue au choix : Jade, Mustache, Handlebars
- MySQL 5.5
- Bootstrap Twitter

# <a name="contraintes"></a>Contraintes

- Toutes les fonctionnalités doivent être fonctionnelles (Sauf les bonus)
- Vous devez structurer votre code selon le modèle MVC. Dans votre architecture de fichiers, on doit bien voir les différentes parties.
- Votre code être pensé Orienté Objet
- Vous devez développer le compteur de caractères en TDD (Test Driven Development)
- Votre code doit être commenté
- Le site doit être responsive et respecter les maquettes.
- Le design doit être propre et professionnel. **Ne passer trop de temps dessus non plus**

# <a name="a-rendre"></a>À rendre 

- Les diagrammes (utilisations, classes, etc.)
- Les maquettes des pages sous format images
- Lien vers le repo
- Lien vers trello
- Le schéma physique de la base de données
- Les scripts de création/sauvegarde/restauration de base de données

# <a name="ressources"></a>Ressources 

- [Diagramme de cas d'utilisation](http://lipn.univ-paris13.fr/~gerard/uml-s2/uml-cours04.html)
- [Modélisation base de données et diagramme de classe](https://www.irit.fr/~Thierry.Millan/CNAM-NFP107/UML%20et%20les%20Bases%20de%20Donn%C3%A9es.pdf)
- [Desing pattern MVC](https://github.com/simplonco/node-mvc-sqlite-step1)
- [L'orientée objet en JS](https://buzut.fr/programmation-orientee-objet-javascript/)
- [Node.js Server & Authentication Basics: Express, Sessions, Passport, and cURL](https://medium.com/@evangow/server-authentication-basics-express-sessions-passport-and-curl-359b7456003d)
- [Sequelize an Node ORM](https://sequelize.readthedocs.io/en/v3/)
- [Mockflow : outil de maquettage en ligne](https://www.mockflow.com/)
- [Tester son code avec Jest](https://jestjs.io/docs/en/getting-started)

