# Introduction

Ce projet GitLab va servir de point de départ pour la remise du projet de fouille de données. Il s'agit depuis votre compte GitLab de créer un projet à partir de ce dépôt pour récupérer la structure de base et au fur et à mesure y ajouter les scripts de préparation des données pour obtenir matrice individus-variables qui servira pour la prise en main, et ensuite l'analyse, et enfin le rapport.


Il y a donc quelques répertoires qu'il vous faudra utiliser et compléter (et nettoyer pour le rendu final) :

- `data.preparation`: il va contenir un sous-répertoire avec les scripts (R, python, bash, ...) permettant, à partir des fichiers de données fournis, d'obtenir la matrice (individus-variables ou individus-variables+classe) pour l'analyse de fouille de données. Il doit contenir aussi la documentation utilisateur qui indiquera comment configurer et utiliser les scripts pour obtenir la matrice.

- `analysis`: ce répertoire contiendra les scripts (R, python, ...) et/ou workflows (Knime, ...) ayant servi à l'analyse de la matrice de données et l'évaluation des performances.

- `rapport`: ce répertoire contiendra le rapport qui sera au format Markdown. Ainsi, il sera possible de le visualiser et de l'éditer directement sur GitLab ou bien localement tout en permettant un suivi des modifications et un travail collaboratif.

- `data`: ce répertoire contient en théorie les fichiers CSV fournis mais **il ne faut pas** concrètement les mettre sur GitLab (ni autre site accessible) puisque tout le monde les a déjà. En paramétrant git, cela permet de les avoir en local, avec les mêmes chemins et les mêmes noms, sans avoir à les mettre sur GitLab, et ainsi, les scripts de préparation des données devraient fonctionner plus facilement.


# Calendrier 2022-23

- **Etape 1 - 24 février** Groupes de projet (2 personnes par groupe), et définition des objectifs (quelles matrices individus-variables pour quelles analyses)
- **Etape 2 - 31 mars** Matrice de données *individus-variables* à fournir avec les scripts et la documentation utilisateur pour l'obtenir (cf. répertoire [data.preparation](./data.preparation)). Il faudra **envoyer un mail à Roland B. avec le lien vers votre projet** GitLab et aussi que votre projet soit accessible par lui (ajouter l'utilisateur rbarriot aux membres du projet avec le rôle *developper* ou *maintainer*).
- **Etape 3 - 14 avril** Fin du projet: **envoyer un mail à Roland B.** qui récupérera les dépôts de chaque projet pour évaluation (notamment les répertoires analysis et [rapport](./rapport)).

# Première étape : compte GitLab et clonage du projet

La première étape pour vous va donc être de créer un compte GitLab si vous n'en avez pas. Et ensuite, de cloner ce projet et d'inviter l'autre membre de votre groupe pour le projet afin d'avoir un seul et même projet par groupe.

Une fois que vous aurez un compte, pour importer ce projet dans votre compte :

- Faire *New project*
- Dans l'onglet *Import project* choisir *Repo by URL*
- Mettre l'URL : https://gitlab.com/rbarriot/datamining.abc.git et renseigner le *Project name*

GitLab va copier la totalité du projet et vous pourrez travailler sur votre propre copie.

# Remarques sur GitLab

- L'idée est de vous forcer à **utiliser git** pour, si ce n'est pas déjà le cas, vous familiariser avec le **suivi de versions** de scripts et autres. C'est particulièrement important lorsqu'on a une version qui fonctionne et que l'on cherche à modifier. Et c'est une **compétence demandée** dans le privé comme dans le public.
- En plus, cela va me permettre de suivre le niveau d'activité de votre projet et des contributions.
- Il est donc important pour chacun de vous d'utiliser git, GitLab et leurs fonctionnalités. Il ne s'agit surtout pas de cloner une fois le projet au début, puis de travailler uniquement sur votre copie, pour déposer toutes les modifications à la fin en une fois. GitLab devrait **vous permettre de vous répartir certaines tâches** puis déposer et partager vos résultats avec l'autre membre de votre groupe. De même, pour la rédaction de la doc utilisateur et du rapport. Cela devrait vous permettre de vous répartir des parties à rédiger pour ensuite fusionner les documents produits chacun de votre côté.

# Liens

- Description des données fournies : http://silico.biotoul.fr/enseignement/m1/datamining/projet/DataMining.ABC.Presentation.des.donnees.html
- Données: https://silico.biotoul.fr/enseignement/m1/datamining/projet/data/

