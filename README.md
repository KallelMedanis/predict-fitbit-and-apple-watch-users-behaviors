# predict-fitbit-and-apple-watch-users-behaviors

# 1. Exploratory Data Analysis
## Checklist de base
#### Analyse de Forme :
- **variable target** : activity
- **lignes et colonnes** : 6264, 20
- **types de variables** : qualitatives : 2, quantitatives : 18
- Y'a pas de valeurs manquantes
#### Analyse de Fond :
- **Visualisation de la target** :
    - 22% Lying
    - 18% Running 7 METs
    - 16% Running 5 METs
    - 15% Running 3 METs
    - 15% Sitting
    - 14% Self Pace walk
- **Signification des variables** :
    - age
    - gender : binarie(0:femme,1;homme)
    - height : cm
    - weight : kg
    - steps  : steps/mins
    - calories
    - distance : en metres
    - entropy_heart : entropie du rythme cardiaque
    - entropy_setps : entropie des pas
    - resting_heart : 10e centile du coeur en repos
    - corr_heart_steps : Correlation rythme cardiaque/pas
    - intensity_karvonen : intensité 
    - sd_norm_heart : Écart type de la fréquence cardiaque
    - device
    - activity
  *Pour la variable activity on va éliminer l'activité "Lying" et mettre toutes les activités "Running 7 METs" , "Running 5 METs" et "Running 3 METs" pour faciliter l'analyse des données
- **Relation Variables / Target** :
    - target / hear_rate,calories,entropy_heart,corr_heart_steps,intensity_karvonen : les taux de hear_rate,calories,entropy_heart,corr_heart_steps,intensity_karvonen semblent liés a l'activité -> hypothese a tester
    - target/gender,height,weight,steps,distance,entropy_setps,resting_heart,norm_heart,sd_norm_heart	steps_times_distance,device :A ce qu'il parait l'activité ne dépend pas de ces variables
## Analyse plus détaillée

- **Relation Variables / Variables** :
    - une forte corrélation entre:
    *norm_heart et intensity_karvonen
    *entre intensity_karvonen et heart_rate
    
### hypotheses nulle du test d'ANOVA: 

    -Les activités des individus ont des steps,hear_rate,calories,entropy_heart,entropy_setps,corr_heart_steps,
    norm_heart,intensity_karvonen,sd_norm_heart ignificativement différents
    
