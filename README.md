# Classification-des-Images-par-Reseaux-de-Neurones-CNN

Ce projet a pour objectif de mettre en œuvre des modèles de réseaux de neurones convolutifs (CNN) en utilisant la bibliothèque PyTorch pour classer des images satellites en détectant la présence ou l'absence d'éoliennes. Trois modèles différents ont été implémentés et comparés pour évaluer leurs performances.

## Auteurs
- BENHAMIDA Mohamed ELAmine
- NDIAYE Mamour

## Structure du projet

Le projet est organisé en trois dossiers, chacun contenant un modèle différent et ses prédictions au format CSV :

1. **Modele 1** : Contient le premier modèle CNN (MyNet1) et ses prédictions.
2. **Modele 2** : Contient le deuxième modèle CNN (MyNet) et ses prédictions.
3. **Modele 3** : Contient le troisième modèle CNN (SimpleCNN) et ses prédictions.

Chaque dossier contient :
- Le script Python du modèle (`model.ipynb`).
- Les prédictions du modèle sur les données de test (`pred.csv`).

## Description des modèles

### 1. Modèle 1
- **Architecture** : 
  - Deux couches de convolution suivies de max-pooling.
  - Couches de dropout pour éviter le surajustement.
  - Normalisation par lots (Batch Normalization).
  - Couches denses avec 120 et 84 neurones.
- **Fonction de perte** : `CrossEntropyLoss`.
- **Optimiseur** : Adam.
- **Précision sur le test** : **95.82%**.

### 2. Modèle 2
- **Architecture** :
  - Deux couches de convolution avec normalisation par lots.
  - Couches de dropout (50%) pour la régularisation.
  - Couches denses avec 120 et 84 neurones.
- **Fonction de perte** : `CrossEntropyLoss`.
- **Optimiseur** : Adam.
- **Précision sur le test** : **96,97%**.

### 3. Modèle 3
- **Architecture** :
  - Une couche de convolution avec padding pour conserver la taille de l'image.
  - Couches entièrement connectées avec 256 et 2 neurones.
  - Fonction d'activation ReLU.
- **Fonction de perte** : `CrossEntropyLoss`.
- **Optimiseur** : Adam.
- **Précision sur le test** : **96,94%**.

## Résultats de la comparaison

Les trois modèles ont été comparés sur un ensemble de 4993 images. Les résultats montrent que les modèles ont des performances très similaires, avec un taux de correspondance global de **94,25%**. Cela signifie que pour 94,25% des images, les modèles ont prédit la même valeur.

### Graphiques de performance
- **Modèle 1** : Précision d'entraînement de **99,14%** et précision de validation de **96,97%**.
- **Modèle 2** : Précision d'entraînement de **99,14%** et précision de validation de **96,97%**.
- **Modèle 3** : Précision d'entraînement de **97%** et précision de validation variant entre **92%** et **93%**.

## Comment exécuter le code

1. **Cloner le dépôt** :
   ```bash
  https://github.com/Benhamida-Elamine/Classification-des-Images-par-Reseaux-de-Neurones-CNN.git
