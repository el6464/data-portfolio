# Projet : Gestion des commandes et articles avec PostgreSQL

## Objectif
Mettre en place une base de données PostgreSQL pour gérer les **articles, clients et commandes**, avec des requêtes SQL pour l’analyse, l’importation et le suivi des données.

---

## Technologies utilisées
- **PostgreSQL** : Base de données relationnelle  
- **SQL** : Requêtes pour extraction, transformation et chargement (ETL)  
- **Power BI / Tableau / autre outil BI** (optionnel) : Visualisation des données

---

## Structure des tables

```sql
-- Table Clients
CREATE TABLE clients (
    client_id SERIAL PRIMARY KEY,
    nom VARCHAR(100),
    prenom VARCHAR(100),
    email VARCHAR(150),
    date_creation TIMESTAMP DEFAULT NOW()
);

-- Table Articles
CREATE TABLE articles (
    article_id SERIAL PRIMARY KEY,
    nom VARCHAR(100),
    categorie VARCHAR(50),
    prix NUMERIC(10,2)
);

-- Table Commandes
CREATE TABLE commandes (
    commande_id SERIAL PRIMARY KEY,
    client_id INT REFERENCES clients(client_id),
    date_commande DATE,
    montant_total NUMERIC(12,2)
);

-- Table Commandes_Articles (relation many-to-many)
CREATE TABLE commandes_articles (
    commande_id INT REFERENCES commandes(commande_id),
    article_id INT REFERENCES articles(article_id),
    quantite INT,
    prix_unitaire NUMERIC(10,2),
    PRIMARY KEY (commande_id, article_id)
);

