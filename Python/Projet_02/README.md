# Projet : Analyse des compétences des étudiants par Machine Learning

## Objectif
Évaluer et comparer les performances de quatre algorithmes de Machine Learning :
- Régression Logistique (LR)
- Decision Tree (DT)
- Random Forest (RF)
- K-Nearest Neighbors (KNN)

Le but est de prédire correctement le placement des étudiants en fonction de leurs compétences.

---

## Prétraitement des données
- Suppression des doublons  
- Encodage des variables textuelles (Skill 1, Skill 2, Profil)  
- Analyse des données :
  - Statistiques descriptives  
  - Boîtes à moustaches (boxplots)  
  - Matrice de corrélation  

Les matières les plus corrélées au succès sont :  
- CN  
- DSA  
- Mathematics  
- Aptitude

---

## Modèles testés
1. **Régression Logistique (LR)**
2. **Decision Tree**
3. **Random Forest**
4. **KNN**

Chaque modèle a été :
- Optimisé via GridSearchCV  
- Évalué avec :
  - Test Accuracy  
  - Classification Report  
  - Confusion Matrix  
  - Learning Curve

---

## Résultats

| Modèle | Accuracy | Erreurs (Confusion Matrix) | Rang |
|--------|----------|----------------------------|------|
| LR | **100%** | 0 | 🥇 |
| KNN | 98.59% | 0 | 🥈 |
| Random Forest | 95.77% | 3 | 🥉 |
| Decision Tree | 84.51% | 11 | 4 |

### Conclusion
- **La Régression Logistique (LR)** est le meilleur modèle, avec 100% de précision.  
- KNN obtient d’excellents résultats également.  
- Decision Tree présente un surapprentissage notable.

---

## Captures d'écran  
> **Pour des raisons de confidentialité, les captures d’écran de ce projet ne sont pas publiées ici. Elles peuvent être fournies sur demande.**
>
> <!--  
Si tu souhaites montrer des captures, tu peux créer une version floutée ou basse résolution et les héberger sur Cloudinary.  
Ensuite, remplace ce message par des balises <img> avec les URLs adaptées.  
-->

---

## Points forts du projet
- Traitement complet de données réelles  
- Comparaison équitable des algorithmes  
- Analyse approfondie des courbes d’apprentissage  
- Basé uniquement sur du code Python reproductible

---

## Notes
- Projet compatible Python 3+ et scikit-learn  
- Le dataset peut être fourni sur demande  
- Toutes les visualisations sont disponibles sur demande


