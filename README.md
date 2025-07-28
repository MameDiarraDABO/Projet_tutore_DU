# Analyse des accidents corporels de la route en France

# 🚗 Analyse des accidents corporels de la route en France

🎓 **Projet tuteuré – Master 2 Big Data, Data Science & Analyse des Risques**  
Université de Montpellier (2024–2025)

---

## 📌 Objectif du projet

Ce projet vise à identifier les **facteurs influençant la gravité des accidents corporels de la route** en France à partir des données publiques de la base BAAC (Bulletin d’Analyse des Accidents Corporels).

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
- Régression logistique (GLM binomial) pour prédire la gravité
- Modèle XGBoost pour la classification binaire "Grave" vs "Non grave"
- Interprétation avec SHAP (importance des variables)

### 5. Visualisation
- Cartes des accidents graves par département (matplotlib + geopandas)
- Dashboard Power BI (non inclus ici)

---

## 🔍 Résultats clés

- Les accidents graves sont surreprésentés la nuit, sur routes bidirectionnelles, avec choc frontal
- Les variables les plus prédictives selon SHAP : **heure**, **type de choc**, **catégorie d’usager**, **situation du lieu**
- Le modèle XGBoost atteint une précision de XX%, avec une AUC de YY%

---

## 📊 Technologies utilisées

- **Python** : pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels, shap, xgboost  
- **Visualisation** : Power BI, matplotlib  
- **Analyse multivariée** : FactoMineR (R) / prince (Python)  
- **Cartographie** : geopandas, contextily

---

## 📁 Arborescence du dépôt


