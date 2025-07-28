# Analyse des accidents corporels de la route en France

---

## 📁 Données utilisées

Les données proviennent de la base ouverte du Ministère de l’Intérieur français :  
- **Accidents** : caractéristiques des événements  
- **Usagers**, **Véhicules**, **Lieux**  
- **Variables spatiales** (communes, départements, coordonnées GPS)

📎 Sources : [data.gouv.fr - BAAC](https://www.data.gouv.fr/fr/datasets/base-de-donnees-accidents-corporels-de-la-circulation/)

---

## 🛠️ Méthodologie

### 1. Préparation des données
- Fusion de 10 fichiers (.csv) contenant des clés multiples
- Nettoyage, recodage et enrichissement des variables

### 2. Analyse exploratoire
- Étude des distributions et des corrélations
- Visualisations univariées et croisées (graphiques, heatmaps)

### 3. Analyse statistique
- Tests d’indépendance (Chi²) entre variables qualitatives et gravité
- Analyse des correspondances multiples (ACM)
- Analyse en composantes principales (ACP) sur variables numériques

### 4. Modélisation
- Régression logistique (GLM multinomiale et binomiale) pour prédire la gravité
- Modèle XGBoost pour la classification multi-classes et binaire "Grave" vs "Non grave"
- Interprétation avec SHAP (importance des variables)

### 5. Visualisation
- Cartes des accidents graves par département (matplotlib + geopandas)
- Dashboard Power BI (non inclus ici)

---

## 🔍 Résultats clés

- Les modèles multi-classes montrent une bonne différenciation entre les niveaux de gravité
- Les accidents graves sont surreprésentés :
  - de nuit, sur routes bidirectionnelles, lors de chocs frontaux
  - chez certaines catégories d'usagers (ex. : piétons, cyclomotoristes)
- Variables les plus influentes (SHAP & XGBoost) : **heure**, **type de choc**, **catégorie d’usager**, **configuration de la route**
- La classification binaire atteint une AUC de XX% – utile pour une détection automatisée rapide

---

## 📊 Technologies utilisées

- **Python** : pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels, shap, xgboost  
- **Visualisation** : Power BI, matplotlib  
- **Analyse multivariée** : FactoMineR (R) / prince (Python)  
- **Cartographie** : geopandas, contextily

---


