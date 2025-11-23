# Projet : Gestion et Importation des Données dans un Data Warehouse PostgreSQL

## Objectif
Mettre en place un processus complet pour **importer, transformer et gérer les données** dans un **Data Warehouse PostgreSQL** afin de faciliter l’analyse et la génération d’indicateurs.

---

## Technologies utilisées
- **PostgreSQL** : Base de données relationnelle pour le stockage et l’organisation des données  
- **SQL** : Requêtes pour extraction, transformation et chargement (ETL)  
- **Power BI / Tableau / autre outil de BI** : Visualisation des données  
- **Python / scripts ETL** (optionnel) : Automatisation de l’importation et de la transformation  
- **SharePoint / fichiers plats** : Sources de données

---

## Étapes et méthodologie

1. **Collecte des données**  
   - Extraction des données depuis différentes sources (fichiers CSV/Excel, SharePoint, bases externes).  
2. **Nettoyage et transformation**  
   - Vérification de la qualité des données (doublons, valeurs manquantes).  
   - Transformation pour correspondre au schéma du Data Warehouse.  
3. **Importation dans le Data Warehouse**  
   - Utilisation de scripts SQL ou d’outils ETL pour charger les données dans PostgreSQL.  
4. **Gestion et suivi des données**  
   - Mise en place de procédures pour mettre à jour, archiver ou purger les données.  
   - Création de vues ou tables matérialisées pour faciliter l’accès aux indicateurs.  
5. **Contrôle et validation**  
   - Vérification de la cohérence des données importées.  
   - Test des requêtes d’analyse et de reporting.

---

## Structure des tables (exemple)
```sql
-- Table des clients
CREATE TABLE clients (
    client_id SERIAL PRIMARY KEY,
    nom VARCHAR(100),
    prenom VARCHAR(100),
    email VARCHAR(150),
    date_creation TIMESTAMP
);

-- Table des ventes
CREATE TABLE ventes (
    vente_id SERIAL PRIMARY KEY,
    client_id INT REFERENCES clients(client_id),
    date_vente DATE,
    montant NUMERIC(10,2)
);

