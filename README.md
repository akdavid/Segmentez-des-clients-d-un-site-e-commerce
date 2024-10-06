
# Segmentation Client pour Olist

## Contexte

Olist est une entreprise brésilienne qui offre une solution de vente sur les marketplaces en ligne. Votre mission en tant que consultant Data est de fournir une segmentation des clients d'Olist pour les aider à mieux cibler leurs campagnes de marketing et à améliorer leur service client. La segmentation doit être exploitable par l'équipe Marketing et permettre de distinguer les clients en termes de commandes et de satisfaction.

## Objectifs de la Mission

1. **Analyse Exploratoire des Données (EDA) :** 
   - Comprendre les données fournies par Olist (informations sur les commandes, produits, commentaires de satisfaction, localisation des clients).
   - Nettoyer et transformer les données pour les rendre exploitables pour une analyse approfondie.

2. **Segmentation Client :**
   - Utiliser des méthodes non supervisées (comme le clustering) pour identifier les différents profils de clients.
   - Évaluer la pertinence de la segmentation pour une utilisation par l'équipe Marketing.

3. **Analyse de la Stabilité des Segments :**
   - Évaluer la stabilité des segments de clients dans le temps.
   - Proposer une fréquence optimale de mise à jour de la segmentation pour garantir sa pertinence.

## Structure du Répertoire

- `.gitattributes` : Configurations Git LFS pour le suivi des fichiers volumineux.
- `.gitignore` : Liste des fichiers et dossiers à exclure du suivi Git.
- `00_customer_positions.ipynb` : Analyse préliminaire de la localisation des clients.
- `01_Analyse_Exploratoire_Des_Donnees.ipynb` : Analyse exploratoire des données (EDA) pour comprendre les caractéristiques des clients et des commandes.
- `02_Analyse_RFM_Des_Donnees_Clients.ipynb` : Mise en œuvre d'une analyse RFM (Récence, Fréquence, Montant) pour comprendre le comportement des clients.
- `03_k_means.ipynb` : Application de l'algorithme de clustering K-means sur les données client.
- `04_tsne_et_RFM_with_optimal_k.ipynb` : Utilisation de t-SNE pour la visualisation et avec nombre optimal de clusters pour K-means.
- `05_analyse_des_clusters.ipynb` : Analyse approfondie des clusters de clients obtenus.
- `06_kmeans_with_more_features.ipynb` : Clustering K-means avec davantage de variables pour enrichir la segmentation.
- `07_test_de_stabilite_splitting_data.ipynb` : Analyse de la stabilité des clusters en divisant les données.
- `08_CAH_and_ARI_with_kmeans.ipynb` : Comparaison de K-means avec CAH.
- `09_DBSCAN.ipynb` : Application de l'algorithme de clustering DBSCAN sur les données.
- `10_contrat_de_maintenance.ipynb` : Proposition d'un contrat de maintenance basé sur la stabilité des segments de clients.

- `customer_details_v3.csv` : Données détaillées des clients.
- `customer_map.html` : Visualisation géographique des clients.
- `database_structure.png` : Schéma de la structure de la base de données.
- `olist.db` : Base de données SQLite contenant les données de commandes, produits, satisfaction, localisation, etc.
- `requete_customer_details_v3` : Requête SQL utilisée pour extraire les détails des clients.
- `unique_customer_positions.csv` : Données de localisation des clients.

## Démarche Méthodologique

1. **Préparation des Données :**
   - Importation des données à partir de la base de données `olist.db`.
   - Nettoyage des données et création de nouvelles variables pour une meilleure compréhension des comportements clients.

2. **Segmentation RFM :**
   - Réalisation d'une première segmentation des clients basée sur la récence, la fréquence, et le montant (RFM).
   - Comparaison des groupes de clients obtenus.

3. **Clustering Avancé :**
   - Exploration de différentes méthodes de clustering (K-means, DBSCAN, CAH).
   - Optimisation du nombre de clusters pour K-means.
   - Analyse de la stabilité des segments dans le temps.

4. **Recommandations :**
   - Proposition d'une fréquence de mise à jour pour la segmentation.
   - Recommandations pour l'utilisation des segments dans les campagnes de marketing.

## Notes et Conseils
- Le code doit respecter la convention PEP8.
- Éviter la fuite de données dans la segmentation (ne pas utiliser de données futures pour prédire le présent).
- La segmentation doit être simple, exploitable et actionable pour l'équipe Marketing.

