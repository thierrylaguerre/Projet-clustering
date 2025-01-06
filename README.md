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
```
├── data/ # Dossier contenant les jeux de données bruts et traités
├── notebooks/ # Notebooks Jupyter pour exploration et expérimentation
│ ├── 01_exploration.ipynb # Analyse exploratoire des données (EDA)
│ ├── 02_preprocessing.ipynb # Pré-traitement des données
│ ├── 03_clustering_models.ipynb # Expérimentation avec différents modèles de clustering
│ └── 04_evaluation.ipynb # Évaluation et analyse comparative des résultats
├── scripts/ # Scripts pour exécuter les différentes étapes de l'analyse
├── results/ # Résultats et visualisations générés par les modèles
├── requirements.txt # Liste des dépendances Python nécessaires └── README.md # Fichier de description du projet
```

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
   ```bash
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

## Données

Les données utilisées sont des informations sur les clients, leurs habitudes d'achat, et leurs réponses aux campagnes marketing.

### Description des colonnes principales

| **Attribut**              | **Description**                                                              |
|----------------------------|------------------------------------------------------------------------------|
| `ID`                      | Identifiant unique du client                                                 |
| `Year_Birth`              | Année de naissance                                                          |
| `Education`               | Niveau d'éducation                                                          |
| `Marital_Status`          | Statut marital                                                              |
| `Income`                  | Revenu annuel                                                               |
| `Kidhome`                 | Nombre de jeunes enfants dans le foyer                                      |
| `Teenhome`                | Nombre d'adolescents dans le foyer                                          |
| `Dt_Customer`             | Date d'enregistrement dans la base de données                               |
| `Recency`                 | Nombre de jours depuis le dernier achat                                     |
| `MntWines`                | Montant dépensé sur les vins                                                |
| `MntFruits`               | Montant dépensé sur les fruits                                              |
| `MntMeatProducts`         | Montant dépensé sur les produits carnés                                     |
| `MntFishProducts`         | Montant dépensé sur les produits de la mer                                  |
| `MntSweetProducts`        | Montant dépensé sur les produits sucrés                                     |
| `MntGoldProds`            | Montant dépensé sur les produits en or                                      |
| `NumDealsPurchases`       | Nombre d'achats avec une remise ou dans une offre promotionnelle            |
| `NumWebPurchases`         | Nombre d'achats réalisés via le site web                                    |
| `NumCatalogPurchases`     | Nombre d'achats réalisés via des catalogues                                 |
| `NumStorePurchases`       | Nombre d'achats réalisés en magasin                                         |
| `NumWebVisitsMonth`       | Nombre de visites sur le site web au cours du dernier mois                  |
| `AcceptedCmp1` à `AcceptedCmp5` | Indicateurs binaires (1 ou 0) d'acceptation des campagnes marketing        |
| `Complain`                | Indicateur binaire (1 ou 0) si le client a déposé une plainte               |
| `Z_CostContact`           | Coût constant associé à la prise de contact                                 |
| `Z_Revenue`               | Revenu constant associé à une réponse positive                             |
| `Response`                | Réponse binaire (1 ou 0) à la dernière campagne marketing                   |

## Résultats attendus

L'objectif principal de ce projet est de segmenter efficacement les clients afin de permettre à l'entreprise d'optimiser ses campagnes marketing et d'améliorer ses performances commerciales. Voici les résultats attendus :  

### 1. **Segmentation des clients**
- Création de groupes homogènes de clients basés sur leurs comportements d'achat, leurs caractéristiques démographiques et leur interaction avec les campagnes marketing.  

### 2. **Visualisation des clusters**
- Production de graphiques illustrant les clusters.  

### 3. **Analyse des performances des modèles**
- Comparaison des résultats des algorithmes de clustering (K-Means, GMM, Bisecting K-Means) à l'aide des métriques suivantes :
  - Silohouette score pour les trois algorithmes.
  - Log-likelihood, BIC et AIC pour GMM.
