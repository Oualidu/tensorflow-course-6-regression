# Projet TensorFlow – TP6 Auto MPG

## Objectif du TP
Le but de ce TP est de prédire la consommation d’une voiture (MPG) à partir de ses caractéristiques
comme la puissance du moteur, le poids ou le nombre de cylindres, en utilisant TensorFlow et Keras.

Le dataset utilisé est le dataset Auto MPG.

---

## Travail réalisé

### Exercice 1 – Préparation des données
Dans cette partie, j’ai commencé par nettoyer les données.
Les valeurs manquantes de la variable Horsepower ont été remplacées,
et la variable Origin a été transformée en variables numériques (one-hot encoding).
Cette étape est nécessaire pour pouvoir entraîner les modèles.

---

### Exercice 2 – Régression linéaire à une variable
J’ai entraîné un modèle de régression linéaire simple pour prédire le MPG
à partir d’une seule variable (Horsepower puis Weight).
J’ai aussi comparé deux optimiseurs : Adam et SGD.
Cela permet de comprendre les limites d’un modèle très simple.

---

### Exercice 3 – Régression linéaire multi-variables
Dans cet exercice, j’ai utilisé plusieurs variables en même temps.
J’ai ajouté une couche Dense de 10 neurones et modifié le learning rate.
Les résultats sont meilleurs que pour la régression à une seule variable.

---

### Exercice 4 – Réseau de neurones profond
J’ai construit un réseau de neurones avec trois couches cachées
(128, 64 et 32 neurones).
J’ai comparé deux fonctions d’activation : ReLU et Tanh.
Le modèle avec ReLU donne de meilleurs résultats.

---

### Exercice 5 – Évaluation des performances
Le modèle simple a été évalué sur le jeu de test.
J’ai tracé un graphique comparant les valeurs réelles et les valeurs prédites,
ainsi qu’un histogramme des erreurs de prédiction.
Cela permet de visualiser les erreurs du modèle.

---

### Exercice 6 – Feature Engineering
J’ai ajouté des variables polynomiales à partir de Horsepower
(Horsepower² et Horsepower³).
J’ai aussi appliqué une normalisation Min-Max.
Le modèle avec ces nouvelles variables donne de meilleurs résultats
que le modèle linéaire simple.

---

### Exercice 7 – Régularisation
J’ai ajouté une régularisation L2 au modèle multi-variables.
J’ai observé son effet sur la loss d’entraînement et de validation,
ce qui permet de réduire le sur-apprentissage.

---

### Exercice 8 – Ajustement des hyperparamètres
J’ai utilisé Keras Tuner pour chercher automatiquement
de bons hyperparamètres pour le réseau de neurones.
Le modèle obtenu a de meilleures performances que le modèle initial.

---

### Exercice 9 – Validation croisée
J’ai mis en place une validation croisée k-fold
pour évaluer plus précisément les performances du modèle.
La MAE moyenne obtenue est cohérente avec les résultats précédents.

---

### Exercice 10 – Déploiement du modèle
Le modèle de réseau de neurones a été sauvegardé puis rechargé.
J’ai aussi créé une petite application Flask
qui permet d’envoyer des caractéristiques en entrée
et d’obtenir une prédiction du MPG.

---

## Résultats
Globalement, les modèles les plus performants sont
les réseaux de neurones profonds et les modèles optimisés.
Les modèles simples donnent des résultats moins précis,
mais permettent de mieux comprendre le problème.

---

## Technologies utilisées
- Python
- TensorFlow / Keras
- Pandas, NumPy
- Scikit-learn
- Google Colab
- Flask (pour le déploiement)

---

## Lien du projet
Le code complet du projet est disponible sur ce dépôt GitHub.
