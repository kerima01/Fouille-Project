# Génération de la matrice individus-variables pour la prédiction des maladies cardiovasculaires
___
## Objectif

L’objectif de cette phase est de construire une matrice individus-variables à partir du fichier de données brutes et réaliser la préparation complète du jeu de données en vue d’une modélisation pour prédire la présence de maladies cardiovasculaires.  
Il s’agit de la première étape du projet, centrée sur le nettoyage, la transformation, l’analyse exploratoire et la normalisation des données.

---

---

## Fichier de départ

- **Chemin :** `data/heart.csv`  
- **Contenu :** Données médicales anonymisées issues d’examens cliniques, avec notamment :
  - Des variables numériques : Age, RestingBP, Cholesterol, MaxHR, Oldpeak.
  - Des variables catégorielles : Sex, ChestPainType, RestingECG, ExerciseAngina, ST_Slope, FastingBS.
  - Une variable cible binaire : présence ou non d’une maladie cardiovasculaire (`HeartDisease`)

---

## Objectif : la matrice finale

La **matrice individus-variables** obtenue à l’issue de ce script contient :

- **Lignes :** chaque individu (patient) de l’échantillon
- **Colonnes :**
  - Variables **numériques standardisées** (z-score) : pour éliminer les différences d’échelle
  - Variables **catégorielles codées en facteurs**
  - Variable cible (`HeartDisease`) recodée en `"Normale"` ou `"Malade"`

Cette matrice est ensuite prête à être utilisée comme **entrée pour les algorithmes de classification**, où chaque ligne représente un individu décrit par ses caractéristiques cliniques.

---

## Étapes de génération

1. **Lancement du script principal :**
   - Fichier : `Projet_Fouille.Rmd` (R Markdown)
   - Ce fichier est exécutable directement dans RStudio (bouton "Knit") ou ligne par ligne dans un environnement R.

2. **Contenu du script :**
   - Chargement et conversion des types de données (`read_csv`, `mutate`)
   - Nettoyage : traitement des doublons, gestion des types, renommage de la variable cible
   - Sélection des variables pertinentes
   - Visualisation exploratoire (boxplots, violons, heatmaps)
   - Normalisation des variables numériques à l’aide du z-score (`scale`)
   - Analyse de corrélation pour éviter les redondances
   - Tests du chi² pour valider l’information portée par les variables catégorielles
   - Construction finale de la matrice avec toutes les variables conservées

3. **Résultat :**
   - Une table nommée `tb_final` dans le script R, qui constitue la **matrice individus-variables propre et prête à l’usage**.

---

## Utilisation future

Cette matrice sera utilisée pour :

- **Classification** : appliquer plusieurs modèles (arbres, forêts, KNN, Naïve Bayes, etc.)
- **Analyse des variables** : identification des facteurs les plus influents dans la détection de maladies cardiovasculaires

Les **lignes** représentent des individus, les **colonnes** représentent les descripteurs cliniques (quantitatifs ou qualitatifs) qui seront utilisés comme **entrées dans les modèles de prédiction**.

---

## Auteurs

Issa KERIMA-KHALIL  
Hawa BALDE  

Année universitaire 2024–2025 — Cours de Fouille de Données

