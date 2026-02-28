<p align="center">
  <img src="figures/model_comparison.png" alt="Comparaison des performances des modèles" width="700"/>
</p>
# 🌍 Classification de la stabilité des terrains — Machine Learning Project

## 📌 Présentation
Ce projet a été réalisé dans le cadre d’un mini-projet académique en **Apprentissage Supervisé**.  
L’objectif est de construire un système de classification capable de prédire le **niveau de stabilité d’un terrain** afin d’identifier les zones à risque de glissement.

Ce problème relève d’une tâche de **classification multiclasse** avec trois catégories :
- Stable
- Moyennement stable
- Instable

---

## 🎯 Objectifs
Le projet vise à mettre en œuvre un pipeline complet de Machine Learning :

- Compréhension et analyse du dataset
- Prétraitement et nettoyage des données
- Visualisation et analyse exploratoire (EDA)
- Entraînement de plusieurs modèles de classification
- Optimisation des hyperparamètres
- Évaluation comparative des performances
- Interprétation des résultats

---

## 📊 Données utilisées
Le dataset contient des variables géotechniques et environnementales décrivant chaque zone :

**Variables explicatives**
- pente_pct — pente du terrain
- altitude_m — altitude
- texture_sol — texture du sol
- humidite_sol — humidité
- distance_faille_km — distance aux failles
- couverture_vegetale — couverture végétale
- indice_geotech_labo — indice géotechnique

**Variables spatiales (non utilisées pour l’entraînement)**
- latitude
- longitude
- zone_id

**Variable cible**
- stabilite_terrain

---

## ⚙️ Méthodologie

### 1 — Analyse exploratoire
- Distribution des variables
- Détection des anomalies
- Analyse du déséquilibre des classes
- Visualisations comparatives

### 2 — Prétraitement
- Nettoyage des données
- Suppression des doublons
- Traitement des valeurs manquantes
- Normalisation des variables numériques
- Encodage des variables catégorielles

### 3 — Modélisation
Plusieurs algorithmes ont été testés :

- XGBoost
- CatBoost
- LightGBM
- SVM
- Random Forest

Chaque modèle a été évalué :
- avec paramètres par défaut
- après optimisation par GridSearch

---

## 📈 Résultats

| Modèle | Accuracy | F1-score Macro | Observation |
|------|---------|----------------|-------------|
| XGBoost | 0.9871 | **0.8564** | Meilleur modèle |
| CatBoost | 0.9845 | 0.8388 | Très stable |
| LightGBM | 0.9871 | 0.8274 | Bon compromis |
| SVM | 0.9328 | 0.5747 | Performance moyenne |
| Random Forest | 0.9742 | 0.4242 | Mauvais équilibre |

---

## 🏆 Modèle retenu
Le modèle **XGBoost optimisé** a été sélectionné comme solution finale car il offre :

- le meilleur F1-score macro
- un bon équilibre entre les classes
- une excellente capacité de généralisation

---

## 📂 Structure du projet
