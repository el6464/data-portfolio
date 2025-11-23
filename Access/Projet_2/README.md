# Projet : Gestion des commandes et articles avec Microsoft Access et SQL

## Objectif
Mettre en place une base de données Access pour gérer les **commandes et articles**, avec des requêtes SQL pour l’extraction et l’analyse des données.  

---

## Technologies utilisées
- **Microsoft Access** : Base de données relationnelle locale pour gestion des commandes et articles  
- **SQL** : Requêtes pour extraction, calculs et reporting  

---

## Structure de la base Access
- **Tables principales** :
  - `Articles` : Informations sur les produits (ID, nom, catégorie, prix)  
  - `Clients` : Informations sur les clients (ID, nom, email)  
  - `Commandes` : Informations sur les commandes (ID, ID client, date, montant total)  
  - `Commandes_Articles` : Table de liaison entre commandes et articles (quantité, prix unitaire)  

- **Relations** :  
  - `Clients` →
