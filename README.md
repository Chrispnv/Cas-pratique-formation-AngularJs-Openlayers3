##Cas concret - Description fonctionnelle
________________________________________

Introduction
--------------
L'application permet de visualiser, de gérer des données métiers, supportées par des données de référence cartographique et de restituer ces données sous forme de tableau...  
L'application est constituée :
- d'une interface cartographique, 
- d'une légende dynamique contenant les données de référence et métier,
- de menus de recherche, de gestion de données (saisie, modificatio et suppression) et de reporting.

Fonctionnalités
---------------
#### Authentification et autorisation d'accès
L'application est accessible en s'identifiant par login/pass. 
Question : est ce la partie serveur (Symfony2) qui gère cela ou est ce la partie client  (AngularJs) ?
#### Interface cartographique
- Le fond de référence cartographique est basée sur l'API Géoportail par défaut et sur des fonds plus spécifiques au territoire (MNT...).
- On retrouve toutes les fonctionnalités classiques de zoom, de centrage...

#### Légende dynamique
- Affichage des fonds carto autre que l'API IGN
  - Fonction visibilité/non visibilité des fonds (même fond IGN par défaut),
  - Fonction transparence des fonds cartographiques (ex superposer fond 25000e et photos aériennes),
- Affichage des données vectorielles de référence
  - Fonction visibilité/non visibilité,
  - Fonction transparence,
  - Fonction de modification graphique (couleur, grosseur objets).
- Affichage des données vectorielles métier
  - Fonction visibilité/non visibilité,
  - Fonction transparence,
  - Fonction de modification graphique (couleur, grosseur objets),
  - Affichage tableau données attributaires accompagnant les données métier.

#### Gestion des données
Fonctions de saisie, de modification et de suppression de données métier (objets géographiques et données attributaires). C'est à dire :
- Saisie 
  - Saisie d'un objet géographique sur la carte avec ouverture d'un formulaire pour la saisie des données attributaires, avec suppression de l'objet géographique si le formulaire est fermé sans soumission,
  - Selon la donnée métier, saisie d'un point ou d'une ligne.
- Modification
  - Fonction permettant de déplacer un objet géographique métier sur la carte
  - Fonction permettant d'accéder au formulaire d'un objet rempli avec ses données attributaires pour les modifier :
    - En cliquant sur l'objet dans la carte,
    - En sélectionnant l'objet dans un tableau de résultats.
- Suppression
  - Fonction permettant de supprimer un ou plusieurs objets métiers sur la carte avec une sélection ponctuelle ou avec un polygone,
  - Fonction permettant de supprimer un ou plusieurs objets depuis un tableau de résultats.
- Formulaire
  - Fonctions dynamiques du formulaire : 
    - Visibilité champs dépendants remplissage d'autres champs,
    - Valeurs champs dépendants remplissage d'autres champs,
    - Saisie semi-automatique dans les listes déroulantes.

#### Recherche sur les données
- Interface de requétage sur les données métiers (affichage du même type que la légende),
- Possibilité de requêter :
  - que géographiquement sur les données métiers (point, polygones, voire zone tampon...),
  - qu'attributairement sur les données métiers,
  - géographiquement et attributairement mixé,
  - ? à voir si pertinent de lancer une requête sur les différentes données métiers ou sur qu'une seule à la fois ?
- Résultats de la requête prennent les comportements graphiques des données présentes dans la légende (transparence, changement aspect graphique...),
- Fonctions de gestion (modification, suppression) des données métier à partir du résultats de la requête, 
- ? à voir possibilité d'enregistrer les requêtes ?

#### Restitution & export
- Restitution de données ou de resultats de requête sous forme d'information statistiques,
- Export de données ou de resultats de requête avec choix des champs à exporter :
  - Fichier plat (csv, xls, txt ...),
  - Couche géographique (shp, gpx, kml...).
