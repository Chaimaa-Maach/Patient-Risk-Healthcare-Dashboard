# 📊  Projet : Tableau Dashboard – Analyse Cardiovasculaire
<img width="1536" height="672" alt="Patient Risk Healthcare" src="https://github.com/user-attachments/assets/4dd0c703-1cd7-4eec-ad0e-e7c9f03ae288" />

## 🩺1. Contexte du projet


Une clinique souhaite suivre les risques de santé de ses patients afin d’identifier rapidement ceux présentant un risque élevé et de surveiller les tendances générales. 
Dans ce projet, l’objectif est d’explorer un dataset médical contenant des informations cliniques afin de créer un **dashboard interactif sous Tableau** permettant de visualiser rapidement :

- l’état général d’une population de patients,
- les facteurs de risques les plus fréquents,
- la répartition des niveaux de cholestérol, glucose et tension,
- la distribution par genre et âge,
- une estimation visuelle du risque cardiovasculaire.

## 2. Objectifs
### Objectif général
Créer un dashboard clair et interactif permettant une vue d’ensemble sur la santé cardiovasculaire.

### Objectifs spécifiques
- Importer et préparer les données dans Tableau.
- Créer des KPI : total patients, âge moyen, répartition par genre.
- Visualiser cholestérol, glucose, tension.
- Construire un indicateur de risque cardiovasculaire.
- Concevoir une présentation intuitive.

## 3. Description du dataset
| Variable | Description |
|---------|-------------|
| age | Âge en jours, converti en années |
| gender | 1 = femme, 2 = homme |
| cholesterol | 1 = normal, 2 = élevé, 3 = très élevé |
| gluc | 1 = normal, 2 = élevé, 3 = très élevé |
| ap_hi | Tension systolique |
| ap_lo | Tension diastolique |
| smoke/alco/active | Habitudes de vie |
| cardio | 1 = présence de maladie cardiovasculaire |

## 4. Préparation des données
### Conversion de l’âge
```
Age (Years) = INT([age] / 365)
```

### Catégorisation de la tension
```
IF [ap_hi] < 120 AND [ap_lo] < 80 THEN "Normale"
ELSE "Hypertension"
END
```

### Classification du risque
```
IF [cholesterol] > 1 OR [gluc] > 1 OR [HighBP] = 1 THEN "Au-dessus de la norme"
ELSE "Normal"
END
```

## 5. Visualisations réalisées
- KPI Cards : total patients, genre, âge moyen  
- Donut chart : répartition par genre  
- Histogramme : distribution d’âge  
- Bar charts : cholestérol, glucose, tension  
- Score de risque cardiovasculaire  
- Habitudes de vie : smoke, alco, active  

## 6. Construction du Dashboard
### Section 1 — KPIs
Conteneur horizontal : Total Patients, Genre, Âge moyen.

### Section 2 — Analyse clinique
Graphiques : Cholestérol, Glucose, Tension.

### Section 3 — Analyse du risque
Score de risque, répartition par âge ou genre.

### Section 4 — Habitudes de vie
Fumeurs, alcool, activité physique.

## 7. Résultats et interprétation
- Le cholestérol et glucose élevés augmentent le risque.
- L’hypertension est courante chez les patients à risque.
- L’âge influence fortement le risque, surtout après 50 ans.
- Légère dominance masculine selon le dataset.

## 8. Conclusion
Ce projet a permis :
- l’analyse d’un dataset médical,
- la création d’un dashboard complet sous Tableau,
- la compréhension des indicateurs cardiovasculaires.

Le dashboard final est clair, structuré et adapté à l’analyse de santé publique.
