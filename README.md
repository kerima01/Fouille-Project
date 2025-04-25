# Introduction

Ce projet GitLab va servir de point de départ pour la remise du projet de fouille de données. Il s'agit depuis votre compte GitLab de créer un projet à partir de ce dépôt pour récupérer la structure de base et au fur et à mesure y ajouter les scripts de préparation des données pour obtenir matrice individus-variables qui servira pour la prise en main, et ensuite l'analyse, et enfin le rapport.

Il y a donc quelques répertoires qu'il vous faudra utiliser et compléter (et **nettoyer pour le rendu final**) :

- `data.preparation`: il va contenir un sous-répertoire avec les scripts (R, python, bash, ...) permettant, à partir des fichiers de données fournis, d'obtenir la matrice (individus-variables ou individus-variables+classe) pour l'analyse de fouille de données. Il doit contenir aussi la documentation utilisateur qui indiquera comment configurer et utiliser les scripts pour obtenir la matrice.

- `analysis`: ce répertoire contiendra les scripts (R, python, ...) et/ou workflows (Knime, ...) ayant servi à l'analyse de la matrice de données et l'évaluation des performances.

- `rapport`: ce répertoire contiendra le rapport qui sera au format Markdown. Ainsi, il sera possible de le visualiser et de l'éditer directement sur GitLab ou bien localement tout en permettant un suivi des modifications et un travail collaboratif.

- `data`: ce répertoire contient les données de départ (brutes) permettant de réaliser le projet. La **provenance des données** doit être indiquée. Pour le projet ABC, **il ne faut pas** concrètement les mettre sur GitLab (ni autre site accessible) car je les ai. En paramétrant git, cela permet de les avoir en local, avec les mêmes chemins et les mêmes noms, sans avoir à les mettre sur GitLab, et ainsi, les scripts de préparation des données devraient fonctionner plus facilement.

# Calendrier 
## 2024-25

