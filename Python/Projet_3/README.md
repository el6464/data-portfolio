# Projet : Automatisation Excel → SQL via ODBC (DHL)

## 🎯 Objectif
Ce projet a été réalisé dans le cadre d'une mission chez **DHL**.  
Il consiste à automatiser la connexion entre **Excel** et une **base SQL** via **ODBC**, afin de :

- Charger automatiquement des données Excel vers SQL
- Exécuter des requêtes SQL depuis Excel
- Mettre à jour les rapports opérationnels en temps réel
- Permettre un échange fluide de données entre Excel et le Data Warehouse interne

Cette automatisation permet de réduire les erreurs manuelles, d’accélérer les flux opérationnels et d’améliorer la qualité des données.

---

## 🧰 Technologies utilisées
- **Microsoft Excel**
- **ODBC**
- **Python (optionnel pour automatisation avancée)**
- **SQL Server / MySQL / PostgreSQL** selon l’environnement client
- **Macros Excel (VBA)** selon les besoins

---

## 🔧 Étapes du projet

### 1️⃣ Configuration de la connexion ODBC
Création d'un DSN ODBC sur Windows :
- Choix du driver SQL Server / MySQL / PostgreSQL
- Configuration du serveur, base, port, type d’authentification
- Test de la connexion

Exemple DSN : `DHL_Production_ODBC`

---

### 2️⃣ Connexion Excel ↔ SQL

#### ✔ Méthode 1 : Via Excel (Power Query)
1. **Données → Obtenir des données → À partir d'ODBC**
2. Sélection du DSN configuré
3. Importation des tables / vues
4. Transformation Power Query si nécessaire
5. Planification du rafraîchissement automatique

#### ✔ Méthode 2 : Via VBA (macro)
Exemple de code :

```vba
Sub ChargerDonneesSQL()

    Dim Conn As Object
    Set Conn = CreateObject("ADODB.Connection")
    
    Conn.Open "DSN=DHL_Production_ODBC;UID=user;PWD=password"

    Dim rs As Object
    Set rs = Conn.Execute("SELECT * FROM commandes WHERE statut = 'EN COURS'")
    
    Sheet1.Range("A2").CopyFromRecordset rs
    
    Conn.Close
End Sub
