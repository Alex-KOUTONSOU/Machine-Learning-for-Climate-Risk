# Machine-Learning-for-Climate-Risk
#  Prédiction des Arrêtés CatNat Sécheresse (2020-2025)

Ce projet vise à modéliser et prédire la reconnaissance administrative de l'état de **Catastrophe Naturelle (CatNat)** liée à la sécheresse en France. Il croise des données météorologiques de haute précision avec des indicateurs géologiques.

##  Aperçu du Projet
L'objectif est de confronter la réalité physique du stress hydrique (via l'indice SWI) à la décision administrative finale. Le modèle utilise un classifieur **XGBoost** pour identifier les communes susceptibles d'obtenir un arrêté.

### Points Clés :
* **Données Météo** : Soil Water Index (SWI) quotidien de Météo-France (2020-2025).
* **Données Géologiques** : Niveaux d'aléa Retrait-Gonflement des Argiles (RGA).
* **Cible** : Historique des arrêtés officiels de la Caisse Centrale de Réassurance (CCR).

##  Méthodologie
Le projet est divisé en trois phases majeures :
1. **Exploration Spatiale** : Cartographie du SWI et analyse de la teneur en argile par commune.
2. **Seuils Critiques** : Identification des épisodes extrêmes (5e percentile) par trimestre.
3. **Modélisation Prédictive** : Entraînement d'un modèle XGBoost sur la période 2020-2024 et test sur 2025.

##  Résultats du Modèle
Le modèle XGBoost atteint des performances exceptionnelles, démontrant que les critères de décision suivent une logique physique et géographique forte :
* **Score AUC-ROC** : 0.9911
* **Rappel (Recall) sur la classe 1** : 0.86 (86% des arrêtés réels détectés)
* **Variable la plus influente** : Localisation géographique (Lambert X/Y) suivie du SWI moyen.

