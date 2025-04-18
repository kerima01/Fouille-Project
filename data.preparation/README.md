Scripts accompagnés de la documentation utilisateur permettant d'obtenir la matrice *individus-variables* qui servira pour le projet à partir des fichiers présents dans le répertoire [data](../data) de votre projet.

**Pour la phase B (cf. [calendrier](../README.md#calendrier))**, vous devez ajouter dans ce répertoire **l'ensembles des scripts** qui me permettront d'obtenir **la même matrice que vous** pour la suite de votre projet.

Les scripts ne devraient utiliser que les données disponibles dans le répertoire [data](../data).

Je vous demande également de rédiger un peu de documentation pour cette partie. Il s'agit de remplacer ce README pour indiquer à l'utilisateur (rbarriot) comment faire pour obtenir votre matrice.

Le plan proposé est :
- qu'est-ce qu'on essaye de faire :\
  → à partir de quels fichiers de départs\
  → pour arriver à quelle matrice\
  → comment (utiliser tel script qui fait ceci de telle manière, puis tel autre qui fait cela, ...)
- pour faire quoi par la suite\
  → un peu plus de précisions sur ce que contient la matrice et comment vont être utilisées les lignes et les colonnes pour la classification ou le clustering.


**Remarque :** à la suite de ce dépôt, vous avez la possibilité d'apporter des modifications à votre matrice (et donc aux scripts pour l'obtenir) si elle ne s'avérait pas parfaitement adaptée ou incomplète par rapport à l'analyse que vous aviez prévue.




# Projet de Fouille de Données : Prédiction des Maladies Cardiovasculaires

## Objectif de ce script

Ce script R (voir `Projet_Fouille.Rmd`) réalise la préparation complète du jeu de données en vue d’une modélisation pour prédire la présence de maladies cardiovasculaires.  
Il s’agit de la première étape du projet, centrée sur le nettoyage, la transformation, l’analyse exploratoire et la normalisation des données.

---

## 1. Chargement et préparation des données

- Importation du fichier CSV (`heart.csv`) contenant les observations cliniques.
- Conversion automatique des colonnes de type caractère en facteurs pour faciliter l’analyse.
- Transformation de la variable cible `HeartDisease` : elle est recodée en deux classes `"Normale"` et `"Malade"` (au lieu de 0/1) pour une lecture plus intuitive.

---

## 2. Exploration des variables

### Variables numériques

- Sélection des variables numériques pertinentes :
  - `Age`, `RestingBP`, `Cholesterol`, `MaxHR`, `Oldpeak`
- Visualisation de leur distribution selon la classe (`HeartDisease`) :
  - Boxplots par variable pour repérer les différences entre groupes
  - Plots interactifs via `plotly`
  - Observation : certaines variables ont des échelles différentes, d’où la nécessité de les normaliser.

### Distribution des classes

- Diagramme en barres du nombre d’individus Normale vs Malade
- Ajout des effectifs directement sur les barres

---

## 3. Normalisation des variables numériques

- Calcul de la moyenne et de l’écart-type pour chaque variable
- Création d’une nouvelle version des données avec des z-scores (valeurs centrées réduites)
- Vérification : chaque variable a bien une moyenne ≈ 0 et un écart-type ≈ 1

Objectif : rendre les variables numériques comparables entre elles malgré des unités différentes.

- Visualisation après normalisation :
  - Graphiques en violon et nuages de points (jitter) pour montrer la distribution par classe

---

## 4. Analyse de corrélation

- Calcul de la matrice de corrélation entre les variables numériques normalisées
- Visualisation avec `corrplot`
- Analyse :
  - Aucune paire de variables n’a une corrélation forte (|corr| > 0.8)
  - Conclusion : on conserve toutes les variables numériques

---

## 5. Analyse des variables catégorielles

- Variables examinées : `Sex`, `ChestPainType`, `RestingECG`, `ExerciseAngina`, `ST_Slope`, `FastingBS`
- Application de tests du chi² pour évaluer l’indépendance avec la variable cible
- Résultats :
  - Toutes les variables présentent une relation statistiquement significative avec la présence de maladie
  - Visualisations : graphiques de contingence, `ggbivariate`, barplots croisés

---

## Conclusion de la préparation

- Toutes les variables (numériques et catégorielles) sont informatives et conservées pour la suite du projet.
- Les données sont maintenant nettoyées, normalisées et prêtes à être utilisées pour entraîner des modèles de classification.

---

## Fichiers concernés

- `Projet_Fouille.Rmd` : script complet reproductible (R Markdown)
- `data/heart.csv` : jeu de données d’origine
- `README.md` : ce fichier de documentation

---

## Auteurs / Contexte

Projet réalisé dans le cadre d’un cours de fouille de données (année universitaire 2024–2025), avec pour objectif de détecter précocement les risques de maladies cardiovasculaires à partir de données médicales.

**Auteurs :**  
- Issa KERIMA-KHALIL  
- Hawa-Mamadou BALDE


