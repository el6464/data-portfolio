# Projet 2 : Automatisation des fichiers SharePoint par Power Automate

## Objectif
Automatiser la gestion et le traitement des fichiers SharePoint afin de rationaliser les processus métiers, réduire les erreurs et améliorer l’efficacité du flux documentaire.

## Technologies utilisées
- Power Automate
- SharePoint
- OneDrive
- API Power BI (via OpenAPI)

## Étapes et méthodologie

### 1️⃣ Configurer la Recurrence
- Création d’un nouveau flux Power Automate avec le déclencheur **Recurrence**.
- Définition de la fréquence d’exécution (exemple : hebdomadaire) et de l’heure souhaitée.

### 2️⃣ Exporter vers un Fichier
- Ajout de l’action **Obtenir les éléments** pour extraire les informations de la liste ou bibliothèque SharePoint.
- Ajout de l’action **Créer un fichier** pour générer un rapport paginé au format XLSX via l’API Power BI.

### 3️⃣ Créer un Fichier Automatiquement
- Définition du chemin d’accès et du nom du fichier.
- Remplissage automatique des champs à partir des informations extraites.

## Résultat
- Les fichiers ajoutés ou modifiés dans SharePoint sont automatiquement transférés vers OneDrive ou d’autres serveurs.
- Les utilisateurs reçoivent des notifications automatiques lors des modifications.
- Les métadonnées des fichiers sont mises à jour automatiquement selon les règles définies.
- Les rapports sont générés pour résumer les nouveaux documents sans intervention manuelle.
- Les fichiers inactifs sont archivés et les processus d’approbation automatisés pour valider les modifications.
- Intégration avec d’autres applications logicielles pour synchronisation et automatisation des processus métiers.

  ## Captures d'écran  
# Mon Projet PowerShell sur VM

> **Pour des raisons de confidentialité, les captures d’écran de ce projet ne sont pas publiées ici. Elles peuvent être fournies sur demande.**

<!--  
Si tu souhaites montrer des captures, tu peux créer une version floutée ou basse résolution et héberger les images sur Cloudinary.  
Ensuite, remplace ce message par des balises <img> avec les URLs adaptées.  
-->
