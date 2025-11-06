Description du projet

Ce dépôt regroupe le notebook « REAL_ESTATE_PRICE_PREDICTION.ipynb » et l’ensemble du code utilisé pour participer au challenge hébergé sur Challenge Data (plate-forme de défis data) — il s’agit du challenge numéro 68 (“Challenge Data 68”). Le défi consistait à prédire le prix de vente de biens immobiliers à partir d’un jeu de données tabulaire fourni (caractéristiques du bien, localisation, surface, typologie, etc).
Notre objectif : concevoir un pipeline complet (cleaning / feature engineering / modélisation) capable de générer des prédictions robustes, pour obtenir un bon classement dans la compétition.

Pipeline et méthodologie

Exploration & préparation des données : analyses univariées et bivariées, imputation des valeurs manquantes, traitement des valeurs aberrantes et des variables extrêmes.

Feature engineering : encodage des variables catégorielles (One-Hot ou Target Encoding selon la nature), standardisation des variables numériques, création de nouvelles variables (ex : âge du bien, point milieu d’étage, durée de bail restante).

Modélisation : en plus d’un modèle de base linéaire, un modèle d’arbre de décision basé sur XGBoost a été utilisé comme modèle principal pour ses performances élevées sur données tabulaires.

Optimisation : recherche d’hyperparamètres via une stratégie de recherche croisée (GridSearchCV ou RandomizedSearchCV) afin de maximiser la métrique d’évaluation (par ex., RMSE ou MAE).

Evaluation & export : la cible a été transformée en log pour stabiliser la variance, puis les prédictions ont été reconverties à l’échelle originale avant calcul des métriques finales. Le modèle entraîné et le pipeline complet sont exportés afin de pouvoir être réutilisés.

Résultats

Grâce à ce pipeline, nous avons terminé 20ᵉ sur 220 participants — un classement dans le top 10 % du challenge.
L’utilisation de XGBoost et d’un bon pré-traitement a donc permis d’atteindre une performance très compétitive.
Le notebook contient une section « Résultats » avec les métriques finales (RMSE, MAE, R²) sur le set de validation ou la soumission.
