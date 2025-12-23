# Projet TensorFlow – TP6 Auto MPG


# Exercice 1 – Préparation des données

J’ai commencé par cette étape car un modèle ne peut pas bien apprendre si les données ne sont pas propres.
Ce que j’ai fait :
J’ai traité les valeurs manquantes de la variable Horsepower pour éviter des erreurs pendant l’entraînement.
J’ai aussi transformé la variable Origin en variables numériques (one-hot encoding),
car TensorFlow ne peut pas utiliser directement des catégories.

Résultat :
Les données sont prêtes à être utilisées par les modèles sans problème.


# Exercice 2 – Régression linéaire à une variable

L’objectif était de commencer avec un modèle très simple pour comprendre le principe de la régression.
Ce que j’ai fait :
J’ai entraîné un modèle pour prédire le MPG à partir d’une seule variable
(Horsepower, puis Weight).
J’ai aussi comparé deux optimiseurs (Adam et SGD) pour voir leur influence.

Résultat :
Le modèle reste limité, mais on voit que le poids est plus informatif que la puissance seule.


# Exercice 3 – Régression linéaire multi-variables

Utiliser une seule variable n’est pas suffisant pour bien prédire le MPG.
Ce que j’ai fait :
J’ai utilisé plusieurs caractéristiques en même temps.
J’ai ajouté une couche Dense de 10 neurones et ajusté le learning rate.

Résultat :
Les performances sont meilleures que pour la régression à une variable,
car le modèle utilise plus d’informations.



# Exercice 4 – Réseau de neurones profond

Je voulais tester un modèle plus puissant capable de capturer des relations plus complexes.
Ce que j’ai fait :
J’ai construit un réseau de neurones avec trois couches cachées (128, 64 et 32 neurones).
J’ai comparé deux fonctions d’activation : ReLU et Tanh.

Résultat :
Le modèle avec ReLU donne de meilleurs résultats et converge plus facilement.



# Exercice 5 – Évaluation des performances

Il est important de visualiser les performances et pas seulement regarder un chiffre.
Ce que j’ai fait :
J’ai évalué le modèle sur le jeu de test.
J’ai tracé un graphique entre les valeurs réelles et les valeurs prédites,
ainsi qu’un histogramme des erreurs.

Résultat :
Les prédictions suivent globalement les valeurs réelles,
même si certaines erreurs restent visibles.



# Exercice 6 – Feature Engineering

Le lien entre les variables et le MPG n’est pas forcément linéaire.

Ce que j’ai fait :
J’ai ajouté des variables polynomiales (Horsepower² et Horsepower³).
J’ai aussi appliqué une normalisation Min-Max pour stabiliser l’apprentissage.

Résultat :
Le modèle avec ces nouvelles variables obtient de meilleurs résultats
que le modèle linéaire simple.



# Exercice 7 – Régularisation

Les modèles plus complexes peuvent facilement sur-apprendre.

Ce que j’ai fait :
J’ai ajouté une régularisation L2 au modèle multi-variables
et observé les courbes de loss.

Résultat :
La régularisation permet de réduire le sur-apprentissage
et rend le modèle plus stable.



# Exercice 8 – Ajustement des hyperparamètres

Choisir les bons hyperparamètres à la main n’est pas toujours évident.

Ce que j’ai fait :
J’ai utilisé Keras Tuner pour chercher automatiquement
de meilleurs paramètres pour le réseau de neurones.

Résultat :
Le modèle obtenu est plus performant que le modèle initial.



# Exercice 9 – Validation croisée

Un simple découpage train/test peut donner une vision partielle des performances.
Ce que j’ai fait :
J’ai mis en place une validation croisée k-fold
et calculé la MAE moyenne sur tous les folds.

Résultat :
Les résultats sont cohérents et confirment les performances observées précédemment.



# Exercice 10 – Déploiement du modèle

Un modèle entraîné doit pouvoir être utilisé en pratique.
Ce que j’ai fait :
J’ai sauvegardé le modèle final, puis je l’ai rechargé.
J’ai aussi créé une petite application Flask
pour prédire le MPG à partir de nouvelles données.

Résultat :
Le modèle peut être réutilisé facilement sans être réentraîné.
*


# Conclusion

Ca m’a permis de mieux comprendre les différentes étapes d’un projet de machine learning.
J’ai vu l’impact du choix des données, du modèle et des paramètres sur les résultats.
Les réseaux de neurones donnent de meilleures performances,
mais les modèles simples restent utiles pour comprendre le problème.



Lien du dépôt GitHub contenant le code du projet et son execution avec tous les résultats !
