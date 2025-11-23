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
  - `Clients` → `Commandes` (1:n)  
  - `Articles` → `Commandes_Articles` (1:n)  
  - `Commandes` → `Commandes_Articles` (1:n)  

---
# Mon Projet Acess

> **Pour des raisons de confidentialité, les captures d’écran de ce projet ne sont pas publiées ici. Elles peuvent être fournies sur demande.**

<!--  
Si tu souhaites montrer des captures, tu peux créer une version floutée ou basse résolution et héberger les images sur Cloudinary.  
Ensuite, remplace ce message par des balises <img> avec les URLs adaptées.  
-->
## Exemples de requêtes SQL

### 1️⃣ Total des ventes par client
```sql
SELECT c.nom, SUM(ca.quantite * ca.prix_unitaire) AS total_ventes
FROM Clients c
JOIN Commandes co ON c.client_id = co.client_id
JOIN Commandes_Articles ca ON co.commande_id = ca.commande_id
GROUP BY c.nom;
