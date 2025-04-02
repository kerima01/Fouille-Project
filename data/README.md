# **1- Descriptions des variables**  

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

# **2- Source**

Cet ensemble de données a été créé en combinant différents ensembles de données déjà disponibles indépendamment, mais non combinés auparavant. Dans cet ensemble de données, 5 ensembles de données cardiaques sont combinés sur 11 caractéristiques communes, ce qui en fait le plus grand ensemble de données sur les maladies cardiaques disponible à ce jour à des fins de recherche. Les cinq ensembles de données utilisés pour sa conservation sont :

Cleveland : 303 observations  
Hongrois : 294 observations  
Suisse : 123 observations  
Long Beach VA : 200 observations  
Ensemble de données Stalog (cœur) : 270 observations  
Total : 1190 observations  
Dupliqué : 272 observations  

Final dataset: 918 observations  

Chaque ensemble de données utilisé peut être trouvé sous l'index des ensembles de données de maladies cardiaques du référentiel d'apprentissage automatique de l'UCI sur le lien suivant : https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/
