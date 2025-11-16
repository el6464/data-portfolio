# Projet 1 : Requêtes Indicateurs de Performance

## Objectif
Calculer et visualiser 133 indicateurs de performance pour ASTEO afin de garantir la conformité contractuelle avec Toulouse Métropole.  

## Technologies utilisées
- Power BI (Power Query, DAX)
- SQL (PostgreSQL / MySQL selon les données)
- SharePoint (source des fichiers)

## Données / Sources
- Entrepôt de Données (EDD)
- SharePoint

## Étapes et méthodologie
1. Extraction et traitement des données depuis l’EDD et SharePoint
2. Intégration dans Power BI via Power Query
3. Création de requêtes DAX pour calcul des indicateurs
4. Construction des tableaux de bord dynamiques pour visualisation et suivi en temps réel

## Captures d'écran
![Exemple Dashboard](screenshots/01_dashboard.png)

## Extrait de code (SQL)
```sql
SELECT customer_id, SUM(amount) AS total_ventes
FROM ventes
GROUP BY customer_id;
