
# PRÉDICTION DES MALADIES CARDIOVASCULAIRES PAR APPRENTISSAGE AUTOMATIQUE


# **1- Contexte**
Les maladies cardiovasculaires (MCV) représentent la première cause de mortalité dans le monde, avec environ 17,9 millions de décès par an, soit environ 31% de tous les décès mondiaux (World Health Organization, 2021) . Parmi ces décès, la grande majorité est due à des crises cardiaques et des accidents vasculaires cérébraux (AVC). Il est donc crucial d’identifier et de traiter les patients à risque avant l’apparition de ces événements graves.
De plus, un tiers des décès dus aux MCV survient chez des personnes de moins de 70 ans, soulignant l'importance de la détection précoce et de la prévention dans les populations jeunes (World Health Organization, 2021).
Les facteurs de risque des maladies cardiovasculaires comprennent des éléments comme l'hypertension, l'hyperlipidémie, le diabète ou l'existence de précédentes maladies cardiaques. La combinaison de ces facteurs peut précipiter l'apparition de maladies cardiaques graves si elle n'est pas identifiée et gérée à temps.

Les modèles d’apprentissage automatique (machine learning) sont de plus en plus utilisés dans le domaine médical pour prédire les risques associés à diverses pathologies, dont les maladies cardiovasculaires (Byrsell et Al., 2021 & Rafi S., et Al., 2022). L'idée est de pouvoir analyser rapidement et précisément de grandes quantités de données médicales et biologiques, en vue de déterminer quels facteurs influencent le plus la présence d'une maladie cardiaque.  

L’utilisation de ces modèles peut apporter une aide précieuse pour le diagnostic précoce, le suivi des patients et l'optimisation des traitements. Dans le cadre de ce projet, nous allons tester différents algorithmes de classification automatique afin de prédire la présence ou l'absence de maladies cardiaques à partir de caractéristiques cliniques et biologiques.

# **2- Objectifs**    
## **a. Préparation du jeu de données :**    
- **Prétraitement :** Nettoyage des données (gestion des valeurs manquantes, suppression de doublons). Sélection des variables (éliminer les variables non pertinentes ou redondantes) pour améliorer la performance des modèles.  
- **Normalisation :** Standardiser les variables numériques pour éviter les biais liés aux différences d’échelle.  
- **Visualisation :** Création d’une matrice individus-variables pour mieux comprendre la structure des données. Explorer la distribution des données et les relations entre les variables à l’aide de graphiques (boxplots, Histogramme).  

## **b. Mise en place des modèles de classification :**  
- **Application de plusieurs algorithmes :** Tester différentes approches (arbres de décision, forêts aléatoires, k-plus proches voisins, naïve bayes).  
- **Comparaison des modèles :** Analyser les forces et faiblesses de chaque méthode en fonction de leurs performances.  

## **c. Évaluation et sélection du modèle optimal :**  
- **Mesure des performances :** Utiliser des métriques pour comparer les modèles.  
- **Optimisation des paramètres :** Ajuster les paramètres des modèles pour améliorer la prédiction.  

## **d.  Interprétation et analyse des résultats :**  
- **Identification des facteurs de risque :** Déterminer les variables les plus influentes dans la prédiction des maladies cardiovasculaires.  
- **Discussion et recommandations :** Interpréter les résultats pour proposer des pistes d’amélioration en prévention et en détection précoce.    

# **3- Résultats principaux**  

Les analyses réalisées montrent que les modèles d'apprentissage automatique, notamment les forêts aléatoires et le Naïve Bayes avec lissage de Laplace, offrent d'excellentes performances en matière de prédiction des maladies cardiovasculaires. Ces modèles ont montré une précision, une sensibilité et une robustesse supérieures, mettant en évidence l'importance de certaines variables cliniques telles que la pente du segment ST (ST_Slope), l'indice Oldpeak, et les types de douleurs thoraciques (ChestPainType).  

Bien que certaines variables classiques comme l'âge ou la pression artérielle au repos aient eu un impact modéré dans notre modèle, elles restent essentielles dans un cadre clinique plus large. Ces résultats soulignent l'importance d'intégrer des tests dynamiques dans les protocoles de dépistage et plaident pour une médecine plus réactive et personnalisée.  

En conclusion, cette étude illustre la pertinence de l'apprentissage automatique dans l'aide à la décision médicale. Elle ouvre la voie à une meilleure stratification des risques, tout en soulignant la nécessité d'un dialogue constant entre la data science et le savoir médical pour garantir une application éthique, explicable et efficace de ces outils dans la pratique clinique.  


Pour une analyse approfondie de la méthodologie employée, des résultats obtenus et des recommandations formulées, veuillez consulter le fichier README.md situé dans le repertoire `rapport`.     
lien vers le rapport:  https://github.com/kerima01/Fouille-Project/blob/master/rapport/README.md


## **Auteurs ** 
Hawa BALDE  
Issa KERIMA-KHALIL

Master Bioinformatique et Biologie des Systèmes  
Université Toulouse Paul Sabatier 2024-2025

## **Références **  
1- World Health Organization. (2021). Cardiovascular diseases (CVDs). Lien vers le rapport https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)  
2- Benjamin, E. J., et al. (2019). Heart Disease and Stroke Statistics—2019 Update: A Report From the American Heart Association.  
3- Rafi S., Gangloff C., Paulhet E., Grimault O., Soulat L., Bouzillé G., Cuggia M. (2022). Out-of-Hospital Cardiac Arrest Detection by Machine Learning Based on the Phonetic Characteristics of the Caller's Voice.  
4- Byrsell, F., Claesson, A., Ringh, M., Svensson, L., Jonsson, M., Nordberg, P., Forsberg, S., Hollenberg, J., & Nord, A. (2021). Machine learning can support dispatchers to better and faster recognize out-of-hospital cardiac arrest during emergency calls: A retrospective study.
