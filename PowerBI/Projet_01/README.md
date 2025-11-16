# Projet Power BI - Dashboard Ventes

## Objectif
Créer un dashboard pour visualiser les ventes mensuelles.

## Technologies
- Power BI
- SQL (pour extraire les données)

## Captures d'écran
![exemple_dashboard](screenshots/01_dashboard.png)

## Extrait de code SQL (non réutilisable)
```sql
SELECT customer_id, SUM(amount) AS total_ventes
FROM ventes
GROUP BY customer_id;

