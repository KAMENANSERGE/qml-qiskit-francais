# Introduction au Quantum Machine Learning avec Qiskit

Cours pratique en français : construire et évaluer deux classifieurs quantiques
(VQC et QSVC) sur le jeu de données Iris, puis les comparer à des modèles classiques.

## Contenu
1. Rappels : superposition, intrication, mesure
2. Encodage des données (encodage par angle, ZZFeatureMap)
3. Classifieur variationnel (VQC) et boucle hybride quantique-classique
4. Noyaux quantiques et QSVC
5. Comparaison avec la régression logistique et la SVM classique
6. Exercices

## Résultats (simulateur sans bruit)
| Modèle | Précision entraînement | Précision test |
|---|---|---|
| QSVC (quantique) | 1,00 | 0,97 |
| SVM classique (RBF) | 0,98 | 0,97 |
| Régression logistique | 0,96 | 0,93 |
| VQC (quantique) | 0,53 | 0,60 |

Le VQC est sensible au point de départ de l'entraînement : sans initialisation
fixe, sa précision de test varie entre 0,40 et 0,60 d'une exécution à l'autre.
Le notebook fixe ce point de départ (graine 42) pour rendre les résultats reproductibles.

Sur des données aussi simples, aucun avantage quantique n'est attendu :
l'objectif est d'apprendre la méthode et de comparer honnêtement avec le classique.

## Lancer le notebook
Sur votre ordinateur :
pip install qiskit qiskit-machine-learning scikit-learn matplotlib pylatexenc pandas notebook
jupyter notebook

Ou dans Google Colab, en activant la cellule d'installation.
Testé avec Qiskit 2.6 et Qiskit Machine Learning 0.9.

## Auteur
Serge Alain Kamenan, certifié IBM Quantum
(Fundamentals of Quantum Algorithms, Basics of Quantum Information, Quantum Business Foundations).
Badges vérifiables : https://www.credly.com/users/serge-alain-kamenan
