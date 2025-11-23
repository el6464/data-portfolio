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

---

## Captures d'écran  
# Mon Projet PowerBI

Voici les captures du projet :

<p align="center">
  <img src="https://res.cloudinary.com/dhhksoj5c/image/upload/v1763899772/DZVDV_p3jmki.png" width="30%">
  <img src="[https://URL-DE-TON-IMAGE-2.png](https://res.cloudinary.com/dhhksoj5c/image/upload/v1763899772/DZVDV_p3jmki.png)" width="30%">
  <img src="https://res.cloudinary.com/dhhksoj5c/image/upload/v1763899600/Capture_d_%C3%A9cran_2024-06-10_141534_ynd77a.png" width="30%">
</p>

<p align="center">
  <img src="https://res.cloudinary.com/dhhksoj5c/image/upload/v1763899567/Capture_d_%C3%A9cran_2024-06-10_135508_wygpou.png" width="30%">
  <img src="[https://URL-DE-TON-IMAGE-5.png](https://res.cloudinary.com/dhhksoj5c/image/upload/v1763899345/Capture_d_%C3%A9cran_2024-08-29_155557_besv8p.png)" width="30%">
  <img src="[https://URL-DE-TON-IMAGE-6.png](https://res.cloudinary.com/dhhksoj5c/image/upload/v1763899302/9_t8c0cx.png)" width="30%">
</p>

---

## Extrait de code (SQL)

```sql
SELECT customer_id, SUM(amount) AS total_ventes
FROM ventes
GROUP BY customer_id;
