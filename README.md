# Analyse de la Personnalité des Clients

## Description du Projet

Ce projet vise à réaliser une **analyse de la personnalité des clients** à partir d'un jeu de données.  
L'objectif est de comprendre les différents segments de clients afin d'aider les entreprises à personnaliser leurs produits et campagnes marketing pour répondre aux besoins spécifiques de leurs clients.

L'approche consiste à :
1. Explorer les données,
2. Effectuer un prétraitement,
3. Appliquer des techniques de clustering (K-Means, GMM, Bisecting K-Means),
4. Évaluer les performances des modèles pour sélectionner la meilleure méthode de segmentation.

---

## Structure du Projet

Le projet est organisé de manière professionnelle selon la structure suivante :

``` ├── data/ # Dossier contenant les jeux de données bruts et traités ├── notebooks/ # Notebooks Jupyter pour exploration et expérimentation │ ├── 01_exploration.ipynb # Analyse exploratoire des données (EDA) │ ├── 02_preprocessing.ipynb # Pré-traitement des données │ ├── 03_clustering_models.ipynb # Expérimentation avec différents modèles de clustering │ └── 04_evaluation.ipynb # Évaluation et analyse comparative des résultats ├── scripts/ # Scripts pour exécuter les différentes étapes de l'analyse ├── results/ # Résultats et visualisations générés par les modèles ├── requirements.txt # Liste des dépendances Python nécessaires └── README.md # Fichier de description du projet
