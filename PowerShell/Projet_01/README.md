# Projet : Automatisation avec PowerShell sur VM - Exécution programmée d’un fichier

## Objectif
Créer un script PowerShell pour automatiser l’exécution d’un fichier via le **Planificateur de tâches** sur une **machine virtuelle Windows**.  
L’objectif est de permettre des tests et des exécutions planifiées dans un environnement isolé sans affecter la machine principale.

---

## Environnement
- **VM Windows** (Windows 10 / 11 ou serveur)  
- **PowerShell 5.1 ou supérieur**  
- **Planificateur de tâches Windows**  

> Le projet a été développé et testé exclusivement sur une VM pour garantir un environnement sûr et isolé.

---

## Fonctionnalités du script
1. Création d’une tâche planifiée dans le Planificateur de tâches Windows de la VM.  
2. Paramétrage :
   - Chemin du fichier à exécuter
   - Nom et fréquence de la tâche
   - Heure exacte de lancement
   - Droits administrateur si nécessaire  
3. Vérification de l’existence d’une tâche du même nom et mise à jour automatique si besoin.  
4. Logs d’exécution pour le suivi et le débogage.

---

## Captures d'écran  
# Mon Projet PowerShell sur VM

> **Pour des raisons de confidentialité, les captures d’écran de ce projet ne sont pas publiées ici. Elles peuvent être fournies sur demande.**

<!--  
Si tu souhaites montrer des captures, tu peux créer une version floutée ou basse résolution et héberger les images sur Cloudinary.  
Ensuite, remplace ce message par des balises <img> avec les URLs adaptées.  
-->

---

## Exemple d’utilisation sur la VM
1. Se connecter à la VM Windows.  
2. Ouvrir PowerShell avec droits administrateur.  
3. Lancer le script avec les paramètres souhaités :
```powershell
.\AutomatisationPlanificateur.ps1 -NomTache "MaTacheVM" -CheminFichier "C:\VM\MonFichier.exe" -Heure "08:00"