- **Rendu 1. 21 mars:** Groupes de projet (2 personnes par groupe)
  - **envoyer un mail à RB avec le lien vers votre projet** GitLab. Attention à ce que votre projet soit accessible par lui (ajouter l'utilisateur **@rbarriot** aux membres du projet avec le rôle *developper* ou *maintainer* s'il n'est pas public).
- **Phase A. Elaboration du projet : recherche d'un jeu de données dans un domaine relatif à la biologie (au sens très large : santé-médecine-agro-environnement-écologie) et définition des objectifs**
  - Pour le jeu de données, il faudrait un volume minimum pour que cela soit intéressant : de l'ordre de **quelques centaines d'individus et une dizaine de variables**, au moins. Vous pouvez/devriez me demander si le jeu de données envisagé convient (merci de me donner le lien, le type de données, et le nombre d'invididus et de variables dans le mail).
- **Rendu 2. 4 avril:** Jeu de données initial et objectifs détaillés du projet
  - Objectifs détaillés ;
    - il s'agit de définir si c'est de la classification automatique ou du clustering (ou des règles d'association), exemples :
      - classification automatique : comparaison des paramètres pour une méthode et de leurs performance
      - classification automatique : comparaison de méthodes (arbre de décision, forêt aléatoire, ...) et de leurs performances
      - clustering : comparaison des résultas obtenus (clusters) par rapport à des classes connues
      - clustering : comparaison des résultas obtenus (clusters) avec différentes méthodes par rapport à des classes connues
      - clustering : analyse détaillée du contenu des clusters obtenus, certains pouvant bien définir des classes, d'autres moins bien
      - ...
    - quelles sont les variables utilisées, les transformations qu'il faudra effectuer, et la classe prédite (pour de la classification)
  - Mise à jour de la page d'accueil de votre gitlab avec la description du jeu de données qui va être utilisé, le lien vers les données, et une section **Objectifs** (sur la page d'accueil) décrivant succinctement l'analyse qui va être effectuée
- **Phase B. Exploration et analyse des données, sélection des variables pertinentes et constitution de la matrice *individus-variables* pour la fouille**
- **Rendu 3. 18 avril:** Matrice de données *individus-variables* à fournir avec les scripts et la documentation utilisateur pour l'obtenir 
  - Mise à jour du projet GitLab avec les données de départ (sauf si elles sont trop volumineuses) ainsi que la matrice dans le répertoire data et les scripts pour obtenir la matrice à partir des données dans le répertoire [data.preparation](./data.preparation)).
- **Phase C. Mise en oeuvre de la fouille et obtention des résultats et de leur évaluation sur la matrice *individus-variables***
- **Rendu 4. 25 avril:** Mise en forme et remise
  - Mise à jour du projet GitLab 
    - Page d'accueil : étude réalisée et principaux résultats obtenus
    - Répertoire [analysis](./analysis) avec les analyes effectuées (scripts R, python ou worklfow Knime, ...) mis en oeuvre pour obtenir les résultats et conclusions
    - Répertoire [rapport](./rapport) 
    - **Fin du projet :** **dépôser le rapport converti au format PDF sur [moodle](https://moodle.univ-tlse3.fr/mod/assign/view.php?id=494193)** et **envoyer un mail à RB** qui récupérera les dépôts de chaque projet pour évaluation.

# Première étape : compte GitLab et clonage du projet

La première étape pour vous va donc être de créer un compte GitLab si vous n'en avez pas. Et ensuite, de cloner ce projet et d'inviter l'autre membre de votre groupe pour le projet afin d'avoir un seul et même projet par groupe.

Une fois que vous aurez un compte, pour importer ce projet dans votre compte :

- Faire *New project*
- Dans l'onglet *Import project* choisir *Repo by URL*
- Mettre l'URL : https://gitlab.com/rbarriot/datamining.project.git et renseigner le *Project name*

GitLab va copier la totalité du projet et vous pourrez travailler sur votre propre copie.

# Remarques sur GitLab

- L'idée est de vous forcer à **utiliser git** pour, si ce n'est pas déjà le cas, vous familiariser avec le **suivi de versions** de scripts et autres. C'est particulièrement important lorsqu'on a une version qui fonctionne et que l'on cherche à modifier. Et, c'est une **compétence demandée** dans le privé comme dans le public.
- En plus, cela va me permettre de suivre le niveau d'activité de votre projet et des contributions.
- Il est donc important pour chacun de vous d'utiliser git, GitLab et leurs fonctionnalités. Il ne s'agit surtout pas de cloner une fois le projet au début, puis de travailler uniquement sur votre copie, pour déposer toutes les modifications à la fin en une fois. GitLab devrait **vous permettre de vous répartir certaines tâches** puis déposer et partager vos résultats avec l'autre membre de votre groupe. De même, pour la rédaction de la doc utilisateur et du rapport. Cela devrait vous permettre de vous répartir des parties à rédiger pour ensuite fusionner les documents produits chacun de votre côté.


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


Pour une analyse approfondie de la méthodologie employée, des résultats obtenus et des recommandations formulées, veuillez consulter le fichier README.md situé dans le repertoire **Rapport**.     
lien vers le rapport:  https://github.com/kerima01/Fouille-Project/blob/master/rapport/README.md

## **Références :**  
1- World Health Organization. (2021). Cardiovascular diseases (CVDs). Lien vers le rapport https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)  
2- Benjamin, E. J., et al. (2019). Heart Disease and Stroke Statistics—2019 Update: A Report From the American Heart Association.  
3- Rafi S., Gangloff C., Paulhet E., Grimault O., Soulat L., Bouzillé G., Cuggia M. (2022). Out-of-Hospital Cardiac Arrest Detection by Machine Learning Based on the Phonetic Characteristics of the Caller's Voice.  
4- Byrsell, F., Claesson, A., Ringh, M., Svensson, L., Jonsson, M., Nordberg, P., Forsberg, S., Hollenberg, J., & Nord, A. (2021). Machine learning can support dispatchers to better and faster recognize out-of-hospital cardiac arrest during emergency calls: A retrospective study.
