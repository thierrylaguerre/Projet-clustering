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

├── data/ # Dossier contenant les jeux de données bruts et traités ├── notebooks/ # Notebooks Jupyter pour exploration et expérimentation │ ├── 01_exploration.ipynb # Analyse exploratoire des données (EDA) │ ├── 02_preprocessing.ipynb # Pré-traitement des données │ ├── 03_clustering_models.ipynb # Expérimentation avec différents modèles de clustering │ └── 04_evaluation.ipynb # Évaluation et analyse comparative des résultats ├── scripts/ # Scripts pour exécuter les différentes étapes de l'analyse ├── results/ # Résultats et visualisations générés par les modèles ├── requirements.txt # Liste des dépendances Python nécessaires └── README.md # Fichier de description du projet


---

## Étapes du Projet

### 1. Exploration des Données
- Réalisation d'une analyse exploratoire (EDA) pour identifier :
  - Les tendances,
  - Les valeurs manquantes,
  - Les outliers,
  - Les relations entre les variables.
- Visualisations pour une meilleure compréhension des données.

### 2. Prétraitement
- Normalisation et standardisation des données.
- Encodage des variables catégoriques.
- Réduction de dimension avec la PCA (Analyse en Composantes Principales).

### 3. Modélisation
- Clustering avec les algorithmes suivants :
  - **K-Means**
  - **Gaussian Mixture Models (GMM)**
  - **Bisecting K-Means**
- Détermination du nombre optimal de clusters à l'aide de :
  - La silhouette,
  - Le BIC,
  - L'inertie intra-cluster.

### 4. Évaluation
- Comparaison des modèles en utilisant :
  - **Silhouette Score**
  - **Davies-Bouldin Index**
  - **Log-likelihood** (pour GMM)
  - **AIC et BIC** (pour GMM)

---

## Installation

### Prérequis
- **Python 3.8 ou supérieur**
- **Apache Spark**
- **Jupyter Notebook**

### Installation des Dépendances
1. Clonez le projet :
   ```bash
   git clone https://github.com/votre-utilisateur/votre-projet.git
   cd votre-projet

2. Installez les dépendances :
   ```bas
   pip install -r requirements.txt
   ```

## Utilisation

### Lancer le fichier .ipynb
1. Lancez Jupyter Notebook :
   ```bash
   jupyter notebook
   ```
2. Ouvrez le fichier notebooks/projet_clutering.ipynb.
Ce fichier contient tout le code pour :
* Explorer les données.
* Effectuer le prétraitement.
* Appliquer des modèles de clustering (K-Means, GMM, Bisecting K-Means).
* Évaluer les performances des modèles.
