# 📊  Projet : Tableau Dashboard – Analyse Cardiovasculaire
<img width="1536" height="672" alt="Patient Risk Healthcare" src="https://github.com/user-attachments/assets/4dd0c703-1cd7-4eec-ad0e-e7c9f03ae288" />

---
## 🩺1. Contexte du projet

Les maladies cardiovasculaires représentent l'une des principales causes de mortalité mondiale.
Dans ce projet, l’objectif est d’explorer un dataset médical contenant des informations cliniques (âge, tension artérielle, cholestérol, glucose, habitudes de vie…) afin de créer un dashboard interactif sous Tableau permettant de visualiser rapidement :
- l’état général d’une population de patients,
- les facteurs de risques les plus fréquents,
- la répartition des niveaux de cholestérol, glucose et tension,
- la distribution par genre et âge,
- une estimation visuelle du risque cardiovasculaire.
  
Ce travail s’inscrit dans un cadre pédagogique visant à développer les compétences en data visualization, data storytelling, et usage de Tableau.

---

## 🎯2. Objectifs

**Objectif général:**

Créer un dashboard clair et interactif permettant d’obtenir une vue d’ensemble sur la santé cardiovasculaire d’un groupe de patients.

 **Objectifs spécifiques:**
- Importer et préparer les données dans Tableau Desktop.
- Créer des KPI essentiels : nombre total de patients, âge moyen, répartition par genre.
- Construire des graphiques pour analyser :
     **le cholestérol**,
     **le glucose**,
     **la tension artérielle**,
     **les comportements (tabac, alcool, activité physique)**.
- Mettre en place une estimation visuelle du risque cardiovasculaire.
- Concevoir une présentation finale soignée et intuitive.

---

## 📂3. Description du dataset
Le jeu de données **Cardiovascular Disease dataset.csv** contient des informations anonymisées sur les patients et leurs interactions avec la clinique :


| **Colonne**      | **Description**                                                                 |
|------------------|---------------------------------------------------------------------------------|
| **id**           | Identifiant unique du patient                                                   |
| **age**          | Âge du patient exprimé en jours (pour obtenir l’âge en années : `Age_en_annee = age / 365.25`) |
| **gender**       | Sexe du patient (1 = Homme, 2 = Femme)                                          |
| **height**       | Taille du patient en centimètres                                                |
| **weight**       | Poids du patient en kilogrammes                                                 |
| **ap_hi**        | Pression artérielle systolique (mmHg)                                           |
| **ap_lo**        | Pression artérielle diastolique (mmHg)                                          |
| **cholesterol**  | Niveau de cholestérol (1 = normal, 2 = au-dessus de la norme, 3 = très élevé)   |
| **gluc**         | Niveau de glucose (1 = normal, 2 = élevé, 3 = très élevé)                       |
| **smoke**        | Statut tabagique (0 = non-fumeur, 1 = fumeur)                                   |
| **alco**         | Consommation d’alcool (0 = non, 1 = oui)                                        |
| **active**       | Niveau d’activité physique ,la marche, course, sport ... Etc.  (0 = faible, 1 = actif)                              |
| **cardio**       | Présence de maladie cardiovasculaire (0 = non, 1 = oui)                         |


---


## 🛠️4.Étapes principales du projet

**1. Collecte et importation des données:** 

   - Récupération du fichier CSV du dataset cardiovasculaire.
   - Vérification de l’intégrité des données et de la compatibilité avec Tableau.
      
**2. Création de champs calculés :**

- Conversion de l’âge:

<img width="200" height="200" alt="age_annee" src="https://github.com/user-attachments/assets/acf2cfdb-e342-4d50-a40d-8d62a6265222" />

- Tranche d’âge :

<img width="450" height="250" alt="tranche_age" src="https://github.com/user-attachments/assets/8e078379-fbad-414a-8084-390530178239" />

- highbp : Hypertension

<img width="300" height="300" alt="highbp" src="https://github.com/user-attachments/assets/74f00890-ab7c-4f87-892f-152c6b4469e5" />

- risk_score : Score de risque cardiovasculaire

<img width="450" height="250" alt="RiskScore" src="https://github.com/user-attachments/assets/f1dc56f6-b8e5-4b03-8eab-ef8e1c35e1fd" />

- category_tension : Classification de tension

<img width="450" height="250" alt="cat_tension" src="https://github.com/user-attachments/assets/1fadd607-cd06-415d-a25b-924575b77dba" />

- glucose_level : Niveau de glucose

<img width="350" height="150" alt="niveau_gluc" src="https://github.com/user-attachments/assets/64ff2d8c-0c66-4e2f-88e1-da2107ca9d01" />

- cholesterol_level : Niveau de cholestérol

<img width="450" height="250" alt="niveau_chol" src="https://github.com/user-attachments/assets/740551b8-b6c0-471f-bf10-0491fd2a5ba8" />




**3. Visualisations réalisées :**

- KPI Cards : total patients, age moyen, Habitudes de vie (% fumeurs, % consommateurs alcool, % Actif en sport)
  
<img width="600" height="400" alt="kpi card" src="https://github.com/user-attachments/assets/f83c671a-3ca1-48b7-a85c-47d7ea0596f5" />

- Donut chart : répartition par genre

 <img width="600" height="400" alt="donut_rep" src="https://github.com/user-attachments/assets/7846e512-3ab2-4712-b52f-33e84574d26d" />

- Histogramme : distribution d’âge

<img width="600" height="400" alt="histo_trancheAge" src="https://github.com/user-attachments/assets/abe46132-8fea-4136-9f84-c91c362da714" />

- Bar charts : cholestérol, glucose, tension
  
<img width="600" height="400" alt="niv_gluc" src="https://github.com/user-attachments/assets/5327b02a-e90e-4996-b6c0-76bf8d678c22" />



<img width="600" height="400" alt="niv_chol" src="https://github.com/user-attachments/assets/66436851-bc50-4d95-aee3-baf02b920d26" />



<img width="600" height="400" alt="cat_tens" src="https://github.com/user-attachments/assets/7573b687-c858-44c0-8c61-8c0936d7c2c5" />



- Bar chart par genre : Score de risque cardiovasculaire
  
<img width="600" height="400" alt="risk" src="https://github.com/user-attachments/assets/2fbad1cb-4e4d-4ebc-94d7-9cdc46cfb9a7" />



## 6. Construction du Dashboard

<img width="1633" height="792" alt="dashboard_final" src="https://github.com/user-attachments/assets/85dec931-31a0-4e2c-8874-371d84d274b7" />


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
