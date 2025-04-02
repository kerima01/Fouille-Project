# **1- Contexte**
Les maladies cardiovasculaires (MCV) représentent la première cause de mortalité dans le monde, avec environ 17,9 millions de décès par an, soit environ 31% de tous les décès mondiaux (World Health Organization, 2021) . Parmi ces décès, la grande majorité est due à des crises cardiaques et des accidents vasculaires cérébraux (AVC). Il est donc crucial d’identifier et de traiter les patients à risque avant l’apparition de ces événements graves.
De plus, un tiers des décès dus aux MCV survient chez des personnes de moins de 70 ans, soulignant l'importance de la détection précoce et de la prévention dans les populations jeunes (World Health Organization, 2021).
Les facteurs de risque des maladies cardiovasculaires comprennent des éléments comme l'hypertension, l'hyperlipidémie, le diabète ou l'existence de précédentes maladies cardiaques. La combinaison de ces facteurs peut précipiter l'apparition de maladies cardiaques graves si elle n'est pas identifiée et gérée à temps.

Les modèles d’apprentissage automatique (machine learning) sont de plus en plus utilisés dans le domaine médical pour prédire les risques associés à diverses pathologies, dont les maladies cardiovasculaires (Byrsell et Al., 2021 & Rafi S., et Al., 2022). L'idée est de pouvoir analyser rapidement et précisément de grandes quantités de données médicales et biologiques, en vue de déterminer quels facteurs influencent le plus la présence d'une maladie cardiaque.  

L’utilisation de ces modèles peut apporter une aide précieuse pour le diagnostic précoce, le suivi des patients et l'optimisation des traitements. Dans le cadre de ce projet, nous allons tester différents algorithmes de classification automatique afin de prédire la présence ou l'absence de maladies cardiaques à partir de caractéristiques cliniques et biologiques.

# **2- Descriptions des variables**  

**Âge :** âge du patient [années]  
**Sexe :** sexe du patient [M : Homme, F : Femme]  
**Type de douleur thoracique :** type de douleur thoracique [TA : Angine typique, ATA : Angine de poitrine atypique, PAN : Douleur non anginale, ASY : Asymptomatique]  
**ReposBP :** pression artérielle au repos [mm Hg]  
**Cholestérol :** cholestérol sérique [mm/dl]  
**FastingBS :** glycémie à jeun [1 : si FastingBS > 120 mg/dl, 0 : sinon]  
**RestingECG :** résultats de l'électrocardiogramme au repos [Normal : Normal, ST : présentant une anomalie de l'onde ST-T (inversions des ondes T et/ou élévation ST ou dépression de > 0,05 mV), LVH : montrant une hypertrophie ventriculaire gauche probable ou définie selon les critères d'Estes]  
**MaxHR :** fréquence cardiaque maximale atteinte [valeur numérique entre 60 et 202]  
**ExerciceAngine :** angine induite par l'exercice [Y : Oui, N : Non]  
**Oldpeak :** oldpeak = ST [valeur numérique mesurée en dépression]  
**ST_Slope :** la pente du segment ST de l'exercice de pointe [Haut : pente ascendante, Plate : plate, bas : pente descendante]  
**Cardiopathie :** classe de sortie [1 : maladie cardiaque, 0 : normale]  

## **Références :**
1- World Health Organization. (2021). Cardiovascular diseases (CVDs). Lien vers le rapport https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)  
2- Benjamin, E. J., et al. (2019). Heart Disease and Stroke Statistics—2019 Update: A Report From the American Heart Association.  
3- Rafi S., Gangloff C., Paulhet E., Grimault O., Soulat L., Bouzillé G., Cuggia M. (2022). Out-of-Hospital Cardiac Arrest Detection by Machine Learning Based on the Phonetic Characteristics of the Caller's Voice.  
4- Byrsell, F., Claesson, A., Ringh, M., Svensson, L., Jonsson, M., Nordberg, P., Forsberg, S., Hollenberg, J., & Nord, A. (2021). Machine learning can support dispatchers to better and faster recognize out-of-hospital cardiac arrest during emergency calls: A retrospective study.
