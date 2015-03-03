Cas concret - Description fonctionnelle
---------------------------------------

### Introduction
L'application permet de visualiser, de gérer des données métiers, supportées par des données de référence cartographique et de restituer ces données sous forme de tableau...  
L'application est constituée :
- d'une interface cartographique, 
- d'une légende dynamique contenant les données de référence et métier,
- de menus de recherche, de gestion de données (saisie, modificatio et suppression) et de reporting.

### Fonctionnalités
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
