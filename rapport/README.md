# Préambule concernant la remise du projet

Pour la remise du projet, il s'agit d'envoyer un mail à RB lorsque votre projet GitLab sera finalisé.

**Pour l'évaluation, c'est le rapport de projet qui va compter le plus. Le reste de ce qui se trouve sur votre projet GitLab pourra éventuellement servir pour des éclaircissements lorsque ce n'est pas suffisamment clair dans le rapport.** 

Le rapport consiste en un fichier Markdown et devra remplacer ce README.

Bien qu'au format markdown, il est attendu un vrai rapport de projet : similaire à **un rapport** de stage et **devant se suffire à lui-même**, c'est-à-dire qu'il n'est pas nécessaire d'aller fouiller ailleurs dans votre projet GitLab pour comprendre ce qui a été fait, pourquoi, comment, pour quels résultats, quelles conclusions et quelles perspectives.

Points à vérifier avant la remise finale :

  * **Nettoyage :** supprimer tous les fichiers et répertoires qui ne sont pas nécessaires dans l'ensemble de votre projet GitLab afin qu'il ne reste que les informations utiles et pertinentes.
  * **Rapport :** vérifier que le rapport est bien présent dans ce répertoire et s'affiche correctement.
  * **Page d'accueil :** suggestion → ne laisser qu'une courte accroche sur la teneur de votre projet et mettre un lien vers le rapport

**Remarques :** 

  * il n'est pas impossible que vous utilisiez ultérieurement votre projet GitLab de fouille de données afin de mettre en valeur votre parcours pour soutenir une candidature à un poste.
  * pensez à utiliser le correcteur d'orthographe et/ou vous faire relire par quelqu'un d'autre
  * un rapport de projet ne contient en général pas de code, il faut plutôt décrire le(s) concept(s) et renvoyer éventuellement aux scripts qui seraient dans des annexes (« ce que l'on conçoit bien s'énonce clairement, et les mots pour le dire arrivent aisément », Nicolas Boileau)



# Contexte

Une brêve introduction sur le contexte (par exemple les systèmes ABC) et les objectifs clairs du projet : quelle question est posée.

![Transporteur ABC](transporteurs.png)

# Analyse

Donnez des précisions sur les objectifs à atteindre et comment y arriver. 

Effectuez une ou des analyses préliminaires des données pour les appréhender ainsi que les méthodes disponibles pour atteindre les objectifs.

# Conception

Fort de l'analyse précedente, présenter l'approche choisie et pourquoi. 

Ensuite, présenter quelle méthodologie vous allez mettre en oeuvre pour les différentes étapes du projet avec quelles méthodes :

  * Tout d'abord, présenter comment va être obtenue la matrice individus-variables+classes (sélection, transformation, nettoyage, ...)
  * Puis, comment elle va être utilisée pour produire des résultats (par exemple : quelle(s) méthode(s) de classification ou de clustering)
  * Enfin, quelle méthodologie sera mise en oeuvre pour l'évaluation des résultats obtenus (quelles mesures ou indicateurs pour évaluer quoi)

# Réalisation

Mise en oeuvre de ce qui a été conçu : il s'agit là de préciser les paramètres et tous les détails concernant la réalisation concrète de l'analyse. 

Inclure ensuite les résultats obtenus et/ou leur synthèse s'ils sont trop nombreux pour le format d'un rapport de projet.

# Discussion

Analyse et discussion sur les résultats obtenus. 

Conclusions sur la qualité de la ou des méhtodes mises en oeuvre.

# Bilan et perspectives

Qu'est-ce qui fonctionne ou pas. 

Pistes d'amélioration. 

Recul sur l'ensemble du projet et votre manière de l'aborder et de le réaliser. 

Si c'était à refaire... ou bien, quelles pourraient être les pistes d'investigation subséquentes ouvertes par les résultats obtenus ?

# Gestion du projet

* Comment s’est organisé le groupe.
* Comment se sont déroulées les discussions, les prises de décisions.
* Comment se sont réparties les tâches. Qui a fait quoi.
* Quels ont été les rôles et les contributions de chacun·e.
* Diagramme de Gantt avec le calendrier et les tâches.
* Section spéciale méthodologie de travail : Dans cette section, **vous devrez mentionner l'aide extérieure** que vous avez pu recevoir (d'autres étudiants ou connaissances) ou si vous avez travailler à plusieurs sur certaines parties du projet. **Vous devrez aussi mentionner l'utilisation ou la non utilisation de chatGPT** (ou autres IA) pour le code et/ou la rédaction.


# I. Introduction
## Contexte
Les maladies cardiovasculaires (MCV) représentent la principale cause de mortalité à l’échelle mondiale, responsable d’environ 17,9 millions de décès chaque année, soit environ 31 % de tous les décès mondiaux (World Health Organization, 2021). La majorité de ces décès sont causés par des crises cardiaques et des accidents vasculaires cérébraux (AVC). Ces statistiques mettent en évidence l'importance d'une détection précoce des facteurs de risque pour prévenir l'apparition de ces événements graves. En effet, un tiers des décès liés aux MCV surviennent chez des personnes de moins de 70 ans, soulignant ainsi la nécessité d’une prise en charge précoce, notamment au sein des populations jeunes. Les principaux facteurs de risque des MCV incluent l’hypertension, l’hyperlipidémie, le diabète et des antécédents de maladies cardiaques. La combinaison de ces facteurs peut précipiter l'apparition de maladies cardiaques graves si elle n'est pas identifiée et gérée à temps (Benjamin et al., 2019). 
Dans ce contexte, l'utilisation de modèles d’apprentissage automatique (machine learning) pour prédire les risques de maladies cardiovasculaires devient de plus en plus populaire dans le domaine médical. Ces modèles permettent d'analyser de grandes quantités de données médicales et biologiques pour déterminer quels facteurs sont les plus influents dans la survenue des MCV (Byrsell et al., 2021; Rafi et al., 2022). L’objectif est de permettre un diagnostic plus rapide et précis, et d’améliorer le suivi des patients, tout en optimisant les traitements.

L’objectif de ce projet est de tester différents algorithmes de classification pour prédire la présence de maladies cardiovasculaires à partir de données cliniques et biologiques. L’analyse sera menée en plusieurs étapes : d’abord, le prétraitement des données incluant le nettoyage et la normalisation des variables ; puis l’application et la comparaison de divers modèles de classification ; et enfin, l’évaluation des performances des modèles suivie d’une analyse des facteurs de risque majeurs. Ce travail s’inscrit dans une démarche de détection précoce des maladies cardiovasculaires, en vue de proposer des pistes d’amélioration pour la prévention et la gestion des risques.
